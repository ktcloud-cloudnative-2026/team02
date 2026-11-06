# 5xx — 피크오더(Peak Order)

## 한 줄 소개

피크 시간대의 음식 주문·재고·조리 대기 흐름을 시뮬레이션하는 클라우드 네이티브 웹 서비스입니다.

## 문서

<table>
  <thead>
    <tr><th>구분</th><th>문서</th><th>내용</th></tr>
  </thead>
  <tbody>
    <tr><td rowspan="2">기획</td><td><a href="docs/plan.md">기획서</a></td><td>목표 · 범위 · 성공 기준 · 제약</td></tr>
    <tr><td><a href="docs/requirements.md">요구사항</a></td><td>기능(US) · 시스템 요구사항(SR) · 시연 시나리오</td></tr>
    <tr><td rowspan="5">설계</td><td><a href="docs/architecture.md">아키텍처</a></td><td>서비스 구성안 · 책임 · 데이터 소유권</td></tr>
    <tr><td><a href="docs/tech-stack.md">기술 스택</a></td><td>기술 후보 · 선정 근거 · 확정 상태</td></tr>
    <tr><td><a href="docs/api/README.md">API 명세</a></td><td>서비스별 API 문서 템플릿</td></tr>
    <tr><td><a href="docs/erd/README.md">ERD</a></td><td>서비스별 데이터베이스 설계 템플릿</td></tr>
    <tr><td><a href="docs/observability.md">관측 설계</a></td><td>지표 · 로그 · 알림 (기존 템플릿)</td></tr>
    <tr><td rowspan="4">협업</td><td><a href="docs/roles.md">역할</a></td><td>서비스 담당 · 공동 영역 담당 (미확정)</td></tr>
    <tr><td><a href="docs/conventions.md">공통 규칙</a></td><td>Git 전략 · 코드 규칙 · 비밀값 관리</td></tr>
    <tr><td><a href="docs/team.md">팀 운영 약속</a></td><td>회의 · 의사결정 · 팀 규칙</td></tr>
    <tr><td><a href="docs/github-guide.md">GitHub 사용 가이드</a></td><td>clone · 브랜치 · PR · 리뷰</td></tr>
    <tr><td rowspan="3">운영</td><td><a href="docs/runbook.md">런북</a></td><td>장애별 확인 · 조치 (기존 템플릿)</td></tr>
    <tr><td><a href="docs/pending-decisions.md">미결정 사항</a></td><td>PD-01~17 · 문서 충돌 · 팀 확인 질문</td></tr>
    <tr><td><a href="docs/adr/0001-template.md">결정 기록 양식</a></td><td>설계 결정 기록(ADR) 템플릿</td></tr>
  </tbody>
</table>

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
