# one-word-steer

**English** | [한국어](README.ko.md)

**Fix "close but not quite" AI answers with a single word.**

A [Claude Agent Skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) that makes every open-ended answer steerable.

---

## The problem

You ask an AI to "summarize this document." The answer is fine... but too long. Or too technical. Or focused on the wrong thing. You can't quite say what's wrong, and rewriting the prompt is a chore.

## How it works

Claude shows the criteria it chose as a tiny tag line, and offers 2–3 one-word handles at the bottom.

```
You: (attaches report.pdf) Summarize this document.

Claude:
📌 Overview · 6 lines · For practitioners

- Q3 revenue was $31M, up 8% from last quarter
- ...

Want it different? Reply with one word → One-line · Numbers only · To-dos
```

Reply with one word. Only that dimension changes; everything else stays.

```
You: To-dos

Claude:
📌 Action items · 6 lines · For practitioners      ← only the focus changed

- Pricing: redesign one-off pricing
- ...

Want it different? Reply with one word → Shorter · Table · Formal
```

### Key ideas

- **Show, don't explain.** Criteria are tags ("5 lines", "Beginner"), never sentences.
- **One word = one axis.** Axes: length · level · focus · format · tone. "Simpler" never changes the length.
- **Words chosen per answer.** The suggestions point where *this* answer most likely missed, not a fixed menu.
- **Free words welcome.** Type "for my boss" or "for Slack" and Claude translates it into axis values. The new tag line shows how it read you, so a wrong guess is one word away from fixed.
- **No clarifying questions** unless a word is truly uninterpretable.
- **Remembers** your choice for the rest of the conversation.
- **Stays out of the way** for short facts, code and casual chat.
- **Works in your language.** Tags and words follow the language you write in.

## Install

### Claude Code

```bash
# personal (all projects)
git clone https://github.com/jiseong-jang/one-word-steer.git ~/.claude/skills/one-word-steer

# or project-level
git clone https://github.com/jiseong-jang/one-word-steer.git .claude/skills/one-word-steer
```

### Claude.ai (web / desktop)

1. Download this repo as a ZIP (the `one-word-steer` folder with `SKILL.md` at its top level).
2. Settings → Capabilities → Skills → **Upload skill**.

### Other Agent Skills–compatible tools

Copy the folder into your tool's skills directory (e.g. `.agents/skills/`).

## Structure

```
one-word-steer/
├── SKILL.md              # when to trigger, output format, steering rules
├── references/
│   └── axes.md           # 5 axes, steer-word vocabulary, free-word mapping
└── examples/
    ├── summary.md        # summarizing a report
    ├── explain.md        # explaining a concept
    └── free-word.md      # user types a word that wasn't offered
```

## Customize

Edit `references/axes.md` to add your own words or axes. For example, an "audience" axis for your team (for designers / for engineers / for executives), or domain-specific focuses such as clauses · deadlines · penalties for contracts.

## License

MIT
