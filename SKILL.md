---
name: one-word-steer
description: Makes open-ended answers steerable with a single word. Adds a tiny tag line showing the criteria the answer was built on (e.g. "Conclusion first · 5 lines · For practitioners") and a short row of one-word alternatives (e.g. "One-line · Simpler · Numbers only"). When the user replies with one word, regenerate by shifting only that one dimension and keep everything else. Use this whenever the request has many valid answers — summarizing a document or file, explaining a concept, drafting or rewriting text, reports, notes, overviews, comparisons — and also whenever the user replies to a previous answer with a single word or a very short correction like "shorter", "easier", "쉽게", "짧게", "핵심만", even if they never mention this skill. Do not use for short factual answers, code, or casual chat.
---

# One-Word Steer

AI answers often land *close* to what the user wanted but not quite: too long, too hard, the wrong focus. Users usually can't say precisely what's wrong, and rewriting the prompt is tiring. But they recognize what they want the moment they see a word for it.

This skill closes that gap in two moves:

1. **Show the criteria as tags.** Before the answer, a single line names the 2–3 choices you made. The user sees at a glance what you assumed.
2. **Offer one-word handles.** After the answer, 2–3 single words point in the directions this answer is most likely to have missed. The user replies with one word, and you rebuild the answer by changing only that dimension.

The whole point is low effort for the user. Never explain the criteria, never list options in sentences, never ask a question when a word will do.

## When to apply

Apply to answers where many versions could be "right":
- Summaries of documents, files, meetings, articles
- Explanations of concepts
- Drafts, rewrites, reports, notes, overviews, comparisons

Skip it for: one-sentence factual answers, code, casual chat, and anything shorter than about 4 lines. A tag line on a tiny answer is clutter.

## Output format

Match the user's language for the tags, words and answer. Korean examples are shown here because the format matters most there; English works the same way.

```
📌 **결론 먼저 · 5줄 · 실무자용**

(answer)

다르게 원하면 한 단어로 → **한줄** · **쉽게** · **숫자만**
```

English:

```
📌 **Conclusion first · 5 lines · For practitioners**

(answer)

Want it different? Reply with one word → **One-line** · **Simpler** · **Numbers only**
```

### Rules for the tag line (top)

- 2–3 tags, each one to three words, separated by ` · `.
- Each tag names the current value on one axis (see `references/axes.md`). Pick the axes that most shaped this answer — usually length, and one or two of level, focus, format, tone.
- Tags state a choice, not a description. "5줄" not "다섯 줄 정도로 간결하게 정리함".

### Rules for the steer words (bottom)

- Offer exactly 2–3 words. Never more.
- Choose them per answer, not from a fixed menu. Ask yourself: *if this answer disappoints, which direction is most likely?* Long answer → offer a shorter length. Technical content → offer an easier level. Number-heavy source → offer a numbers focus. Opinion-heavy draft → offer a tone shift.
- Each word must move a **different** axis, so the choices are genuinely different.
- Each word must be vivid enough that the user can picture the result: "한줄" beats "간결하게", "초등학생" beats "쉽게 설명". See `references/axes.md` for the vocabulary.
- Bold each word so it reads like a button.

## When the user replies with a word

1. **Map the word to one axis and a new value.** Use `references/axes.md`. If the word is one you offered, the mapping is already known.
2. **Change only that axis.** Keep every other tag exactly as it was. If "쉽게" changes the length too, the user loses trust in the controls. The exception is when the new value forces a change (e.g. "한줄" makes a table format impossible); then adjust the dependent tag and it will show in the new tag line.
3. **Regenerate the full answer** from the source material, not by editing the previous answer. Shortening a long answer by trimming produces worse results than writing to the new length.
4. **Show the updated tag line**, so the user can confirm what changed. Then offer fresh steer words chosen for the new answer (don't repeat the word just used).
5. **Keep the choice for the rest of the conversation.** If the user said "쉽게" once, the next summary in this conversation should start at the easier level.

### Words you didn't offer

Users will type their own words: "보고용", "슬랙에 올릴 거", "더 날카롭게", "for my boss". Accept them. Translate the word into one or more axis values (see the "free words" section of `references/axes.md`), rebuild, and let the new tag line show your interpretation. If you guessed wrong, the tag line makes that visible and the user fixes it with one more word. That's cheaper for them than you asking a clarifying question.

Only ask a question if the word is truly uninterpretable (e.g. a typo or a word with opposite possible meanings). Ask it in one short line with two options.

### Multiple words

If the user sends two words ("짧게 쉽게"), apply both — each still changes only its own axis.

## Examples

Detailed before/after conversations are in `examples/`:
- `examples/summary.md` — summarizing a report
- `examples/explain.md` — explaining a concept
- `examples/free-word.md` — the user types a word that wasn't offered

Read one if you are unsure how the format should look in practice.
