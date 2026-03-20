# Agent Skills

Agent Skills는 Anthropic의 [Agent Skills Specification](https://github.com/anthropics/skills/blob/main/agent_skills_spec.md)에 따른 모듈식 패키지로, Claude의 기능을 전문 도메인 지식으로 확장합니다. 이 플러그인 생태계는 27개의 플러그인에 걸쳐 **129개의 전문화된 스킬**을 포함하고 있으며, 점진적 공개 및 효율적인 토큰 사용을 가능하게 합니다.

## 개요

스킬은 Claude에 특정 도메인의 깊이 있는 전문성을 제공하며, 처음부터 모든 내용을 컨텍스트에 로드할 필요가 없습니다. 각 스킬은 다음을 포함합니다:

- **YAML Frontmatter**: 이름 및 활성화 기준
- **점진적 공개**: 메타데이터 → 지침 → 리소스
- **활성화 트리거**: 자동 호출을 위한 명확한 "Use when" 절

## 플러그인별 스킬

### Kubernetes 운영 (4개 스킬)

| 스킬                      | 설명                                                                                                              |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| **k8s-manifest-generator** | Deployment, Service, ConfigMap, Secret에 대한 프로덕션 레디 Kubernetes manifest 생성 및 모범 사례 준수 |
| **helm-chart-scaffolding** | Kubernetes 애플리케이션 템플릿팅 및 패키징을 위한 Helm Chart 설계, 조직화 및 관리 |
| **gitops-workflow**        | ArgoCD 및 Flux를 사용한 GitOps 워크플로우 구현으로 자동화된 선언형 배포 실현 |
| **k8s-security-policies**  | NetworkPolicy, PodSecurityPolicy, RBAC를 포함한 Kubernetes 보안 정책 구현 |

### LLM 애플리케이션 개발 (8개 스킬)

| 스킬                            | 설명                                                                                 |
| -------------------------------- | ------------------------------------------------------------------------------------------- |
| **langchain-architecture**       | LangChain 프레임워크를 사용한 LLM 애플리케이션 설계 (agent, memory, tool 통합 포함) |
| **prompt-engineering-patterns**  | LLM 성능 및 신뢰성을 위한 고급 프롬프트 엔지니어링 기법 습득 |
| **rag-implementation**           | Vector database 및 semantic search를 통한 Retrieval-Augmented Generation 시스템 구축 |
| **llm-evaluation**               | 자동화된 메트릭 및 벤치마킹을 통한 포괄적인 평가 전략 구현 |
| **embedding-strategies**         | 최적 청킹을 통한 텍스트, 이미지, 멀티모달 콘텐츠의 embedding pipeline 설계 |
| **similarity-search-patterns**   | ANN 알고리즘 및 거리 메트릭을 사용한 효율적인 유사도 검색 구현 |
| **vector-index-tuning**          | HNSW, IVF 및 하이브리드 구성을 통한 vector index 성능 최적화 |
| **hybrid-search-implementation** | 향상된 검색 정확도를 위한 vector 및 keyword search 결합 |

### 백엔드 개발 (9개 스킬)

| 스킬                               | 설명                                                                                           |
| ----------------------------------- | ----------------------------------------------------------------------------------------------------- |
| **api-design-principles**           | 직관적이고 확장 가능하며 유지보수하기 쉬운 REST 및 GraphQL API 설계 습득 |
| **architecture-patterns**           | Clean Architecture, Hexagonal Architecture, Domain-Driven Design 구현 |
| **microservices-patterns**          | 서비스 경계, 이벤트 기반 통신, 복원력 있는 마이크로서비스 설계 |
| **workflow-orchestration-patterns** | 분산 시스템, saga 패턴, 상태 관리를 위한 Temporal을 사용한 지속적 워크플로우 설계 |
| **temporal-python-testing**         | pytest, time-skipping, mocking 전략을 통한 Temporal 워크플로우 포괄적 커버리지 테스트 |
| **event-store-design**              | 최적화된 schema, snapshot, stream partitioning을 통한 event store 설계 |
| **cqrs-implementation**             | 별도의 읽기/쓰기 모델 및 eventual consistency 패턴을 통한 CQRS 구현 |
| **projection-patterns**             | event stream에서 읽기 최적화 view를 위한 효율적인 projection 구축 |
| **saga-orchestration**              | 보상 로직 및 실패 처리를 포함한 분산 saga 설계 |

### 개발자 필수 요소 (11개 스킬)

| 스킬                            | 설명                                                                                     |
| -------------------------------- | ----------------------------------------------------------------------------------------------- |
| **git-advanced-workflows**       | rebase, cherry-pick, bisect, worktree, reflog를 포함한 고급 Git 워크플로우 습득 |
| **sql-optimization-patterns**    | SQL 쿼리, 인덱싱 전략, EXPLAIN 분석을 통한 데이터베이스 성능 최적화 |
| **error-handling-patterns**      | exception, Result type, graceful degradation을 통한 견고한 에러 처리 구현 |
| **code-review-excellence**       | 건설적인 피드백 및 체계적 분석을 통한 효과적인 코드 리뷰 제공 |
| **e2e-testing-patterns**         | 중요 사용자 워크플로우를 위한 Playwright 및 Cypress를 사용한 신뢰성 있는 E2E 테스트 수트 구축 |
| **auth-implementation-patterns** | JWT, OAuth2, session, RBAC를 사용한 인증 및 권한 부여 구현 |
| **debugging-strategies**         | 체계적인 디버깅 기법, 프로파일링 도구, 근본 원인 분석 습득 |
| **monorepo-management**          | 확장 가능한 다중 패키지 프로젝트를 위한 Turborepo, Nx, pnpm workspace를 사용한 monorepo 관리 |
| **nx-workspace-patterns**        | 계산 캐싱 및 영향받는 명령어를 통한 Nx workspace 구성 |
| **turborepo-caching**            | 원격 캐싱 및 파이프라인 구성을 통한 Turborepo 빌드 최적화 |
| **bazel-build-optimization**     | hermetic action 및 원격 실행을 통한 Bazel 빌드 설계 |

### Blockchain 및 Web3 (4개 스킬)

| 스킬                       | 설명                                                                             |
| --------------------------- | --------------------------------------------------------------------------------------- |
| **defi-protocol-templates** | staking, AMM, governance, lending에 대한 템플릿을 사용한 DeFi 프로토콜 구현 |
| **nft-standards**           | 메타데이터 및 마켓플레이스 통합을 포함한 NFT 표준 (ERC-721, ERC-1155) 구현 |
| **solidity-security**       | 취약점 방지 및 보안 패턴 구현을 위한 스마트 컨트랙트 보안 습득 |
| **web3-testing**            | Hardhat 및 Foundry를 사용한 단위 테스트 및 mainnet forking을 통한 스마트 컨트랙트 테스트 |

### CI/CD 자동화 (4개 스킬)

| 스킬                          | 설명                                                                               |
| ------------------------------ | ----------------------------------------------------------------------------------------- |
| **deployment-pipeline-design** | 승인 게이트 및 보안 검사를 포함한 다단계 CI/CD 파이프라인 설계 |
| **github-actions-templates**   | 테스트, 빌드, 배포를 위한 프로덕션 레디 GitHub Actions 워크플로우 생성 |
| **gitlab-ci-patterns**         | 다단계 워크플로우 및 분산 runner를 포함한 GitLab CI/CD 파이프라인 구축 |
| **secrets-management**         | Vault, AWS Secrets Manager 또는 네이티브 솔루션을 사용한 보안 비밀 관리 구현 |

### 클라우드 인프라 (8개 스킬)

| 스킬                          | 설명                                                                               |
| ------------------------------ | ------------------------------------------------------------------------- |
| **terraform-module-library**   | AWS, Azure, GCP 인프라를 위한 재사용 가능한 Terraform 모듈 구축 |
| **multi-cloud-architecture**   | 벤더 종속성을 피하는 멀티클라우드 아키텍처 설계 |
| **hybrid-cloud-networking**    | 온프레미스 및 클라우드 플랫폼 간의 보안 연결성 구성 |
| **cost-optimization**          | 우측 크기 조정, 태깅, 예약 인스턴스를 통한 클라우드 비용 최적화 |
| **istio-traffic-management**   | Istio 트래픽 라우팅, 로드 밸런싱, canary 배포 구성 |
| **linkerd-patterns**           | 자동 mTLS 및 트래픽 분할을 통한 Linkerd service mesh 구현 |
| **mtls-configuration**         | 인증서 관리를 통한 영(zero)-trust mTLS 아키텍처 설계 |
| **service-mesh-observability** | 분산 트래싱 및 메트릭을 통한 포괄적 가시성 구축 |

### 프레임워크 마이그레이션 (4개 스킬)

| 스킬                   | 설명                                                                   |
| ----------------------- | ----------------------------------------------------------------------------- |
| **react-modernization** | React 앱 업그레이드, hook 마이그레이션, concurrent 기능 채택 |
| **angular-migration**   | hybrid mode 및 증분 재작성을 사용한 AngularJS에서 Angular로 마이그레이션 |
| **database-migration**  | zero-downtime 전략 및 데이터 변환을 통한 데이터베이스 마이그레이션 실행 |
| **dependency-upgrade**  | 호환성 분석 및 테스트를 통한 주요 종속성 업그레이드 관리 |

### 관찰성 및 모니터링 (4개 스킬)

| 스킬                        | 설명                                                             |
| ---------------------------- | ----------------------------------------------------------------------- |
| **prometheus-configuration** | 포괄적 메트릭 수집 및 모니터링을 위한 Prometheus 설정 |
| **grafana-dashboards**       | 실시간 시스템 시각화를 위한 프로덕션 Grafana 대시보드 생성 |
| **distributed-tracing**      | 요청 추적을 위한 Jaeger 및 Tempo를 사용한 분산 트래싱 구현 |
| **slo-implementation**        | 에러 예산 및 경보를 포함한 SLI 및 SLO 정의 |

### 결제 처리 (4개 스킬)

| 스킬                  | 설명                                                                   |
| ---------------------- | ----------------------------------------------------------------------------- |
| **stripe-integration** | 체크아웃, 구독, webhook에 대한 Stripe 결제 처리 구현 |
| **paypal-integration** | express checkout 및 구독을 포함한 PayPal 결제 처리 통합 |
| **pci-compliance**     | 안전한 결제 카드 데이터 처리를 위한 PCI DSS 준수 구현 |
| **billing-automation** | 반복 청구 및 인보이싱을 위한 자동화된 청구 시스템 구축 |

### Python 개발 (5개 스킬)

| 스킬                               | 설명                                                                           |
| ----------------------------------- | ------------------------------------------------------------------------------------- |
| **async-python-patterns**           | Python asyncio, 동시 프로그래밍, async/await 패턴 습득 |
| **python-testing-patterns**         | pytest, fixture, mocking을 통한 포괄적 테스트 구현 |
| **python-packaging**                | 적절한 구조 및 PyPI 퍼블리싱을 통한 배포 가능한 Python 패키지 생성 |
| **python-performance-optimization** | cProfile 및 성능 모범 사례를 사용한 Python 코드 프로파일링 및 최적화 |
| **uv-package-manager**              | 빠른 종속성 관리 및 가상 환경을 위한 uv package manager 습득 |

### JavaScript/TypeScript (4개 스킬)

| 스킬                           | 설명                                                                           |
| ------------------------------- | ------------------------------------------------------------------------------------- |
| **typescript-advanced-types**   | generics 및 conditional type을 포함한 TypeScript 고급 타입 시스템 습득 |
| **nodejs-backend-patterns**     | Express/Fastify 및 모범 사례를 사용한 프로덕션 레디 Node.js 서비스 구축 |
| **javascript-testing-patterns** | Jest, Vitest, Testing Library를 사용한 포괄적 테스트 구현 |
| **modern-javascript-patterns**  | async/await, destructuring, 함수형 프로그래밍을 포함한 ES6+ 기능 습득 |

### API Scaffolding (1개 스킬)

| 스킬                 | 설명                                                                     |
| --------------------- | ------------------------------------------------------------------------------- |
| **fastapi-templates** | async 패턴 및 에러 처리를 포함한 프로덕션 레디 FastAPI 프로젝트 생성 |

### Machine Learning Operations (1개 스킬)

| 스킬                    | 설명                                                               |
| ------------------------ | ------------------------------------------------------------------------- |
| **ml-pipeline-workflow** | 데이터 준비에서 배포까지의 엔드-투-엔드 MLOps 파이프라인 구축 |

### 보안 스캐닝 (5개 스킬)

| 스킬                               | 설명                                                                     |
| ----------------------------------- | ------------------------------------------------------------------------------- |
| **sast-configuration**              | 취약점 감지를 위한 Static Application Security Testing 도구 구성 |
| **stride-analysis-patterns**        | spoofing, tampering 등의 위협을 식별하기 위해 STRIDE 방법론 적용 |
| **attack-tree-construction**        | 위협 시나리오를 취약점에 매핑하는 attack tree 구축 |
| **security-requirement-extraction** | 수용 기준을 포함한 위협 모델에서 보안 요구사항 도출 |
| **threat-mitigation-mapping**       | 우선순위가 지정된 재해결 계획을 통한 위협을 완화 매핑 |

### 접근성 준수 (2개 스킬)

| 스킬                     | 설명                                                             |
| ------------------------- | ----------------------------------------------------------------------- |
| **wcag-audit-patterns**   | 자동화된 및 수동 테스트를 통한 WCAG 2.2 접근성 감사 실시 |
| **screen-reader-testing** | NVDA, JAWS, VoiceOver에서의 screen reader 호환성 테스트 |

### 비즈니스 분석 (2개 스킬)

| 스킬                    | 설명                                                                  |
| ------------------------ | ---------------------------------------------------------------------------- |
| **kpi-dashboard-design** | 실행 가능한 KPI 및 드릴다운 기능을 포함한 executive 대시보드 설계 |
| **data-storytelling**    | 이해 관계자를 위한 데이터 인사이트를 설득력 있는 내러티브로 변환 |

### 데이터 엔지니어링 (4개 스킬)

| 스킬                           | 설명                                                                 |
| ------------------------------- | --------------------------------------------------------------------------- |
| **spark-optimization**          | 분할, 캐싱, broadcast join을 통한 Apache Spark 작업 최적화 |
| **dbt-transformation-patterns** | 증분 전략 및 테스트를 포함한 dbt 모델 구축 |
| **airflow-dag-patterns**        | 적절한 종속성 및 에러 처리를 포함한 Airflow DAG 설계 |
| **data-quality-frameworks**     | Great Expectations 및 사용자정의 validator를 통한 데이터 품질 검사 구현 |

### 문서 생성 (3개 스킬)

| 스킬                             | 설명                                                         |
| --------------------------------- | ------------------------------------------------------------------- |
| **openapi-spec-generation**       | 완전한 schema와 함께 코드에서 OpenAPI 3.1 사양 생성 |
| **changelog-automation**          | conventional commit에서 변경 로그 자동 생성 |
| **architecture-decision-records** | 아키텍처 결정 및 트레이드오프를 문서화하는 ADR 작성 |

### Frontend 모바일 개발 (4개 스킬)

| 스킬                          | 설명                                                     |
| ------------------------------ | --------------------------------------------------------------- |
| **react-state-management**     | Zustand, Jotai, React Query를 사용한 상태 관리 구현 |
| **nextjs-app-router-patterns** | App Router, RSC, streaming을 사용한 Next.js 14+ 앱 구축 |
| **tailwind-design-system**     | Tailwind CSS 및 component library를 사용한 design system 생성 |
| **react-native-architecture**  | navigation 및 native module를 포함한 React Native 앱 아키텍처 |

### UI 설계 (9개 스킬)

| 스킬                         | 설명                                                         |
| ----------------------------- | ------------------------------------------------------------------- |
| **design-system-patterns**    | token, component, theming을 포함한 확장 가능한 design system 구축 |
| **accessibility-compliance**  | 적절한 ARIA 및 keyboard navigation을 통한 WCAG 2.1/2.2 준수 구현 |
| **responsive-design**         | CSS Grid, Flexbox, container query를 사용한 유동적 레이아웃 생성 |
| **mobile-ios-design**         | Human Interface Guidelines를 따른 iOS 앱 설계 |
| **mobile-android-design**     | Material Design 3 가이드라인을 따른 Android 앱 설계 |
| **react-native-design**       | React Native 애플리케이션을 위한 크로스 플랫폼 설계 패턴 |
| **web-component-design**      | Shadow DOM을 포함한 접근 가능하고 재사용 가능한 web component 구축 |
| **interaction-design**        | micro-interaction, animation, gesture 기반 인터페이스 생성 |
| **visual-design-foundations** | 타이포그래피, 색 이론, 공백, visual hierarchy 적용 |

### 게임 개발 (2개 스킬)

| 스킬                       | 설명                                                          |
| --------------------------- | -------------------------------------------------------------------- |
| **unity-ecs-patterns**      | 고성능 게임 시스템을 위한 Unity ECS 구현 |
| **godot-gdscript-patterns** | GDScript 모범 사례 및 scene composition을 통한 Godot 게임 구축 |

### HR 법률 준수 (2개 스킬)

| 스킬                             | 설명                                                      |
| --------------------------------- | ---------------------------------------------------------------- |
| **gdpr-data-handling**            | 동의 관리를 포함한 GDPR 준수 데이터 처리 구현 |
| **employment-contract-templates** | 관할권 특정 조항을 포함한 고용 계약 생성 |

### Incident 대응 (3개 스킬)

| 스킬                          | 설명                                                           |
| ------------------------------ | --------------------------------------------------------------------- |
| **postmortem-writing**         | 근본 원인 분석 및 조치 항목을 포함한 비난 없는 postmortem 작성 |
| **incident-runbook-templates** | 에스컬레이션 경로를 포함한 일반적인 incident 시나리오용 runbook 생성 |
| **on-call-handoff-patterns**   | 컨텍스트 보존 및 경보 라우팅을 포함한 on-call handoff 설계 |

### 정량화 거래 (2개 스킬)

| 스킬                        | 설명                                                             |
| ---------------------------- | ----------------------------------------------------------------------- |
| **backtesting-frameworks**   | 현실적인 slippage 및 거래 비용을 통한 backtesting 시스템 구축 |
| **risk-metrics-calculation** | 포트폴리오를 위한 VaR, Sharpe ratio, drawdown 메트릭 계산 |

### 시스템 프로그래밍 (3개 스킬)

| 스킬                       | 설명                                                                 |
| --------------------------- | --------------------------------------------------------------------------- |
| **rust-async-patterns**     | Tokio, futures, 적절한 에러 처리를 통한 async Rust 구현 |
| **go-concurrency-patterns** | channel, worker pool, context cancellation을 사용한 Go 동시성 설계 |
| **memory-safety-patterns**  | ownership, bounds checking, sanitizer를 사용한 메모리 안전 코드 작성 |

### Conductor - 프로젝트 관리 (3개 스킬)

| 스킬                          | 설명                                                                                             |
| ------------------------------ | ------------------------------------------------------------------------------------------------------- |
| **context-driven-development** | product context, specification, phased planning을 포함한 Context-Driven Development 방법론 적용 |
| **track-management**           | spec 및 구현 계획을 포함한 feature, bug, chore, refactor에 대한 development track 관리 |
| **workflow-patterns**          | 체계적 개발을 위한 TDD 워크플로우, commit 전략, verification checkpoint 구현 |

## 스킬의 작동 방식

### 활성화

스킬은 Claude가 요청에서 일치하는 패턴을 감지할 때 자동으로 활성화됩니다:

```
사용자: "Helm chart를 사용한 Kubernetes 배포 설정"
-> 활성화: helm-chart-scaffolding, k8s-manifest-generator

사용자: "문서 Q&A를 위한 RAG 시스템 구축"
-> 활성화: rag-implementation, prompt-engineering-patterns

사용자: "Python async 성능 최적화"
-> 활성화: async-python-patterns, python-performance-optimization
```

### 점진적 공개

스킬은 토큰 효율성을 위한 3계층 아키텍처를 사용합니다:

1. **메타데이터** (Frontmatter): 이름 및 활성화 기준 (항상 로드)
2. **지침**: 핵심 가이드 및 패턴 (활성화될 때 로드)
3. **리소스**: 예제 및 템플릿 (필요 시 로드)

### Agent와의 통합

스킬은 agent와 함께 작동하여 깊이 있는 도메인 전문성을 제공합니다:

- **Agent**: 높은 수준의 추론 및 조율
- **스킬**: 전문화된 지식 및 구현 패턴

예시 워크플로우:

```
backend-architect agent -> API 아키텍처 계획
  |
api-design-principles skill -> REST/GraphQL 모범 사례 제공
  |
fastapi-templates skill -> 프로덕션 레디 템플릿 제공
```

## 사양 준수

모든 107개의 스킬은 [Agent Skills Specification](https://github.com/anthropics/skills/blob/main/agent_skills_spec.md)을 따릅니다:

- 필수 `name` 필드 (hyphen-case)
- 필수 `description` 필드 ("Use when" 절 포함)
- 1024자 이하의 설명
- 완전하고 잘린 부분이 없는 설명
- 적절한 YAML frontmatter 형식

## 새 스킬 생성

플러그인에 스킬을 추가하려면:

1. `plugins/{plugin-name}/skills/{skill-name}/SKILL.md` 생성
2. YAML frontmatter 추가:
   ```yaml
   ---
   name: skill-name
   description: 스킬이 하는 일. Use when [활성화 트리거].
   ---
   ```
3. 점진적 공개를 사용하여 포괄적인 스킬 콘텐츠 작성
4. `marketplace.json`에 스킬 경로 추가:
   ```json
   {
     "name": "plugin-name",
     "skills": ["./skills/skill-name"]
   }
   ```

### 스킬 구조

```
plugins/{plugin-name}/
-- skills/
    -- {skill-name}/
        -- SKILL.md        # Frontmatter + 콘텐츠
```

## 이점

- **토큰 효율성**: 필요할 때만 관련 지식 로드
- **전문화된 전문성**: bloat 없는 깊이 있는 도메인 지식
- **명확한 활성화**: 명시적 트리거로 원치 않는 호출 방지
- **조합 가능성**: 워크플로우 전체에서 스킬 혼합 및 매칭
- **유지보수성**: 격리된 업데이트로 다른 스킬에 영향 없음

## 리소스

- [Anthropic Skills Repository](https://github.com/anthropics/skills)
- [Agent Skills Documentation](https://docs.claude.com/en/docs/claude-code/skills)
