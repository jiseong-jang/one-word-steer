# Axes and steer words

Every tag and every steer word belongs to exactly one axis. One word = one axis moved.

Pick words from the "steer word" columns when offering choices. Use the "also accepts" column to interpret what users type. Korean and English are both listed; always answer in the user's language.

## 1. Length (분량)

| Value | Tag (ko / en) | Steer word (ko / en) | Also accepts |
|---|---|---|---|
| One sentence | 한줄 / One line | **한줄** / **One-line** | 한 문장, 한마디, tl;dr, 요점만 |
| Very short (≈3 lines) | 3줄 / 3 lines | **짧게** / **Shorter** | 간단히, 줄여줘, brief, quick |
| Medium (≈5–8 lines) | 5줄 / 5 lines | — (default) | |
| Detailed | 자세히 / Detailed | **자세히** / **Deeper** | 길게, 풀어서, 전부, in depth, more |

Rule of thumb: shorter always means *choosing* what matters, not compressing everything.

## 2. Level (난이도)

| Value | Tag | Steer word | Also accepts |
|---|---|---|---|
| Child-level | 초등학생용 / For a kid | **초등학생** / **Like I'm 10** | 아주 쉽게, eli5 |
| Beginner | 입문자용 / Beginner | **쉽게** / **Simpler** | 비전공자, 용어 빼고, plain |
| Practitioner | 실무자용 / Practitioner | — (default) | |
| Expert | 전문가용 / Expert | **전문가** / **Expert** | 깊게, 기술적으로, technical |

Easier means: no jargon (or jargon explained in passing), one concrete example or analogy, shorter sentences. It does not mean shorter overall — length is a separate axis.

## 3. Focus (초점)

What the answer is *about*. Choose values that fit the source; these are common ones.

| Value | Tag | Steer word | Also accepts |
|---|---|---|---|
| Conclusion / decision | 결론 먼저 / Conclusion first | **결론** / **Bottom line** | 그래서 뭐, 핵심, so what |
| Numbers / data | 숫자 중심 / Numbers | **숫자만** / **Numbers only** | 수치, 데이터, 통계, metrics |
| Action items | 할 일 중심 / Action items | **할일** / **To-dos** | 액션, 뭐 해야 돼, next steps |
| Risks / issues | 리스크 중심 / Risks | **리스크** / **Risks** | 문제점, 주의할 점, 걸리는 거 |
| Background / why | 배경 중심 / Background | **배경** / **Why** | 이유, 맥락, context |
| Overall flow | 전체 흐름 / Overview | **흐름** / **Big picture** | 개요, 구조, outline |

## 4. Format (형식)

| Value | Tag | Steer word | Also accepts |
|---|---|---|---|
| Prose | 문장형 / Prose | **문장** / **Prose** | 글로, 이어서, paragraph |
| Bullets | 불릿 / Bullets | **불릿** / **Bullets** | 항목별, 목록, list |
| Table | 표 / Table | **표** / **Table** | 비교표, 정리표 |
| Q&A | 문답형 / Q&A | **문답** / **Q&A** | 질문으로, FAQ |

## 5. Tone (말투)

| Value | Tag | Steer word | Also accepts |
|---|---|---|---|
| Casual | 편하게 / Casual | **편하게** / **Casual** | 반말, 친구처럼, 가볍게 |
| Neutral | — (default, usually no tag) | | |
| Formal / report | 보고체 / Formal | **보고체** / **Formal** | 공식적으로, ~함 체, 격식 |
| Sharp / critical | 날카롭게 / Critical | **날카롭게** / **Critical** | 비판적으로, 냉정하게, blunt |

## Free words → axis values

Users often name a *situation* instead of a dimension. Translate it into 1–3 axis values and let the new tag line show your reading.

| User says | Interpret as |
|---|---|
| 보고용, 윗선에, for my boss | Conclusion first · 3 lines · Formal |
| 슬랙/카톡에 올릴 거 | 3 lines · Casual · Bullets |
| 발표용, for slides | Bullets · Conclusion first · 3–5 lines |
| 공부용, to study | Detailed · Beginner · Q&A or Bullets |
| 회의 전에 빨리 | One line or 3 lines · Action items |
| 뻔해, 식상해, generic | Focus shift to the most specific/surprising content; drop general statements |
| 틀렸어 / 그게 아니라, that's wrong | Not a style issue — reread the source and fix the content; keep tags |

## Choosing which 2–3 words to offer

Look at the answer you just wrote and pick the most likely miss on different axes:

- Longer than ~6 lines → offer a shorter length (**한줄** or **짧게**).
- Contains 2+ technical terms → offer an easier level (**쉽게**).
- Source has many figures → offer **숫자만**.
- Source is a meeting/plan → offer **할일**.
- You chose prose → offer **불릿** or **표**; you chose bullets on a comparison → offer **표**.
- Draft text for others → offer a tone word.

Never offer the value that's already active, and never offer two words on the same axis.
