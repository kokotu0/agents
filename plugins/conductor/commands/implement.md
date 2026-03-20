---
description: "Execute tasks from a track's implementation plan following TDD workflow"
argument-hint: "[track-id] [--task X.Y] [--phase N]"
---

# Implement Track

Execute tasks from a track's implementation plan, following the workflow rules defined in `conductor/workflow.md`.

## Pre-flight Checks

1. Verify Conductor is initialized:
   - Check `conductor/product.md` exists
   - Check `conductor/workflow.md` exists
   - Check `conductor/tracks.md` exists
   - If missing: Display error and suggest running `/conductor:setup` first

2. Load workflow configuration:
   - Read `conductor/workflow.md`
   - Parse TDD strictness level
   - Parse commit strategy
   - Parse verification checkpoint rules

## Track Selection

### If argument provided:

- Validate track exists: `conductor/tracks/{argument}/plan.md`
- If not found: Search for partial matches, suggest corrections

### If no argument:

1. Read `conductor/tracks.md`
2. Parse for incomplete tracks (status `[ ]` or `[~]`)
3. Display selection menu:

   ```
   Select a track to implement:

   In Progress:
   1. [~] auth_20250115 - User Authentication (Phase 2, Task 3)

   Pending:
   2. [ ] nav-fix_20250114 - Navigation Bug Fix
   3. [ ] dashboard_20250113 - Dashboard Feature

   Enter number or track ID:
   ```

## Context Loading

Load all relevant context for implementation:

1. Track documents:
   - `conductor/tracks/{trackId}/spec.md` - Requirements
   - `conductor/tracks/{trackId}/plan.md` - Task list
   - `conductor/tracks/{trackId}/metadata.json` - Progress state

2. Project context:
   - `conductor/product.md` - Product understanding
   - `conductor/tech-stack.md` - Technical constraints
   - `conductor/workflow.md` - Process rules

3. Code style (if exists):
   - `conductor/code_styleguides/{language}.md`

## Track Status Update

Update track to in-progress:

1. In `conductor/tracks.md`:
   - Change `[ ]` to `[~]` for this track

2. In `conductor/tracks/{trackId}/metadata.json`:
   - Set `status: "in_progress"`
   - Update `updated` timestamp

## Task Execution Loop

For each incomplete task in plan.md (marked with `[ ]`):

### 1. Task Identification

Parse plan.md to find next incomplete task:

- Look for lines matching `- [ ] Task X.Y: {description}`
- Track current phase from structure

### 2. Task Start

Mark task as in-progress:

- Update plan.md: Change `[ ]` to `[~]` for current task
- Announce: "Starting Task X.Y: {description}"

### 3. TDD Workflow (if TDD enabled in workflow.md)

**Red Phase - Write Failing Test:**

```
Following TDD workflow for Task X.Y...

Step 1: Writing failing test
```

- Create test file if needed
- Write test(s) for the task functionality
- Run tests to confirm they fail
- If tests pass unexpectedly: HALT, investigate

**Green Phase - Implement:**

```
Step 2: Implementing minimal code to pass test
```

- Write minimum code to make test pass
- Run tests to confirm they pass
- If tests fail: Debug and fix

**Refactor Phase:**

```
Step 3: Refactoring while keeping tests green
```

- Clean up code
- Run tests to ensure still passing

### 4. Non-TDD Workflow (if TDD not strict)

- Implement the task directly
- Run any existing tests
- Manual verification as needed

### 5. Task Completion

**Commit changes** (following commit strategy from workflow.md):

```bash
git add -A
git commit -m "{commit_prefix}: {task description} ({trackId})"
```

**Update plan.md:**

- Change `[~]` to `[x]` for completed task
- Commit plan update:

```bash
git add conductor/tracks/{trackId}/plan.md
git commit -m "chore: mark task X.Y complete ({trackId})"
```

**Update metadata.json:**

- Increment `tasks.completed`
- Update `updated` timestamp

### 6. Phase Completion Check

After each task, check if phase is complete:

- Parse plan.md for phase structure
- If all tasks in current phase are `[x]`:

**Run phase verification:**

```
Phase {N} complete. Running verification...
```

- Execute verification tasks listed for the phase
- Run full test suite: `npm test` / `pytest` / etc.

**Report and wait for approval:**

```
Phase {N} Verification Results:
- All phase tasks: Complete
- Tests: {passing/failing}
- Verification: {pass/fail}

Approve to continue to Phase {N+1}?
1. Yes, continue
2. No, there are issues to fix
3. Pause implementation
```

**CRITICAL: Wait for explicit user approval before proceeding to next phase.**

## Error Handling During Implementation

### On Tool Failure

```
ERROR: {tool} failed with: {error message}

Options:
1. Retry the operation
2. Skip this task and continue
3. Pause implementation
4. Revert current task changes
```

- HALT and present options
- Do NOT automatically continue

### On Test Failure

```
TESTS FAILING after Task X.Y

Failed tests:
- {test name}: {failure reason}

Options:
1. Attempt to fix
2. Rollback task changes
3. Pause for manual intervention
```

### On Git Failure

```
GIT ERROR: {error message}

This may indicate:
- Uncommitted changes from outside Conductor
- Merge conflicts
- Permission issues

Options:
1. Show git status
2. Attempt to resolve
3. Pause for manual intervention
```

## Track Completion

When all phases and tasks are complete:

### 1. Final Verification

```
All tasks complete. Running final verification...
```

- Run full test suite
- Check all acceptance criteria from spec.md
- Generate verification report

### 2. Update Track Status

In `conductor/tracks.md`:

- Change `[~]` to `[x]` for this track
- Update the "Updated" column

In `conductor/tracks/{trackId}/metadata.json`:

- Set `status: "complete"`
- Set `phases.completed` to total
- Set `tasks.completed` to total
- Update `updated` timestamp

In `conductor/tracks/{trackId}/plan.md`:

- Update header status to `[x] Complete`

### 3. Documentation Sync Offer

```
Track complete! Would you like to sync documentation?

This will update:
- conductor/product.md (if new features added)
- conductor/tech-stack.md (if new dependencies added)
- README.md (if applicable)

1. Yes, sync documentation
2. No, skip
```

### 4. Cleanup Offer

```
Track {trackId} is complete.

Cleanup options:
1. Archive - Move to conductor/tracks/_archive/
2. Delete - Remove track directory
3. Keep - Leave as-is
```

### 5. Completion Summary

```
Track Complete: {track title}

Summary:
- Track ID: {trackId}
- Phases completed: {N}/{N}
- Tasks completed: {M}/{M}
- Commits created: {count}
- Tests: All passing

Next steps:
- Run /conductor:status to see project progress
- Run /conductor:new-track for next feature
```

## Progress Tracking

Maintain progress in `metadata.json` throughout:

```json
{
  "id": "auth_20250115",
  "title": "User Authentication",
  "type": "feature",
  "status": "in_progress",
  "created": "2025-01-15T10:00:00Z",
  "updated": "2025-01-15T14:30:00Z",
  "current_phase": 2,
  "current_task": "2.3",
  "phases": {
    "total": 3,
    "completed": 1
  },
  "tasks": {
    "total": 12,
    "completed": 7
  },
  "commits": [
    "abc1234: feat: add login form (auth_20250115)",
    "def5678: feat: add password validation (auth_20250115)"
  ]
}
```

## Resumption

If implementation is paused and resumed:

1. Load `metadata.json` for current state
2. Find current task from `current_task` field
3. Check if task is `[~]` in plan.md
4. Ask user:

   ```
   Resuming track: {title}

   Last task in progress: Task {X.Y}: {description}

   Options:
   1. Continue from where we left off
   2. Restart current task
   3. Show progress summary first
   ```

## Critical Rules

1. **NEVER skip verification checkpoints** - Always wait for user approval between phases
2. **STOP on any failure** - Do not attempt to continue past errors
3. **Follow workflow.md strictly** - TDD, commit strategy, and verification rules are mandatory
4. **Keep plan.md updated** - Task status must reflect actual progress
5. **Commit frequently** - Each task completion should be committed
6. **Track all commits** - Record commit hashes in metadata.json for potential revert

## Subagent Invocation Rules

Task 도구를 사용하여 서브에이전트를 호출할 때 다음 규칙을 따릅니다.

### 1. 호출 시점

- 단일 태스크가 독립적으로 실행 가능할 때
- 병렬로 여러 작업을 처리해야 할 때
- 특정 도메인 전문성이 필요한 작업

### 2. 모델 선택 기준

| 작업 유형 | 모델 | 이유 |
|----------|------|------|
| 일반 구현 작업 | sonnet | 비용 효율, 충분한 성능 |
| 검증/분석 (conductor-validator) | opus | 정확성 중요 |
| 탐색/간단한 작업 | haiku | 빠른 응답, 저비용 |

### 3. 에이전트 타입 매핑

| 작업 | subagent_type | 모델 |
|------|---------------|------|
| 프로젝트 검증 | conductor:conductor-validator | opus |
| 백엔드 구현 | python-development:python-pro | sonnet |
| 프론트엔드 구현 | frontend-mobile-development:frontend-developer | sonnet |
| 코드 리뷰 | code-reviewer | sonnet |
| E2E 테스트 | e2e-test | haiku |
| 테스트 자동화 | full-stack-orchestration:test-automator | sonnet |

### 4. 재호출 시 모델 업그레이드 규칙

코드 리뷰에서 문제가 발견되거나 사용자가 문제를 지적하여 **재호출이 필요한 경우**, 한 단계 상위 모델을 사용합니다:

| 최초 모델 | 재호출 시 모델 |
|----------|---------------|
| haiku | sonnet |
| sonnet | opus |
| opus | opus (유지) |

**재호출 판단 기준:**
- 코드 리뷰 결과 CRITICAL 또는 WARNING 이슈 발견
- 사용자가 구현 품질에 문제 제기
- 테스트 실패 후 수정 필요
- 동일 태스크 2회 이상 시도

### 5. 필수 파라미터

Task 도구 호출 시 반드시 다음을 명시합니다:

```
Task(
  subagent_type: "에이전트 타입",
  model: "sonnet",  // 반드시 명시
  prompt: "컨텍스트와 목표를 명확히 기술"
)
```
