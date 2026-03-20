# 아키텍처 및 디자인 원칙

이 마켓플레이스는 세분화, 조합성, 최소 토큰 사용에 중점을 두고 업계 모범 사례를 따릅니다.

## 핵심 철학

### 단일 책임 원칙

- 각 플러그인은 **한 가지를 잘 수행합니다** (Unix 철학)
- 명확하고 집중된 목적 (5-10단어로 설명 가능)
- 평균 플러그인 크기: **3.4개 컴포넌트** (Anthropic의 2-8 패턴 준수)
- **비대한 플러그인 없음** - 모든 플러그인이 집중되고 목표 지향적

### 번들링보다 조합성 우선

- 필요에 따라 플러그인을 혼합하고 매칭
- 워크플로 오케스트레이터가 집중된 플러그인을 조합
- 강제된 기능 번들링 없음
- 플러그인 간 명확한 경계

### 컨텍스트 효율성

- 더 작은 도구 = 더 빠른 처리
- LLM 컨텍스트 윈도우에 더 잘 맞음
- 더 정확하고 집중된 응답
- 필요한 것만 설치

### 유지보수성

- 단일 목적 = 더 쉬운 업데이트
- 명확한 경계 = 독립적인 변경
- 적은 중복 = 더 간단한 유지보수
- 격리된 의존성

## 세분화된 플러그인 아키텍처

### 플러그인 분포

- **67개의 집중된 플러그인** 특정 사용 사례에 최적화
- **23개의 명확한 카테고리** (플러그인당 1-6개로 쉬운 발견)
- 도메인별로 조직화:
  - **Development**: 4개 플러그인 (디버깅, 백엔드, 프론트엔드, 다중 플랫폼)
  - **Security**: 4개 플러그인 (스캔, 규정 준수, 백엔드-API, 프론트엔드-모바일)
  - **Operations**: 4개 플러그인 (사건, 진단, 분산, 관찰성)
  - **Languages**: 7개 플러그인 (Python, JS/TS, 시스템, JVM, 스크립팅, 함수형, 임베디드)
  - **Infrastructure**: 5개 플러그인 (배포, 검증, K8s, 클라우드, CI/CD)
  - 그 외 18개 전문 카테고리

### 컴포넌트 분석

**99개의 전문화된 Agent**

- 깊이 있는 지식을 가진 도메인 전문가
- 아키텍처, 언어, 인프라, 품질, 데이터/AI, 문서화, 비즈니스, SEO 전반에 걸쳐 조직화
- 3단계 전략(Opus, Sonnet, Haiku)으로 성능과 비용에 최적화

**15개의 워크플로 오케스트레이터**

- 다중 agent 조정 시스템
- 풀스택 개발, 보안 강화, ML 파이프라인, 사건 대응 같은 복잡한 작업
- 사전 구성된 agent 워크플로

**71개의 개발 도구**

- 다음을 포함한 최적화된 유틸리티:
  - 프로젝트 스캐폴딩 (Python, TypeScript, Rust)
  - 보안 스캔 (SAST, 의존성 감사, XSS)
  - 테스트 생성 (pytest, Jest)
  - 컴포넌트 스캐폴딩 (React, React Native)
  - 인프라 설정 (Terraform, Kubernetes)

**107개의 Agent Skills**

- 모듈식 지식 패키지
- Progressive disclosure 아키텍처
- 18개 플러그인에 걸친 도메인별 전문 지식
- Spec 준수 (Anthropic Agent Skills Specification)

## 저장소 구조

```
claude-agents/
-- .claude-plugin/
|   -- marketplace.json          # 마켓플레이스 카탈로그 (67개 플러그인)
-- plugins/                       # 격리된 플러그인 디렉토리
|   -- python-development/
|   |   -- agents/               # Python 언어 agent
|   |   |   -- python-pro.md
|   |   |   -- django-pro.md
|   |   |   -- fastapi-pro.md
|   |   -- commands/             # Python 도구
|   |   |   -- python-scaffold.md
|   |   -- skills/               # Python skills (5개)
|   |       -- async-python-patterns/
|   |       -- python-testing-patterns/
|   |       -- python-packaging/
|   |       -- python-performance-optimization/
|   |       -- uv-package-manager/
|   -- backend-development/
|   |   -- agents/
|   |   |   -- backend-architect.md
|   |   |   -- graphql-architect.md
|   |   |   -- tdd-orchestrator.md
|   |   -- commands/
|   |   |   -- feature-development.md
|   |   -- skills/               # Backend skills (3개)
|   |       -- api-design-principles/
|   |       -- architecture-patterns/
|   |       -- microservices-patterns/
|   -- security-scanning/
|   |   -- agents/
|   |   |   -- security-auditor.md
|   |   -- commands/
|   |   |   -- security-hardening.md
|   |   |   -- security-sast.md
|   |   |   -- security-dependencies.md
|   |   -- skills/               # Security skills (1개)
|   |       -- sast-configuration/
|   -- c4-architecture/
|   |   -- agents/               # C4 아키텍처 agent
|   |   |   -- c4-code.md
|   |   |   -- c4-component.md
|   |   |   -- c4-container.md
|   |   |   -- c4-context.md
|   |   -- commands/
|   |       -- c4-architecture.md
|   -- ... (62개 이상의 격리된 플러그인)
-- docs/                          # 문서화
|   -- agent-skills.md           # Agent Skills 가이드
|   -- agents.md                 # Agent 레퍼런스
|   -- plugins.md                # 플러그인 카탈로그
|   -- usage.md                  # 사용 가이드
|   -- architecture.md           # 이 파일
-- README.md                      # 빠른 시작
```

## 플러그인 구조

각 플러그인에는 다음이 포함됩니다:

- **agents/** - 해당 도메인의 전문화된 agent (선택 사항)
- **commands/** - 해당 플러그인에 특화된 도구 및 워크플로 (선택 사항)
- **skills/** - Progressive disclosure를 포함한 모듈식 지식 패키지 (선택 사항)

### 최소 요구 사항

- 최소 하나의 agent 또는 하나의 command
- 명확하고 집중된 목적
- 모든 파일에 적절한 frontmatter
- marketplace.json에 항목 등록

### 플러그인 예시

```
plugins/kubernetes-operations/
-- agents/
|   -- kubernetes-architect.md   # K8s 아키텍처 및 설계
-- commands/
|   -- k8s-deploy.md            # 배포 자동화
-- skills/
    -- k8s-manifest-generator/   # Manifest 생성 skill
    -- helm-chart-scaffolding/   # Helm chart skill
    -- gitops-workflow/          # GitOps 자동화 skill
    -- k8s-security-policies/    # 보안 정책 skill
```

## Agent Skills 아키텍처

### Progressive Disclosure

Skills는 토큰 효율성을 위해 3단계 아키텍처를 사용합니다:

1. **Metadata** (Frontmatter): 이름과 활성화 기준 (항상 로드됨)
2. **Instructions**: 핵심 지침 및 패턴 (활성화될 때 로드됨)
3. **Resources**: 예제 및 템플릿 (필요에 따라 로드됨)

### Specification 준수

모든 skills는 [Agent Skills Specification](https://github.com/anthropics/skills/blob/main/agent_skills_spec.md)을 준수합니다:

```yaml
---
name: skill-name # 필수: hyphen-case
description: skill이 무엇을 하는지. [trigger]할 때 사용합니다. # 필수: < 1024 문자
---
# Progressive disclosure가 있는 skill 컨텐츠
```

### 이점

- **토큰 효율성**: 필요할 때만 관련 지식 로드
- **전문화된 전문 지식**: 비대함 없이 깊이 있는 도메인 지식
- **명확한 활성화**: 명시적 트리거는 원치 않는 호출 방지
- **조합성**: 워크플로 전반에서 skills를 혼합하고 매칭
- **유지보수성**: 격리된 업데이트는 다른 skills에 영향 없음

[Agent Skills](./agent-skills.md)에서 107개 skills에 대한 완전한 세부 사항을 확인하세요.

## 모델 구성 전략

### 2단계 아키텍처

시스템은 Claude Opus와 Sonnet 모델을 전략적으로 사용합니다:

| 모델  | 개수 | 사용 사례                                     |
| ------ | --------- | -------------------------------------------- |
| Opus   | 42개 agent | 중요 아키텍처, 보안, 코드 리뷰|
| Sonnet | 39개 agent | 복잡한 작업, 지능형 지원 |
| Haiku  | 18개 agent | 빠른 운영 작업 |

### 선택 기준

**Haiku - 빠른 실행 및 결정적 작업**

- 잘 정의된 스펙으로부터 코드 생성
- 확립된 패턴을 따르는 테스트 작성
- 명확한 템플릿으로 문서화 작성
- 인프라 운영 실행
- 데이터베이스 쿼리 최적화 수행
- 고객 지원 응답 처리
- SEO 최적화 작업 실행
- 배포 파이프라인 관리

**Sonnet - 복잡한 추론 및 아키텍처**

- 시스템 아키텍처 설계
- 기술 선택 결정
- 보안 감사 수행
- 아키텍처 패턴에 대한 코드 리뷰
- 복잡한 AI/ML 파이프라인 생성
- 언어별 전문 지식 제공
- 다중 agent 워크플로 오케스트레이션
- 비즈니스 중요 법무/HR 사항 처리

### 하이브리드 오케스트레이션

최적의 성능과 비용을 위해 모델 조합:

```
계획 단계 (Sonnet) -> 실행 단계 (Haiku) -> 검토 단계 (Sonnet)

예시:
backend-architect (Sonnet) API 설계
  |
Generate endpoints (Haiku) 스펙 구현
  |
test-automator (Haiku) 테스트 생성
  |
code-reviewer (Sonnet) 아키텍처 검증
```

## 성능 및 품질

### 최적화된 토큰 사용

- **격리된 플러그인** 필요한 것만 로드
- **세분화된 아키텍처** 불필요한 컨텍스트 감소
- **Progressive disclosure** (skills) 필요에 따라 지식 로드
- **명확한 경계** 컨텍스트 오염 방지

### 컴포넌트 커버리지

- **100% agent 커버리지** - 모든 플러그인은 최소 하나의 agent 포함
- **100% 컴포넌트 가용성** - 모든 99개 agent는 플러그인 전반에서 접근 가능
- **효율적인 분포** - 플러그인당 평균 3.4개 컴포넌트

### 발견성

- **명확한 플러그인 이름** 목적을 즉시 전달
- **논리적 분류** 23개 잘 정의된 카테고리
- **검색 가능한 문서화** 교차 참조 포함
- **쉬운 검색** 올바른 도구 찾기

## 디자인 패턴

### 패턴 1: 단일 목적 플러그인

각 플러그인은 하나의 도메인에 집중합니다:

```
python-development/
-- agents/           # Python 언어 전문가
-- commands/         # Python 프로젝트 스캐폴딩
-- skills/           # Python 특화 지식
```

**이점:**

- 명확한 책임
- 유지보수 용이
- 최소 토큰 사용
- 다른 플러그인과 조합 가능

### 패턴 2: 워크플로 오케스트레이션

오케스트레이터 플러그인은 여러 agent를 조정합니다:

```
full-stack-orchestration/
-- commands/
    -- full-stack-feature.md    # 7개 이상 agent 조정
```

**오케스트레이션:**

1. backend-architect (API 설계)
2. database-architect (스키마 설계)
3. frontend-developer (UI 구축)
4. test-automator (테스트 생성)
5. security-auditor (보안 리뷰)
6. deployment-engineer (CI/CD)
7. observability-engineer (모니터링)

### 패턴 3: Agent + Skill 통합

Agent는 추론을 제공하고 skills는 지식을 제공합니다:

```
사용자: "비동기 패턴을 사용하여 FastAPI 프로젝트 구축"
  |
fastapi-pro agent (오케스트레이션)
  |
fastapi-templates skill (패턴 제공)
  |
python-scaffold command (프로젝트 생성)
```

### 패턴 4: 다중 플러그인 조합

복잡한 워크플로는 여러 플러그인을 사용합니다:

```
기능 개발 워크플로:
1. backend-development:feature-development
2. security-scanning:security-hardening
3. unit-testing:test-generate
4. code-review-ai:ai-review
5. cicd-automation:workflow-automate
6. observability-monitoring:monitor-setup
```

## 버전 관리 및 업데이트

### 마켓플레이스 업데이트

- `.claude-plugin/marketplace.json`의 마켓플레이스 카탈로그
- 플러그인의 Semantic versioning
- 후방 호환성 유지
- 주요 변경사항에 대한 명확한 마이그레이션 가이드

### 플러그인 업데이트

- 개별 플러그인 업데이트는 다른 플러그인에 영향 없음
- Skills는 독립적으로 업데이트 가능
- Agent는 워크플로를 깨지 않고 추가/제거 가능
- Commands는 안정적인 인터페이스 유지

## 기여 가이드라인

### 플러그인 추가

1. 플러그인 디렉토리 생성: `plugins/{plugin-name}/`
2. Agent 및/또는 command 추가
3. 선택적으로 skills 추가
4. marketplace.json 업데이트
5. 적절한 카테고리에 문서화

### Agent 추가

1. `plugins/{plugin-name}/agents/{agent-name}.md` 파일 생성
2. Frontmatter 추가 (이름, 설명, 모델)
3. 포괄적인 시스템 프롬프트 작성
4. 플러그인 정의 업데이트

### Skill 추가

1. `plugins/{plugin-name}/skills/{skill-name}/SKILL.md` 파일 생성
2. YAML frontmatter 추가 (이름, "Use when"이 있는 설명)
3. Progressive disclosure가 있는 skill 컨텐츠 작성
4. marketplace.json의 플러그인 skills 배열에 추가

### 품질 기준

- **명확한 네이밍** - Hyphen-case, 설명적
- **집중된 범위** - 단일 책임
- **완전한 문서화** - 무엇, 언제, 어떻게
- **테스트된 기능** - 커밋 전 검증
- **Spec 준수** - Anthropic 가이드라인 준수

## 참고

- [Agent Skills](./agent-skills.md) - 모듈식 지식 패키지
- [Agent Reference](./agents.md) - 완전한 agent 카탈로그
- [Plugin Reference](./plugins.md) - 모든 67개 플러그인
- [Usage Guide](./usage.md) - 명령 및 워크플로
