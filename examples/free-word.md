# Example: the user types a word that wasn't offered

## Turn 1

**User:** (attaches `weekly_meeting_notes.docx`) 회의록 정리해줘

**Assistant:**

📌 **전체 흐름 · 7줄 · 불릿**

- 신규 온보딩 화면 A/B 테스트 결과, B안 전환율 +12%로 B안 채택
- 결제 오류 이슈는 PG사 API 변경이 원인, 이번 주 금요일 패치 예정
- 10월 프로모션 예산 3천만 원 확정, 채널 배분은 다음 회의에서 결정
- 디자인팀 인력 1명 충원 요청, 인사팀과 협의 중
- 고객 문의 응답 시간 평균 6시간 → 목표 3시간
- 담당: 온보딩(민지), 결제 패치(태호), 프로모션(수연)
- 다음 회의: 10월 6일

다르게 원하면 한 단어로 → **할일** · **짧게** · **표**

## Turn 2

**User:** 팀장님께 보고용

**Assistant:**

📌 **결론 먼저 · 3줄 · 보고체**

1. 온보딩 B안 채택(전환율 +12%), 결제 오류는 금주 금요일 패치 완료 예정임.
2. 10월 프로모션 예산 3천만 원 확정, 채널 배분은 10/6 회의에서 결정 예정임.
3. 디자인 인력 1명 충원 및 고객 응대 시간 단축(6h→3h)에 대한 지원 필요함.

다르게 원하면 한 단어로 → **자세히** · **리스크** · **표**

> "보고용" wasn't offered. It was read as a situation and translated into three axis values (see "Free words" in `references/axes.md`). The new tag line shows that interpretation, so if the user actually wanted a longer report they can just reply **자세히** — no clarifying question needed.

## Turn 3 (wrong guess, fixed with one word)

**User:** 자세히

**Assistant:**

📌 **결론 먼저 · 자세히 · 보고체**

(focus and tone kept; the report is rewritten at full length)
