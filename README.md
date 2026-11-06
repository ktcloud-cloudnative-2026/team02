# 5xx — 피크오더(Peak Order)

음식점의 피크 시간대에 몰리는 주문을 안정적으로 처리하고, 고객에게 주문 진행 상황과 예상 대기 시간을 실시간으로 보여 주는 주문 서비스입니다.

Notion 자료에서는 **음식 주문 및 조리 대기 시뮬레이션 웹 서비스**로 설명합니다. 모의 결제를 사용하며, 배포 자동화·모니터링·로깅과 주문·재고 정합성 검증을 목표로 합니다. 구현·검증 완료를 의미하지 않습니다.

> 문서 상태: **Notion 자료를 정리한 1단계 초안 · 팀 전체 승인 필요**
> 기획·설계 문서, 코드, 배포 파일, 결정 기록을 이 저장소에 정리합니다. 최종 합의본으로 전환하기 전에는 원문과 미결정 목록을 함께 확인합니다.
> 현재 제공 자료만으로 팀 최종 승인이 확인된 항목은 없습니다. 서비스 수(3·5·6개), 로그인·관리자 범위와 기술 스택을 임의로 확정하지 않습니다.

## 문서 목차

| 문서 | 내용·현재 상태 |
|---|---|
| [프로젝트 기획서](docs/plan.md) | 문제·사용자·범위·성공 목표. 범위 충돌 및 승인 필요 |
| [요구사항](docs/requirements.md) | US-01~20·SR-01~06·S1~S4. US-14~20은 팀원 승인 필요 |
| [시스템 아키텍처](docs/architecture.md) | 원문의 5개 서비스 안. 최종 구성 미결정 |
| [기술 스택](docs/tech-stack.md) | React·Spring Boot·PostgreSQL 등을 포함한 기술 초안 |
| [미결정 사항과 문서 충돌](docs/pending-decisions.md) | 원문 간 차이, 승인 필요 항목, 확인 질문과 출처 |
| [설계 결정 기록 양식](docs/adr/0001-template.md) | 기존 양식 유지. 이번 단계에서 개별 ADR을 만들지 않음 |
| [API 문서](docs/api/README.md) · [ERD 문서](docs/erd/README.md) | 기존 템플릿 유지. 상세 명세 확정·작성 완료를 의미하지 않음 |
| [역할 분담](docs/roles.md) · [팀 운영](docs/team.md) | 기존 템플릿 유지. Notion 팀 정보 반영은 이번 단계 범위 밖 |
| [관측 설계](docs/observability.md) · [런북](docs/runbook.md) | 기존 템플릿 유지. 상세 관측·장애 대응 절차는 후속 검토 |
| [공통 규칙](docs/conventions.md) · [GitHub 사용 가이드](docs/github-guide.md) | 기존 가이드 유지. 팀 규칙과의 대조 필요 |

## 상태를 읽는 방법

- **확정**: 팀 승인 근거가 확인된 항목. 이번 자료만으로 최종 확정한 항목은 없습니다.
- **제안**: 원문에 제시된 후보·목표·설계안으로, 승인된 선택이 아닙니다.
- **미결정**: 값·방식이 정해지지 않았거나 문서가 충돌해 선택할 수 없습니다.
- **승인 필요**: 팀 검토·합의가 필요한 항목. 특히 US-14~20은 원문에 명시되어 있습니다.

여러 문서에 같은 내용이 있어도 최종 승인 증거로 간주하지 않습니다. 문서 승인과 구현·테스트 완료도 별개입니다.

## 원본 자료와 외부 링크

- 원본 Notion 문서: [피크오더(Peak Order)](https://puzzling-woolen-3e9.notion.site/Peak-Order-35f2f07e947883f88d530131eb2b8f0b?source=copy_link)
- 기존 README의 Notion 링크: [Peak Order](https://app.notion.com/p/Peak-Order-35f2f07e947883f88d530131eb2b8f0b?source=copy_link)
- 기존 시퀀스 다이어그램 링크: [FigJam](https://www.figma.com/board/PfXHpZdcoHplNNKP6ZPcx1/kt-cloud-team2?node-id=0-1&t=N8W9xaJJmx3OKX5J-1)

본문은 첨부 Notion ZIP을 기준으로 정리했습니다. 각 문서에 관련 원본 문서명과 출처 링크를 남겼습니다. 외부 링크의 현재 본문·다이어그램은 이번 정리에서 확인한 것으로 간주하지 않습니다.

| 항목 | 등록 상태 |
|---|---|
| GitHub Projects | 준비 중 — 기존 README에 실제 주소 없음 |
| dev 주소 | 미등록 — 기존 README에 실제 주소 없음 |
| prod 주소 | 미등록 — 기존 README에 실제 주소 없음 |
| Grafana 대시보드 | 미등록 — 기존 README에 실제 주소 없음 |

## 폴더

```text
docs/       기획·설계·운영 문서와 결정 기록
services/   서비스 코드 — 기존 README만 있으며 최종 서비스 구성은 미결정
deploy/     Kubernetes 매니페스트·Argo CD 관련 기존 안내
.github/    PR·이슈 템플릿 등 협업 설정
```

기존 README의 프로젝트 소개와 Notion·FigJam 링크를 보존했습니다. 미등록 주소의 자리표시자를 상태 설명으로 정리하고, 다른 문서의 템플릿 예시는 실제 설계와 구분했습니다.
