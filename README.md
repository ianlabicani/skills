# shipwithian skills

Free Claude skills made by [shipwithian](https://shipwithian.online). Ship it.

## Skills

| Skill | What it does |
|---|---|
| [direction-grill](plugins/direction-grill/skills/direction-grill/SKILL.md) | Grills you about your life or business direction in numbered rounds, each with a recommended answer, then gives you a one-page plan. Good for "I have too many ideas, which one do I focus on?" |

## Install

### Claude Code

```
/plugin marketplace add ianlabicani/skills
/plugin install direction-grill@shipwithian-skills
```

### claude.ai (web or desktop app)

1. Download [`dist/direction-grill.zip`](dist/direction-grill.zip).
2. Go to **Settings → Customize → Skills**, click **Add**, and upload the zip.

Skills on claude.ai need a paid plan.

## Use it

In any chat, type something like:

> Grill me on my direction. I'm 24, I work full-time, I support my family, and I want more time freedom. My ideas are a kiosk, freelancing, and farming.

Answer each round by number ("1. agree, 2. no, because..."). It ends with a one-page plan.
