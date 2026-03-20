# 사용 가이드

Agent, Slash Command 및 다중 Agent 워크플로우 사용에 대한 완전한 가이드입니다.

## 개요

플러그인 에코시스템은 두 가지 주요 인터페이스를 제공합니다:

1. **Slash Command** - Tool과 워크플로우의 직접 실행
2. **자연언어** - Claude가 사용할 Agent를 판단합니다.

## Slash Command

Slash Command는 Agent와 워크플로우를 작업하기 위한 주요 인터페이스입니다. 각 플러그인은 직접 실행할 수 있는 Namespace 명령어를 제공합니다.

### 명령어 형식

```bash
/plugin-name:command-name [arguments]
```

### 명령어 발견

설치된 플러그인의 사용 가능한 모든 Slash Command를 나열합니다:

```bash
/plugin
```

### Slash Command의 장점

- **직접 실행** - 자연언어로 설명할 필요가 없습니다.
- **구조화된 인자** - 정밀한 제어를 위해 매개변수를 명시적으로 전달합니다.
- **조합성** - 복잡한 워크플로우를 위해 명령어를 함께 연결합니다.
- **발견가능성** - `/plugin`을 사용하여 사용 가능한 모든 명령어를 확인합니다.

## 자연언어

특정 전문가를 사용해야 할 시기를 Claude가 판단해야 할 때 자연언어를 통해 Agent를 실행할 수도 있습니다:

```
"backend-architect를 사용하여 인증 API를 설계해줘"
"security-auditor가 OWASP 취약점을 스캔해줘"
"performance-engineer가 이 데이터베이스 쿼리를 최적화해줘"
```

Claude Code는 요청에 따라 자동으로 적절한 Agent를 선택하고 조정합니다.

## 카테고리별 명령어 참조

### 개발 및 기능

| 명령어 | 설명 |
| ---------------------------------------------- | ------------------------------------------- |
| `/backend-development:feature-development` | 백엔드 기능 엔드-투-엔드 개발 |
| `/full-stack-orchestration:full-stack-feature` | 완전한 풀스택 기능 구현 |
| `/multi-platform-apps:multi-platform` | 크로스 플랫폼 앱 개발 조정 |

### 테스트 및 품질

| 명령어 | 설명 |
| ----------------------------- | ------------------------------------- |
| `/unit-testing:test-generate` | 종합 단위 테스트 생성 |
| `/tdd-workflows:tdd-cycle` | 완전한 TDD 빨강-초록-리팩토링 사이클 |
| `/tdd-workflows:tdd-red` | 먼저 실패하는 테스트 작성 |
| `/tdd-workflows:tdd-green` | 테스트를 통과하는 코드 구현 |
| `/tdd-workflows:tdd-refactor` | 통과하는 테스트와 함께 리팩토링 |

### 코드 품질 및 검토

| 명령어 | 설명 |
| ----------------------------------- | -------------------------- |
| `/code-review-ai:ai-review` | AI 기반 코드 검토 |
| `/comprehensive-review:full-review` | 다중 관점 분석 |
| `/comprehensive-review:pr-enhance` | Pull Request 개선 |

### 디버깅 및 문제 해결

| 명령어 | 설명 |
| -------------------------------------- | ------------------------------ |
| `/debugging-toolkit:smart-debug` | 대화형 스마트 디버깅 |
| `/incident-response:incident-response` | 프로덕션 장애 관리 |
| `/incident-response:smart-fix` | 자동화된 장애 해결 |
| `/error-debugging:error-analysis` | 심화 오류 분석 |
| `/error-debugging:error-trace` | 스택 추적 디버깅 |
| `/error-diagnostics:smart-debug` | 스마트 진단 디버깅 |
| `/distributed-debugging:debug-trace` | 분산 시스템 추적 |

### 보안

| 명령어 | 설명 |
| ------------------------------------------ | ----------------------------------- |
| `/security-scanning:security-hardening` | 종합 보안 강화 |
| `/security-scanning:security-sast` | 정적 애플리케이션 보안 테스트 |
| `/security-scanning:security-dependencies` | 의존성 취약점 스캔 |
| `/security-compliance:compliance-check` | SOC2/HIPAA/GDPR 컴플라이언스 |
| `/frontend-mobile-security:xss-scan` | XSS 취약점 스캔 |

### 인프라 및 배포

| 명령어 | 설명 |
| ----------------------------------------- | ------------------------------- |
| `/observability-monitoring:monitor-setup` | 모니터링 인프라 설정 |
| `/observability-monitoring:slo-implement` | SLO/SLI 메트릭 구현 |
| `/deployment-validation:config-validate` | 배포 전 검증 |
| `/cicd-automation:workflow-automate` | CI/CD 파이프라인 자동화 |

### 데이터 및 ML

| 명령어 | 설명 |
| --------------------------------------- | ---------------------------------- |
| `/machine-learning-ops:ml-pipeline` | ML 학습 파이프라인 오케스트레이션 |
| `/data-engineering:data-pipeline` | ETL/ELT 파이프라인 구성 |
| `/data-engineering:data-driven-feature` | 데이터 기반 기능 개발 |

### 문서화

| 명령어 | 설명 |
| ---------------------------------------- | ------------------------------------------------------------------------------------------ |
| `/code-documentation:doc-generate` | 종합 문서 생성 |
| `/code-documentation:code-explain` | 코드 기능 설명 |
| `/documentation-generation:doc-generate` | OpenAPI 사양, 다이어그램, 튜토리얼 |
| `/c4-architecture:c4-architecture` | 종합 C4 아키텍처 문서 생성 (Context, Container, Component, Code) |

### 리팩토링 및 유지보수

| 명령어 | 설명 |
| --------------------------------------- | ---------------------------- |
| `/code-refactoring:refactor-clean` | 코드 정리 및 리팩토링 |
| `/code-refactoring:tech-debt` | 기술 부채 관리 |
| `/codebase-cleanup:deps-audit` | 의존성 감사 |
| `/codebase-cleanup:tech-debt` | 기술 부채 감소 |
| `/framework-migration:legacy-modernize` | 레거시 코드 현대화 |
| `/framework-migration:code-migrate` | Framework 마이그레이션 |
| `/framework-migration:deps-upgrade` | 의존성 업그레이드 |

### 데이터베이스

| 명령어 | 설명 |
| ---------------------------------------------- | ------------------------------- |
| `/database-migrations:sql-migrations` | SQL 마이그레이션 자동화 |
| `/database-migrations:migration-observability` | 마이그레이션 모니터링 |
| `/database-cloud-optimization:cost-optimize` | 데이터베이스 및 클라우드 최적화 |

### Git 및 PR 워크플로우

| 명령어 | 설명 |
| -------------------------------- | ---------------------------- |
| `/git-pr-workflows:pr-enhance` | Pull Request 품질 개선 |
| `/git-pr-workflows:onboard` | 팀 온보딩 자동화 |
| `/git-pr-workflows:git-workflow` | Git 워크플로우 자동화 |

### 프로젝트 Scaffolding

| 명령어 | 설명 |
| -------------------------------------------- | ---------------------------- |
| `/python-development:python-scaffold` | FastAPI/Django 프로젝트 설정 |
| `/javascript-typescript:typescript-scaffold` | Next.js/React + Vite 설정 |
| `/systems-programming:rust-project` | Rust 프로젝트 Scaffolding |

### AI 및 LLM 개발

| 명령어 | 설명 |
| ------------------------------------------- | ------------------------------- |
| `/llm-application-dev:langchain-agent` | LangChain Agent 개발 |
| `/llm-application-dev:ai-assistant` | AI Assistant 구현 |
| `/llm-application-dev:prompt-optimize` | Prompt Engineering 최적화 |
| `/agent-orchestration:multi-agent-optimize` | 다중 Agent 최적화 |
| `/agent-orchestration:improve-agent` | Agent 개선 워크플로우 |

### 테스트 및 성능

| 명령어 | 설명 |
| --------------------------------------------------- | -------------------- |
| `/performance-testing-review:ai-review` | 성능 분석 |
| `/application-performance:performance-optimization` | 앱 최적화 |

### 팀 협업

| 명령어 | 설명 |
| ----------------------------------- | --------------------------- |
| `/team-collaboration:issue` | 이슈 관리 자동화 |
| `/team-collaboration:standup-notes` | 스탠드업 노트 생성 |

### 접근성

| 명령어 | 설명 |
| ----------------------------------------------- | ------------------------ |
| `/accessibility-compliance:accessibility-audit` | WCAG 컴플라이언스 감사 |

### API 개발

| 명령어 | 설명 |
| ------------------------------------- | ----------------------- |
| `/api-testing-observability:api-mock` | API Mocking 및 테스트 |

### Context 관리

| 명령어 | 설명 |
| ------------------------------------- | ------------------------- |
| `/context-management:context-save` | 대화 Context 저장 |
| `/context-management:context-restore` | 이전 Context 복원 |

## 다중 Agent 워크플로우 예시

플러그인은 Slash Command를 통해 접근 가능한 사전 구성된 다중 Agent 워크플로우를 제공합니다.

### 풀스택 개발

```bash
# Command 기반 워크플로우 실행
/full-stack-orchestration:full-stack-feature "실시간 분석이 있는 사용자 대시보드"

# 자연언어 대안
"실시간 분석이 있는 사용자 대시보드를 구현해줘"
```

**Orchestration:** backend-architect -> database-architect -> frontend-developer -> test-automator -> security-auditor -> deployment-engineer -> observability-engineer

**실행 과정:**

1. 마이그레이션을 포함한 데이터베이스 스키마 설계
2. 백엔드 API 구현 (REST/GraphQL)
3. 상태 관리가 있는 프론트엔드 컴포넌트
4. 종합 테스트 스위트 (단위/통합/E2E)
5. 보안 감사 및 강화
6. Feature Flag가 있는 CI/CD 파이프라인 설정
7. 가시성 및 모니터링 구성

### 보안 강화

```bash
# 종합 보안 평가 및 수정
/security-scanning:security-hardening --level comprehensive

# 자연언어 대안
"보안 감사를 수행하고 OWASP 모범 사례를 구현해줘"
```

**Orchestration:** security-auditor -> backend-security-coder -> frontend-security-coder -> mobile-security-coder -> test-automator

### 데이터/ML 파이프라인

```bash
# 프로덕션 배포를 포함한 ML 기능 개발
/machine-learning-ops:ml-pipeline "고객 이탈 예측 모델"

# 자연언어 대안
"배포를 포함하여 고객 이탈 예측 모델을 구축해줘"
```

**Orchestration:** data-scientist -> data-engineer -> ml-engineer -> mlops-engineer -> performance-engineer

### 장애 대응

```bash
# 근본 원인 분석을 포함한 스마트 디버깅
/incident-response:smart-fix "결제 서비스의 프로덕션 메모리 누수"

# 자연언어 대안
"프로덕션 메모리 누수를 디버깅하고 실행 북을 만들어줘"
```

**Orchestration:** incident-responder -> devops-troubleshooter -> debugger -> error-detective -> observability-engineer

### C4 아키텍처 문서화

```bash
# 종합 C4 아키텍처 문서 생성
/c4-architecture:c4-architecture

# 자연언어 대안
"이 코드베이스에 대한 C4 아키텍처 문서를 만들어줘"
```

**Orchestration:** c4-code -> c4-component -> c4-container -> c4-context

**실행 과정:**

1. **Code Level**: 모든 하위 디렉토리의 상향식 분석으로 함수 서명 및 의존성을 포함한 코드 레벨 문서 작성
2. **Component Level**: 코드 문서를 인터페이스 및 관계가 있는 논리적 컴포넌트로 통합
3. **Container Level**: 컴포넌트를 OpenAPI/Swagger API 사양이 있는 배포 컨테이너에 매핑
4. **Context Level**: 사용자, 사용자 여정 및 외부 의존성이 있는 고수준 시스템 Context 생성

**출력:** `C4-Documentation/` 디렉토리의 완전한 C4 문서로 모든 레벨(Context, Container, Component, Code)의 Mermaid 다이어그램 포함

## 명령어 인자 및 옵션

많은 Slash Command는 정밀한 제어를 위해 인자를 지원합니다:

```bash
# 특정 파일에 대한 테스트 생성
/unit-testing:test-generate src/api/users.py

# 방법론 지정이 있는 기능 개발
/backend-development:feature-development OAuth2 integration with social login

# 보안 의존성 스캔
/security-scanning:security-dependencies

# 컴포넌트 Scaffolding
/frontend-mobile-development:component-scaffold UserProfile component with hooks

# TDD 워크플로우 사이클
/tdd-workflows:tdd-red User can reset password
/tdd-workflows:tdd-green
/tdd-workflows:tdd-refactor

# 스마트 디버깅
/debugging-toolkit:smart-debug memory leak in checkout flow

# Python 프로젝트 Scaffolding
/python-development:python-scaffold fastapi-microservice

# C4 아키텍처 문서 생성
/c4-architecture:c4-architecture
```

## 자연언어와 Command 결합하기

최적의 유연성을 위해 두 가지 방식을 혼합할 수 있습니다:

```
# 구조화된 워크플로우로 시작
/full-stack-orchestration:full-stack-feature "결제 처리"

# 그 다음 자연언어 지침 제공
"PCI-DSS 컴플라이언스를 보장하고 Stripe와 통합해줘"
"실패한 거래에 대한 재시도 로직을 추가해줘"
"사기 탐지 규칙을 설정해줘"
```

## 모범 사례

### Slash Command를 사용할 시기

- **구조화된 워크플로우** - 명확한 단계가 있는 다중 단계 프로세스
- **반복되는 작업** - 자주 수행하는 작업
- **정밀한 제어** - 특정 매개변수가 필요할 때
- **발견** - 사용 가능한 기능 탐색

### 자연언어를 사용할 시기

- **탐색 작업** - 어떤 Tool을 사용할지 불확실할 때
- **복잡한 추론** - Claude가 여러 Agent를 조정해야 할 때
- **Context 기반 결정** - 올바른 접근 방식이 상황에 따라 달라질 때
- **임시 작업** - Command에 맞지 않는 일회성 작업

### 워크플로우 구성

복잡한 시나리오를 위해 여러 플러그인을 구성합니다:

```bash
# 1. 기능 개발로 시작
/backend-development:feature-development payment processing API

# 2. 보안 강화 추가
/security-scanning:security-hardening

# 3. 종합 테스트 생성
/unit-testing:test-generate

# 4. 구현 검토
/code-review-ai:ai-review

# 5. CI/CD 설정
/cicd-automation:workflow-automate

# 6. 모니터링 추가
/observability-monitoring:monitor-setup
```

## Agent Skills 통합

Agent Skills는 Command와 함께 깊이 있는 전문성을 제공합니다:

```
사용자: "비동기 패턴이 있는 FastAPI 프로젝트를 설정해줘"
-> 활성화: fastapi-templates skill
-> 실행: /python-development:python-scaffold
-> 결과: 모범 사례가 있는 프로덕션 준비 FastAPI 프로젝트

사용자: "Helm이 있는 Kubernetes 배포를 구현해줘"
-> 활성화: helm-chart-scaffolding, k8s-manifest-generator skills
-> 가이드: kubernetes-architect agent
-> 결과: Helm Chart가 있는 프로덕션 등급 K8s Manifest
```

자세한 내용은 [Agent Skills](./agent-skills.md)를 참고하여 107개의 전문화된 Skill을 확인하세요.

## 참고 자료

- [Agent Skills](./agent-skills.md) - 전문화된 지식 패키지
- [Agent Reference](./agents.md) - 완전한 Agent 카탈로그
- [Plugin Reference](./plugins.md) - 모든 67개 플러그인
- [Architecture](./architecture.md) - 설계 원칙
