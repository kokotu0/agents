# Agent 참고 자료

**100개의 전문화된 AI Agent**를 카테고리별로 정리한 완전한 참고 자료입니다.

## Agent 카테고리

### 아키텍처 및 시스템 설계

#### 핵심 아키텍처

| Agent                                                                                         | Model  | 설명                                                                  |
| --------------------------------------------------------------------------------------------- | ------ | --------------------------------------------------------------------- |
| [backend-architect](../plugins/backend-development/agents/backend-architect.md)               | opus   | RESTful API 설계, 마이크로서비스 경계 설정, 데이터베이스 스키마      |
| [frontend-developer](../plugins/multi-platform-apps/agents/frontend-developer.md)             | sonnet | React 컴포넌트, 반응형 레이아웃, 클라이언트 상태 관리               |
| [graphql-architect](../plugins/backend-development/agents/graphql-architect.md)               | opus   | GraphQL 스키마, resolver, federation 아키텍처                        |
| [architect-reviewer](../plugins/comprehensive-review/agents/architect-review.md)              | opus   | 아키텍처 일관성 분석 및 패턴 검증                                    |
| [cloud-architect](../plugins/cloud-infrastructure/agents/cloud-architect.md)                  | opus   | AWS/Azure/GCP 인프라 설계 및 비용 최적화                             |
| [hybrid-cloud-architect](../plugins/cloud-infrastructure/agents/hybrid-cloud-architect.md)    | opus   | 클라우드 및 온프레미스 환경 전반의 멀티클라우드 전략                |
| [kubernetes-architect](../plugins/kubernetes-operations/agents/kubernetes-architect.md)       | opus   | Kubernetes 및 GitOps를 활용한 클라우드 네이티브 인프라              |
| [service-mesh-expert](../plugins/cloud-infrastructure/agents/service-mesh-expert.md)          | opus   | Istio/Linkerd service mesh 아키텍처, mTLS 및 트래픽 관리            |
| [event-sourcing-architect](../plugins/backend-development/agents/event-sourcing-architect.md) | opus   | Event sourcing, CQRS 패턴, event store 및 saga 오케스트레이션      |
| [monorepo-architect](../plugins/developer-essentials/agents/monorepo-architect.md)            | opus   | Nx, Turborepo, Bazel을 활용한 Monorepo 도구 및 워크스페이스 최적화 |

#### UI/UX 및 모바일

| Agent                                                                                    | Model  | 설명                                                        |
| ---------------------------------------------------------------------------------------- | ------ | ----------------------------------------------------------- |
| [ui-designer](../plugins/ui-design/agents/ui-designer.md)                                | opus   | 모바일 및 웹용 UI/UX 디자인과 현대적 패턴                  |
| [accessibility-expert](../plugins/ui-design/agents/accessibility-expert.md)              | opus   | WCAG 준수, 접근성 감사, 포괄적 설계                        |
| [design-system-architect](../plugins/ui-design/agents/design-system-architect.md)        | opus   | 디자인 토큰, 컴포넌트 라이브러리, 테마 시스템             |
| [ui-ux-designer](../plugins/multi-platform-apps/agents/ui-ux-designer.md)                | sonnet | 인터페이스 설계, 와이어프레임, 디자인 시스템              |
| [ui-visual-validator](../plugins/accessibility-compliance/agents/ui-visual-validator.md) | sonnet | 시각적 회귀 테스트 및 UI 검증                             |
| [mobile-developer](../plugins/multi-platform-apps/agents/mobile-developer.md)            | sonnet | React Native 및 Flutter 애플리케이션 개발                 |
| [ios-developer](../plugins/multi-platform-apps/agents/ios-developer.md)                  | sonnet | Swift/SwiftUI를 활용한 네이티브 iOS 개발                  |
| [flutter-expert](../plugins/multi-platform-apps/agents/flutter-expert.md)                | sonnet | 상태 관리를 포함한 고급 Flutter 개발                      |

### 프로그래밍 언어

#### 시스템 및 저수준

| Agent                                                             | Model  | 설명                                                        |
| ----------------------------------------------------------------- | ------ | ----------------------------------------------------------- |
| [c-pro](../plugins/systems-programming/agents/c-pro.md)           | sonnet | 메모리 관리 및 OS 인터페이스를 이용한 시스템 프로그래밍   |
| [cpp-pro](../plugins/systems-programming/agents/cpp-pro.md)       | sonnet | RAII, 스마트 포인터, STL 알고리즘을 활용한 현대 C++      |
| [rust-pro](../plugins/systems-programming/agents/rust-pro.md)     | sonnet | 소유권 패턴을 활용한 메모리 안전 시스템 프로그래밍       |
| [golang-pro](../plugins/systems-programming/agents/golang-pro.md) | sonnet | goroutine 및 channel을 활용한 동시성 프로그래밍          |

#### 웹 및 애플리케이션

| Agent                                                                               | Model  | 설명                                                                   |
| ----------------------------------------------------------------------------------- | ------ | ---------------------------------------------------------------------- |
| [javascript-pro](../plugins/javascript-typescript/agents/javascript-pro.md)         | sonnet | ES6+, 비동기 패턴, Node.js를 활용한 현대 JavaScript                   |
| [typescript-pro](../plugins/javascript-typescript/agents/typescript-pro.md)         | sonnet | 타입 시스템 및 제네릭을 활용한 고급 TypeScript                        |
| [python-pro](../plugins/python-development/agents/python-pro.md)                    | sonnet | 고급 기능 및 최적화를 포함한 Python 개발                              |
| [temporal-python-pro](../plugins/backend-development/agents/temporal-python-pro.md) | sonnet | Temporal workflow 오케스트레이션, Python SDK, 지속 가능한 워크플로우  |
| [ruby-pro](../plugins/web-scripting/agents/ruby-pro.md)                             | sonnet | 메타프로그래밍, Rails 패턴, gem 개발을 포함한 Ruby                   |
| [php-pro](../plugins/web-scripting/agents/php-pro.md)                               | sonnet | 프레임워크 및 성능 최적화를 포함한 현대 PHP                          |

#### 엔터프라이즈 및 JVM

| Agent                                                       | Model  | 설명                                                      |
| ----------------------------------------------------------- | ------ | --------------------------------------------------------- |
| [java-pro](../plugins/jvm-languages/agents/java-pro.md)     | sonnet | Stream, 동시성, JVM 최적화를 포함한 현대 Java            |
| [scala-pro](../plugins/jvm-languages/agents/scala-pro.md)   | sonnet | 함수형 프로그래밍 및 분산 시스템을 포함한 엔터프라이즈 Scala |
| [csharp-pro](../plugins/jvm-languages/agents/csharp-pro.md) | sonnet | .NET 프레임워크 및 패턴을 포함한 C# 개발                 |

#### 특화된 플랫폼

| Agent                                                                              | Model  | 설명                                                                           |
| ---------------------------------------------------------------------------------- | ------ | ------------------------------------------------------------------------------ |
| [elixir-pro](../plugins/functional-programming/agents/elixir-pro.md)               | sonnet | OTP 패턴 및 Phoenix 프레임워크를 포함한 Elixir                                |
| [django-pro](../plugins/api-scaffolding/agents/django-pro.md)                      | sonnet | ORM 및 비동기 뷰를 포함한 Django 개발                                         |
| [fastapi-pro](../plugins/api-scaffolding/agents/fastapi-pro.md)                    | sonnet | 비동기 패턴 및 Pydantic을 포함한 FastAPI                                     |
| [haskell-pro](../plugins/functional-programming/agents/haskell-pro.md)             | sonnet | 순수성, 고급 타입 시스템, 동시성을 포함한 강타입 함수형 프로그래밍           |
| [unity-developer](../plugins/game-development/agents/unity-developer.md)           | sonnet | Unity 게임 개발 및 최적화                                                     |
| [minecraft-bukkit-pro](../plugins/game-development/agents/minecraft-bukkit-pro.md) | sonnet | Minecraft 서버 플러그인 개발                                                  |
| [sql-pro](../plugins/database-design/agents/sql-pro.md)                            | sonnet | 복잡한 SQL 쿼리 및 데이터베이스 최적화                                       |

### 인프라 및 운영

#### DevOps 및 배포

| Agent                                                                                  | Model  | 설명                                                        |
| -------------------------------------------------------------------------------------- | ------ | ----------------------------------------------------------- |
| [devops-troubleshooter](../plugins/incident-response/agents/devops-troubleshooter.md)  | sonnet | 프로덕션 디버깅, 로그 분석, 배포 문제 해결                |
| [deployment-engineer](../plugins/cloud-infrastructure/agents/deployment-engineer.md)   | sonnet | CI/CD 파이프라인, 컨테이너화, 클라우드 배포               |
| [terraform-specialist](../plugins/cloud-infrastructure/agents/terraform-specialist.md) | sonnet | Terraform 모듈 및 상태 관리를 포함한 Infrastructure as Code |
| [dx-optimizer](../plugins/team-collaboration/agents/dx-optimizer.md)                   | sonnet | 개발자 경험 최적화 및 도구 개선                            |

#### 데이터베이스 관리

| Agent                                                                                  | Model  | 설명                                                      |
| -------------------------------------------------------------------------------------- | ------ | --------------------------------------------------------- |
| [database-optimizer](../plugins/observability-monitoring/agents/database-optimizer.md) | sonnet | 쿼리 최적화, 인덱스 설계, 마이그레이션 전략              |
| [database-admin](../plugins/database-migrations/agents/database-admin.md)              | sonnet | 데이터베이스 운영, 백업, 복제, 모니터링                  |
| [database-architect](../plugins/database-design/agents/database-architect.md)          | opus   | 데이터베이스 설계, 기술 선택, 스키마 모델링             |

#### 인시던트 대응 및 네트워크

| Agent                                                                              | Model  | 설명                                             |
| ---------------------------------------------------------------------------------- | ------ | ------------------------------------------------ |
| [incident-responder](../plugins/incident-response/agents/incident-responder.md)    | opus   | 프로덕션 인시던트 관리 및 해결                   |
| [network-engineer](../plugins/observability-monitoring/agents/network-engineer.md) | sonnet | 네트워크 디버깅, 로드 밸런싱, 트래픽 분석      |

#### 프로젝트 관리

| Agent                                                             | Model | 설명                                                                           |
| ----------------------------------------------------------------- | ----- | ------------------------------------------------------------------------------ |
| [conductor-validator](../conductor/agents/conductor-validator.md) | opus  | Conductor 프로젝트 아티팩트의 완성도, 일관성, 정확성 검증                   |

### 품질 보증 및 보안

#### 코드 품질 및 리뷰

| Agent                                                                                            | Model | 설명                                                      |
| ------------------------------------------------------------------------------------------------ | ----- | --------------------------------------------------------- |
| [code-reviewer](../plugins/comprehensive-review/agents/code-reviewer.md)                         | opus  | 보안 중심 코드 리뷰 및 프로덕션 안정성 검증             |
| [security-auditor](../plugins/comprehensive-review/agents/security-auditor.md)                   | opus  | 취약점 평가 및 OWASP 준수                               |
| [backend-security-coder](../plugins/data-validation-suite/agents/backend-security-coder.md)      | opus  | 안전한 백엔드 코딩 관행 및 API 보안 구현               |
| [frontend-security-coder](../plugins/frontend-mobile-security/agents/frontend-security-coder.md) | opus  | XSS 방지, CSP 구현, 클라이언트 보안                     |
| [mobile-security-coder](../plugins/frontend-mobile-security/agents/mobile-security-coder.md)     | opus  | 모바일 보안 패턴, WebView 보안, 생체 인증              |
| [threat-modeling-expert](../plugins/security-scanning/agents/threat-modeling-expert.md)          | opus  | STRIDE 위협 모델링, 공격 트리, 보안 요구사항           |

#### 테스트 및 디버깅

| Agent                                                                         | Model  | 설명                                                   |
| ----------------------------------------------------------------------------- | ------ | ------------------------------------------------------ |
| [test-automator](../plugins/codebase-cleanup/agents/test-automator.md)        | sonnet | 포괄적인 테스트 스위트 생성 (단위, 통합, E2E)         |
| [tdd-orchestrator](../plugins/backend-development/agents/tdd-orchestrator.md) | sonnet | 테스트 주도 개발 방법론 가이드                         |
| [debugger](../plugins/error-debugging/agents/debugger.md)                     | sonnet | 에러 해결 및 테스트 실패 분석                         |
| [error-detective](../plugins/error-debugging/agents/error-detective.md)       | sonnet | 로그 분석 및 에러 패턴 인식                           |

#### 성능 및 관찰성

| Agent                                                                                          | Model | 설명                                                   |
| ---------------------------------------------------------------------------------------------- | ----- | ------------------------------------------------------ |
| [performance-engineer](../plugins/observability-monitoring/agents/performance-engineer.md)     | opus  | 애플리케이션 프로파일링 및 최적화                     |
| [observability-engineer](../plugins/observability-monitoring/agents/observability-engineer.md) | opus  | 프로덕션 모니터링, 분산 추적, SLI/SLO 관리           |
| [search-specialist](../plugins/content-marketing/agents/search-specialist.md)                  | haiku | 고급 웹 조사 및 정보 종합                             |

### 데이터 및 AI

#### 데이터 엔지니어링 및 분석

| Agent                                                                      | Model  | 설명                                                   |
| -------------------------------------------------------------------------- | ------ | ------------------------------------------------------ |
| [data-scientist](../plugins/machine-learning-ops/agents/data-scientist.md) | opus   | 데이터 분석, SQL 쿼리, BigQuery 운영                  |
| [data-engineer](../plugins/data-engineering/agents/data-engineer.md)       | sonnet | ETL 파이프라인, 데이터 웨어하우스, 스트리밍 아키텍처 |

#### 머신러닝 및 AI

| Agent                                                                                         | Model | 설명                                                                |
| --------------------------------------------------------------------------------------------- | ----- | ------------------------------------------------------------------- |
| [ai-engineer](../plugins/llm-application-dev/agents/ai-engineer.md)                           | opus  | LLM 애플리케이션, RAG 시스템, 프롬프트 파이프라인                 |
| [ml-engineer](../plugins/machine-learning-ops/agents/ml-engineer.md)                          | opus  | ML 파이프라인, 모델 제공, 특성 엔지니어링                         |
| [mlops-engineer](../plugins/machine-learning-ops/agents/mlops-engineer.md)                    | opus  | ML 인프라, 실험 추적, 모델 레지스트리                             |
| [prompt-engineer](../plugins/llm-application-dev/agents/prompt-engineer.md)                   | opus  | LLM 프롬프트 최적화 및 엔지니어링                                 |
| [vector-database-engineer](../plugins/llm-application-dev/agents/vector-database-engineer.md) | opus  | Vector 데이터베이스, embedding, 유사성 검색, 하이브리드 검색     |

### 문서화 및 기술 저술

| Agent                                                                                | Model  | 설명                                                            |
| ------------------------------------------------------------------------------------ | ------ | --------------------------------------------------------------- |
| [docs-architect](../plugins/code-documentation/agents/docs-architect.md)             | opus   | 포괄적인 기술 문서 생성                                        |
| [api-documenter](../plugins/api-testing-observability/agents/api-documenter.md)      | sonnet | OpenAPI/Swagger 명세 및 개발자 문서                            |
| [reference-builder](../plugins/documentation-generation/agents/reference-builder.md) | haiku  | 기술 참고 자료 및 API 문서                                     |
| [tutorial-engineer](../plugins/code-documentation/agents/tutorial-engineer.md)       | sonnet | 단계별 튜토리얼 및 교육 콘텐츠                                 |
| [mermaid-expert](../plugins/documentation-generation/agents/mermaid-expert.md)       | sonnet | 다이어그램 생성 (순서도, 시퀀스, ERD)                         |
| [c4-code](../plugins/c4-architecture/agents/c4-code.md)                              | haiku  | 함수 서명 및 의존성을 포함한 C4 코드 수준 문서                |
| [c4-component](../plugins/c4-architecture/agents/c4-component.md)                    | sonnet | C4 컴포넌트 수준 아키텍처 종합 및 문서화                      |
| [c4-container](../plugins/c4-architecture/agents/c4-container.md)                    | sonnet | API 문서를 포함한 C4 컨테이너 수준 아키텍처                   |
| [c4-context](../plugins/c4-architecture/agents/c4-context.md)                        | sonnet | 페르소나 및 사용자 여정을 포함한 C4 컨텍스트 수준 시스템 문서 |

### 비즈니스 및 운영

#### 비즈니스 분석 및 재무

| Agent                                                                        | Model  | 설명                                                   |
| ---------------------------------------------------------------------------- | ------ | ------------------------------------------------------ |
| [business-analyst](../plugins/business-analytics/agents/business-analyst.md) | sonnet | 메트릭 분석, 보고, KPI 추적                           |
| [quant-analyst](../plugins/quantitative-trading/agents/quant-analyst.md)     | opus   | 금융 모델링, 거래 전략, 시장 분석                    |
| [risk-manager](../plugins/quantitative-trading/agents/risk-manager.md)       | sonnet | 포트폴리오 위험 모니터링 및 관리                      |

#### 마케팅 및 영업

| Agent                                                                             | Model  | 설명                                          |
| --------------------------------------------------------------------------------- | ------ | --------------------------------------------- |
| [content-marketer](../plugins/content-marketing/agents/content-marketer.md)       | sonnet | 블로그 포스트, 소셜 미디어, 이메일 캠페인   |
| [sales-automator](../plugins/customer-sales-automation/agents/sales-automator.md) | haiku  | 콜드 이메일, 후속 조치, 제안서 생성         |

#### 지원 및 법무

| Agent                                                                               | Model  | 설명                                                |
| ----------------------------------------------------------------------------------- | ------ | --------------------------------------------------- |
| [customer-support](../plugins/customer-sales-automation/agents/customer-support.md) | sonnet | 지원 티켓, FAQ 응답, 고객 커뮤니케이션           |
| [hr-pro](../plugins/hr-legal-compliance/agents/hr-pro.md)                           | opus   | HR 운영, 정책, 직원 관계                          |
| [legal-advisor](../plugins/hr-legal-compliance/agents/legal-advisor.md)             | opus   | 개인정보 보호 정책, 서비스 약관, 법률 문서       |

### SEO 및 콘텐츠 최적화

| Agent                                                                                                     | Model  | 설명                                             |
| --------------------------------------------------------------------------------------------------------- | ------ | ------------------------------------------------ |
| [seo-content-auditor](../plugins/seo-content-creation/agents/seo-content-auditor.md)                      | sonnet | 콘텐츠 품질 분석, E-E-A-T 신호 평가             |
| [seo-meta-optimizer](../plugins/seo-technical-optimization/agents/seo-meta-optimizer.md)                  | haiku  | 메타 제목 및 설명 최적화                        |
| [seo-keyword-strategist](../plugins/seo-technical-optimization/agents/seo-keyword-strategist.md)          | haiku  | 키워드 분석 및 의미적 변형                      |
| [seo-structure-architect](../plugins/seo-technical-optimization/agents/seo-structure-architect.md)        | haiku  | 콘텐츠 구조 및 schema markup                    |
| [seo-snippet-hunter](../plugins/seo-technical-optimization/agents/seo-snippet-hunter.md)                  | haiku  | 특별 스니펫 포맷팅                              |
| [seo-content-refresher](../plugins/seo-analysis-monitoring/agents/seo-content-refresher.md)               | haiku  | 콘텐츠 신선도 분석                              |
| [seo-cannibalization-detector](../plugins/seo-analysis-monitoring/agents/seo-cannibalization-detector.md) | haiku  | 키워드 중복 탐지                                |
| [seo-authority-builder](../plugins/seo-analysis-monitoring/agents/seo-authority-builder.md)               | sonnet | E-E-A-T 신호 분석                               |
| [seo-content-writer](../plugins/seo-content-creation/agents/seo-content-writer.md)                        | sonnet | SEO 최적화 콘텐츠 생성                          |
| [seo-content-planner](../plugins/seo-content-creation/agents/seo-content-planner.md)                      | haiku  | 콘텐츠 계획 및 토픽 클러스터                    |

### 특화 도메인

| Agent                                                                                   | Model  | 설명                                                   |
| --------------------------------------------------------------------------------------- | ------ | ------------------------------------------------------ |
| [arm-cortex-expert](../plugins/arm-cortex-microcontrollers/agents/arm-cortex-expert.md) | sonnet | ARM Cortex-M 펌웨어 및 주변 장치 드라이버 개발       |
| [blockchain-developer](../plugins/blockchain-web3/agents/blockchain-developer.md)       | sonnet | Web3 앱, 스마트 계약, DeFi 프로토콜                  |
| [payment-integration](../plugins/payment-processing/agents/payment-integration.md)      | sonnet | 결제 프로세서 통합 (Stripe, PayPal)                  |
| [legacy-modernizer](../plugins/framework-migration/agents/legacy-modernizer.md)         | sonnet | 레거시 코드 리팩토링 및 현대화                       |
| [context-manager](../plugins/agent-orchestration/agents/context-manager.md)             | haiku  | 다중 Agent 컨텍스트 관리                            |

## 모델 구성

Agent는 작업 복잡도와 계산 요구사항에 따라 특정 Claude 모델에 할당됩니다.

### 모델 배포 요약

| Model  | Agent 수 | 사용 사례                                                    |
| ------ | -------- | ----------------------------------------------------------- |
| Opus   | 42       | 중요 아키텍처, 보안, 코드 리뷰, 프로덕션 코딩             |
| Sonnet | 39       | 복잡한 작업, 지능형 지원                                   |
| Haiku  | 18       | 빠른 운영 작업                                             |

### 모델 선택 기준

#### Haiku - 빠른 실행 및 결정적 작업

**사용 시기:**

- 잘 정의된 명세에서 코드 생성
- 확립된 패턴을 따르는 테스트 작성
- 명확한 템플릿을 포함한 문서 작성
- 인프라 운영 실행
- 데이터베이스 쿼리 최적화 수행
- 고객 지원 응답 처리
- SEO 최적화 작업 수행
- 배포 파이프라인 관리

#### Sonnet - 복잡한 추론 및 아키텍처

**사용 시기:**

- 시스템 아키텍처 설계
- 기술 선택 의사결정
- 보안 감사 수행
- 아키텍처 패턴 코드 리뷰
- 복잡한 AI/ML 파이프라인 생성
- 언어별 전문성 제공
- 다중 Agent 워크플로우 오케스트레이션
- 중요 비즈니스 법무/HR 사항 처리

### 하이브리드 오케스트레이션 패턴

플러그인 에코시스템은 최적의 성능과 비용 효율을 위해 Sonnet + Haiku 오케스트레이션을 활용합니다.

#### 패턴 1: 계획 -> 실행

```
Sonnet: backend-architect (API 아키텍처 설계)
  |
Haiku: 명세에 따라 API 엔드포인트 생성
  |
Haiku: test-automator (포괄적인 테스트 생성)
  |
Sonnet: code-reviewer (아키텍처 리뷰)
```

#### 패턴 2: 추론 -> 행동 (인시던트 대응)

```
Sonnet: incident-responder (이슈 진단, 전략 수립)
  |
Haiku: devops-troubleshooter (수정 사항 실행)
  |
Haiku: deployment-engineer (긴급 패치 배포)
  |
Haiku: 모니터링 알림 구현
```

#### 패턴 3: 복잡 -> 단순 (데이터베이스 설계)

```
Sonnet: database-architect (스키마 설계, 기술 선택)
  |
Haiku: sql-pro (마이그레이션 스크립트 생성)
  |
Haiku: database-admin (마이그레이션 실행)
  |
Haiku: database-optimizer (쿼리 성능 최적화)
```

#### 패턴 4: 다중 Agent 워크플로우

```
풀스택 기능 개발:
Sonnet: backend-architect + frontend-developer (컴포넌트 설계)
  |
Haiku: 설계에 따라 코드 생성
  |
Haiku: test-automator (단위 + 통합 테스트)
  |
Sonnet: security-auditor (보안 리뷰)
  |
Haiku: deployment-engineer (CI/CD 설정)
  |
Haiku: 관찰성 스택 설정
```

## Agent 호출

### 자연어

어떤 전문가를 사용해야 할지 추론해야 할 때 자연어를 통해 Agent를 호출할 수 있습니다.

```
"backend-architect를 사용하여 인증 API 설계"
"security-auditor를 통해 OWASP 취약점 스캔"
"performance-engineer에게 이 데이터베이스 쿼리 최적화"
```

### 슬래시 명령어

많은 Agent는 직접 호출을 위한 플러그인 슬래시 명령어를 통해 접근 가능합니다.

```bash
/backend-development:feature-development user authentication
/security-scanning:security-sast
/incident-response:smart-fix "memory leak in payment service"
```

## 기여

새로운 Agent를 추가하려면:

1. `plugins/{plugin-name}/agents/{agent-name}.md` 생성
2. 이름, 설명, 모델 할당을 포함한 frontmatter 추가
3. 포괄적인 시스템 프롬프트 작성
4. `.claude-plugin/marketplace.json`의 플러그인 정의 업데이트

자세한 내용은 [기여 가이드](../CONTRIBUTING.md)를 참고하십시오.
