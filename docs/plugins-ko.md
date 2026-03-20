# 완전한 플러그인 레퍼런스

**72개의 집중화된 단일 목적 플러그인**을 카테고리별로 정리하여 제공합니다.

## 빠른 시작 - 필수 플러그인

> 처음 시작하나요? 즉각적인 생산성 향상을 위해 이 인기 플러그인들을 설치하세요.

### 개발 필수 도구

**code-documentation** - 문서 작성 및 기술 문서화

```bash
/plugin install code-documentation
```

포괄적인 기술 문서를 위한 자동 문서 생성, 코드 설명, 튜토리얼 생성입니다.

**debugging-toolkit** - 스마트 디버깅 및 개발자 경험 최적화

```bash
/plugin install debugging-toolkit
```

대화형 디버깅, 에러 분석, 그리고 더 빠른 문제 해결을 위한 DX 최적화입니다.

**git-pr-workflows** - Git 자동화 및 PR 개선

```bash
/plugin install git-pr-workflows
```

Git 워크플로우 자동화, pull request 개선, 팀 온보딩 프로세스입니다.

### 풀스택 개발

**backend-development** - 백엔드 API 설계 및 아키텍처

```bash
/plugin install backend-development
```

RESTful 및 GraphQL API 설계, 테스트 주도 개발, 현대적 백엔드 아키텍처 패턴입니다.

**frontend-mobile-development** - UI 및 모바일 개발

```bash
/plugin install frontend-mobile-development
```

React/React Native 컴포넌트 개발, 자동 스캐폴딩, 크로스 플랫폼 구현입니다.

**full-stack-orchestration** - 엔드투엔드 기능 개발

```bash
/plugin install full-stack-orchestration
```

백엔드 → 프론트엔드 → 테스팅 → 보안 → 배포의 다중 에이전트 조정입니다.

### 테스팅 및 품질

**unit-testing** - 자동 테스트 생성

```bash
/plugin install unit-testing
```

pytest(Python) 및 Jest(JavaScript) 단위 테스트를 포괄적인 엣지 케이스 커버리지와 함께 자동 생성합니다.

**code-review-ai** - AI 기반 코드 리뷰

```bash
/plugin install code-review-ai
```

아키텍처 분석, 보안 평가, 실행 가능한 피드백이 포함된 코드 품질 리뷰입니다.

### 인프라 및 운영

**cloud-infrastructure** - 클라우드 아키텍처 설계

```bash
/plugin install cloud-infrastructure
```

AWS/Azure/GCP 아키텍처, Kubernetes 설정, Terraform IaC, 멀티클라우드 비용 최적화입니다.

**incident-response** - 프로덕션 인시던트 관리

```bash
/plugin install incident-response
```

빠른 인시던트 분류, 근본 원인 분석, 프로덕션 시스템을 위한 자동 해결 워크플로우입니다.

### 언어 지원

**python-development** - Python 프로젝트 스캐폴딩

```bash
/plugin install python-development
```

현대적 도구(uv, ruff)와 프로덕션 준비 아키텍처가 포함된 FastAPI/Django 프로젝트 초기화입니다.

**javascript-typescript** - JavaScript/TypeScript 스캐폴딩

```bash
/plugin install javascript-typescript
```

Next.js, React + Vite, 그리고 pnpm 및 TypeScript 모범 사례가 포함된 Node.js 프로젝트 설정입니다.

---

## 완전한 플러그인 카탈로그

### 개발 (5개 플러그인)

| 플러그인                        | 설명                                                  | 설치                                       |
| ------------------------------- | ------------------------------------------------------------ | --------------------------------------------- |
| **debugging-toolkit**           | 대화형 디버깅 및 DX 최적화                    | `/plugin install debugging-toolkit`           |
| **backend-development**         | GraphQL 및 TDD를 포함한 백엔드 API 설계                      | `/plugin install backend-development`         |
| **frontend-mobile-development** | 프론트엔드 UI 및 모바일 개발                           | `/plugin install frontend-mobile-development` |
| **ui-design**                   | 모바일(iOS, Android, React Native) 및 웹용 UI/UX 설계 | `/plugin install ui-design`                   |
| **multi-platform-apps**         | 크로스 플랫폼 앱 조정(웹/iOS/Android)            | `/plugin install multi-platform-apps`         |

### 문서화 (3개 플러그인)

| 플러그인                       | 설명                                                                                                                                     | 설치                                    |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| **code-documentation**       | 문서 생성 및 코드 설명                                                                                                                   | `/plugin install code-documentation`       |
| **documentation-generation** | OpenAPI 스펙, Mermaid 다이어그램, 튜토리얼                                                                                                      | `/plugin install documentation-generation` |
| **c4-architecture**          | 하향식 코드 분석, 컴포넌트 합성, 컨테이너 매핑, 컨텍스트 다이어그램을 포함한 포괄적인 C4 아키텍처 문서 워크플로우 | `/plugin install c4-architecture`          |

### 워크플로우 (4개 플러그인)

| 플러그인                       | 설명                                                                    | 설치                                    |
| ---------------------------- | ------------------------------------------------------------------------------ | ------------------------------------------ |
| **conductor**                | 추적, 사양 및 단계별 구현 계획을 포함한 컨텍스트 주도 개발 | `/plugin install conductor`                |
| **git-pr-workflows**         | Git 자동화 및 PR 개선                                              | `/plugin install git-pr-workflows`         |
| **full-stack-orchestration** | 엔드투엔드 기능 오케스트레이션                                               | `/plugin install full-stack-orchestration` |
| **tdd-workflows**            | 테스트 주도 개발 방법론                                            | `/plugin install tdd-workflows`            |

### 테스팅 (2개 플러그인)

| 플러그인            | 설명                                        | 설치                         |
| ----------------- | -------------------------------------------------- | ------------------------------- |
| **unit-testing**  | 자동 단위 테스트 생성(Python/JavaScript) | `/plugin install unit-testing`  |
| **tdd-workflows** | 테스트 주도 개발 방법론                | `/plugin install tdd-workflows` |

### 품질 (3개 플러그인)

| 플러그인                         | 설명                                   | 설치                                      |
| ------------------------------ | --------------------------------------------- | -------------------------------------------- |
| **code-review-ai**             | AI 기반 아키텍처 리뷰               | `/plugin install code-review-ai`             |
| **comprehensive-review**       | 다각도 코드 분석               | `/plugin install comprehensive-review`       |
| **performance-testing-review** | 성능 분석 및 테스트 커버리지 리뷰 | `/plugin install performance-testing-review` |

### 유틸리티 (4개 플러그인)

| 플러그인                    | 설명                                | 설치                                 |
| ------------------------- | ------------------------------------------ | --------------------------------------- |
| **code-refactoring**      | 코드 정리 및 기술 부채 관리 | `/plugin install code-refactoring`      |
| **dependency-management** | 의존성 감시 및 버전 관리 | `/plugin install dependency-management` |
| **error-debugging**       | 에러 분석 및 트레이스 디버깅         | `/plugin install error-debugging`       |
| **team-collaboration**    | 팀 워크플로우 및 스탠드업 자동화      | `/plugin install team-collaboration`    |

### AI 및 ML (4개 플러그인)

| 플러그인                   | 설명                         | 설치                                |
| ------------------------ | ----------------------------------- | -------------------------------------- |
| **llm-application-dev**  | LLM 앱 및 프롬프트 엔지니어링     | `/plugin install llm-application-dev`  |
| **agent-orchestration**  | 다중 에이전트 시스템 최적화     | `/plugin install agent-orchestration`  |
| **context-management**   | 컨텍스트 지속성 및 복원 | `/plugin install context-management`   |
| **machine-learning-ops** | ML 학습 파이프라인 및 MLOps     | `/plugin install machine-learning-ops` |

### 데이터 (2개 플러그인)

| 플러그인                    | 설명                        | 설치                                 |
| ------------------------- | ---------------------------------- | --------------------------------------- |
| **data-engineering**      | ETL 파이프라인 및 데이터 웨어하우스  | `/plugin install data-engineering`      |
| **data-validation-suite** | 스키마 검증 및 데이터 품질 | `/plugin install data-validation-suite` |

### 데이터베이스 (2개 플러그인)

| 플러그인                  | 설명                             | 설치                               |
| ----------------------- | ------------------------------------- | ------------------------------------- |
| **database-design**     | 데이터베이스 아키텍처 및 스키마 설계 | `/plugin install database-design`     |
| **database-migrations** | 데이터베이스 마이그레이션 자동화           | `/plugin install database-migrations` |

### 운영 (4개 플러그인)

| 플러그인                       | 설명                           | 설치                                    |
| ---------------------------- | ------------------------------------- | ------------------------------------------ |
| **incident-response**        | 프로덕션 인시던트 관리        | `/plugin install incident-response`        |
| **error-diagnostics**        | 에러 추적 및 근본 원인 분석 | `/plugin install error-diagnostics`        |
| **distributed-debugging**    | 분산 시스템 추적            | `/plugin install distributed-debugging`    |
| **observability-monitoring** | 메트릭, 로깅, 추적 및 SLO    | `/plugin install observability-monitoring` |

### 성능 (2개 플러그인)

| 플러그인                          | 설명                                | 설치                                       |
| ------------------------------- | ------------------------------------------ | --------------------------------------------- |
| **application-performance**     | 애플리케이션 프로파일링 및 최적화     | `/plugin install application-performance`     |
| **database-cloud-optimization** | 데이터베이스 쿼리 및 클라우드 비용 최적화 | `/plugin install database-cloud-optimization` |

### 인프라 (5개 플러그인)

| 플러그인                    | 설명                                 | 설치                                 |
| ------------------------- | ------------------------------------------- | --------------------------------------- |
| **deployment-strategies** | 배포 패턴 및 롤백 자동화 | `/plugin install deployment-strategies` |
| **deployment-validation** | 배포 전 검사 및 검증        | `/plugin install deployment-validation` |
| **kubernetes-operations** | K8s 매니페스트 및 GitOps 워크플로우          | `/plugin install kubernetes-operations` |
| **cloud-infrastructure**  | AWS/Azure/GCP 클라우드 아키텍처            | `/plugin install cloud-infrastructure`  |
| **cicd-automation**       | CI/CD 파이프라인 설정                | `/plugin install cicd-automation`       |

### 보안 (4개 플러그인)

| 플러그인                       | 설명                              | 설치                                    |
| ---------------------------- | ---------------------------------------- | ------------------------------------------ |
| **security-scanning**        | SAST 분석 및 취약점 스캔 | `/plugin install security-scanning`        |
| **security-compliance**      | SOC2/HIPAA/GDPR 준수               | `/plugin install security-compliance`      |
| **backend-api-security**     | API 보안 및 인증          | `/plugin install backend-api-security`     |
| **frontend-mobile-security** | XSS/CSRF 방지 및 모바일 보안  | `/plugin install frontend-mobile-security` |

### 현대화 (2개 플러그인)

| 플러그인                  | 설명                               | 설치                               |
| ----------------------- | ----------------------------------------- | ------------------------------------- |
| **framework-migration** | 프레임워크 업그레이드 및 마이그레이션 계획 | `/plugin install framework-migration` |
| **codebase-cleanup**    | 기술 부채 감소 및 정리      | `/plugin install codebase-cleanup`    |

### API (2개 플러그인)

| 플러그인                        | 설명                 | 설치                                     |
| ----------------------------- | --------------------------- | ------------------------------------------- |
| **api-scaffolding**           | REST/GraphQL API 생성 | `/plugin install api-scaffolding`           |
| **api-testing-observability** | API 테스팅 및 모니터링  | `/plugin install api-testing-observability` |

### 마케팅 (4개 플러그인)

| 플러그인                         | 설명                             | 설치                                      |
| ------------------------------ | --------------------------------------- | -------------------------------------------- |
| **seo-content-creation**       | SEO 콘텐츠 작성 및 계획        | `/plugin install seo-content-creation`       |
| **seo-technical-optimization** | 메타 태그, 키워드 및 스키마 마크업  | `/plugin install seo-technical-optimization` |
| **seo-analysis-monitoring**    | 콘텐츠 분석 및 권한 구축 | `/plugin install seo-analysis-monitoring`    |
| **content-marketing**          | 콘텐츠 전략 및 웹 리서치       | `/plugin install content-marketing`          |

### 비즈니스 (3개 플러그인)

| 플러그인                        | 설명                          | 설치                                     |
| ----------------------------- | ------------------------------------ | ------------------------------------------- |
| **business-analytics**        | KPI 추적 및 재무 보고 | `/plugin install business-analytics`        |
| **hr-legal-compliance**       | HR 정책 및 법률 템플릿      | `/plugin install hr-legal-compliance`       |
| **customer-sales-automation** | 지원 및 판매 자동화         | `/plugin install customer-sales-automation` |

### 프로그래밍 언어 (7개 플러그인)

| 플러그인                          | 설명                              | 설치                                       |
| ------------------------------- | ---------------------------------------- | --------------------------------------------- |
| **python-development**          | Django/FastAPI를 포함한 Python 3.12+         | `/plugin install python-development`          |
| **javascript-typescript**       | Node.js를 포함한 JavaScript/TypeScript       | `/plugin install javascript-typescript`       |
| **systems-programming**         | 시스템 개발을 위한 Rust, Go, C, C++ | `/plugin install systems-programming`         |
| **jvm-languages**               | 엔터프라이즈 패턴을 포함한 Java, Scala, C# | `/plugin install jvm-languages`               |
| **web-scripting**               | 웹 애플리케이션을 위한 PHP 및 Ruby        | `/plugin install web-scripting`               |
| **functional-programming**      | OTP 및 Phoenix를 포함한 Elixir              | `/plugin install functional-programming`      |
| **arm-cortex-microcontrollers** | ARM Cortex-M 펌웨어 및 드라이버        | `/plugin install arm-cortex-microcontrollers` |

### 블록체인 (1개 플러그인)

| 플러그인              | 설명                        | 설치                           |
| ------------------- | ---------------------------------- | --------------------------------- |
| **blockchain-web3** | 스마트 컨트랙트 및 DeFi 프로토콜 | `/plugin install blockchain-web3` |

### 금융 (1개 플러그인)

| 플러그인                   | 설명                             | 설치                                |
| ------------------------ | --------------------------------------- | -------------------------------------- |
| **quantitative-trading** | 알고리즘 트레이딩 및 위험 관리 | `/plugin install quantitative-trading` |

### 결제 (1개 플러그인)

| 플러그인                 | 설명                           | 설치                              |
| ---------------------- | ------------------------------------- | ------------------------------------ |
| **payment-processing** | Stripe/PayPal 통합 및 결제 | `/plugin install payment-processing` |

### 게임 (1개 플러그인)

| 플러그인               | 설명                            | 설치                            |
| -------------------- | -------------------------------------- | ---------------------------------- |
| **game-development** | Unity 및 Minecraft 플러그인 개발 | `/plugin install game-development` |

### 접근성 (1개 플러그인)

| 플러그인                       | 설명                        | 설치                                    |
| ---------------------------- | ---------------------------------- | ------------------------------------------ |
| **accessibility-compliance** | WCAG 감시 및 포용적 설계 | `/plugin install accessibility-compliance` |

## 플러그인 구조

각 플러그인에는 다음이 포함됩니다.

- **agents/** - 해당 도메인을 위한 특화된 에이전트
- **commands/** - 해당 플러그인 특화 도구 및 워크플로우
- **skills/** - 선택적 모듈식 지식 패키지(점진적 공개)

예시:

```
plugins/python-development/
-- agents/
|   -- python-pro.md
|   -- django-pro.md
|   -- fastapi-pro.md
-- commands/
|   -- python-scaffold.md
-- skills/
    -- async-python-patterns/
    -- python-testing-patterns/
    -- python-packaging/
    -- python-performance-optimization/
    -- uv-package-manager/
```

## 설치

### 단계 1: 마켓플레이스 추가

```bash
/plugin marketplace add wshobson/agents
```

이 명령으로 67개의 모든 플러그인을 사용할 수 있게 만들지만, **어떤 에이전트나 도구도 Claude의 컨텍스트에 로드되지 않습니다**.

### 단계 2: 특정 플러그인 설치

사용 가능한 플러그인 확인:

```bash
/plugin
```

필요한 플러그인만 설치하세요:

```bash
/plugin install python-development
/plugin install backend-development
```

각 설치된 플러그인은 **해당 플러그인의 에이전트와 명령어만** Claude의 컨텍스트에 로드합니다.

## 플러그인 설계 원칙

### 단일 책임

- 각 플러그인은 **한 가지를 잘합니다** (Unix 철학)
- 명확하고 집중화된 목적 (5-10단어로 표현 가능)
- 평균 플러그인 크기: **3.4개 컴포넌트** (Anthropic의 2-8 패턴 준수)

### 최소 토큰 사용

- 필요한 것만 설치하세요
- 각 플러그인은 자신의 특화 에이전트 및 도구만 로드합니다
- 불필요한 리소스를 컨텍스트에 로드하지 않습니다
- 세분화된 플러그인으로 더 나은 컨텍스트 효율성

### 조합성

- 복잡한 워크플로우를 위해 플러그인을 혼합 및 매칭하세요
- 워크플로우 오케스트레이터는 집중화된 플러그인을 조합합니다
- 플러그인 간의 명확한 경계
- 강제되는 기능 번들이 없습니다

## 관련 항목

- [에이전트 스킬](./agent-skills.md) - 플러그인 전체 107개의 특화 스킬
- [에이전트 레퍼런스](./agents.md) - 완전한 에이전트 카탈로그
- [사용 가이드](./usage.md) - 명령어 및 워크플로우
- [아키텍처](./architecture.md) - 설계 원칙
