# shipwithian skills

Free, ready-to-use skills for [Claude](https://claude.ai) by [shipwithian](https://shipwithian.online). Ship it.

A **skill** is a set of instructions Claude loads when a task needs it, so it works the same way every time without you re-explaining. This repo is a growing list of skills built from real work, packaged so anyone can add them to Claude Code or claude.ai in a minute.

## Skills

| Skill | What it does | Good for |
|---|---|---|
| [direction-grill](plugins/direction-grill/skills/direction-grill/SKILL.md) | Questions you in numbered rounds, each with a recommended answer, until your direction is clear, then writes a one-page plan. | "I have too many ideas. Which one do I focus on?" Career moves, side businesses, family-business decisions. |

## Install

### Option 1: Claude Code (recommended)

Run these inside Claude Code:

```
/plugin marketplace add ianlabicani/skills
/plugin install direction-grill@shipwithian-skills
```

The first command adds this repo as a skill source. The second installs one skill from it. To get updates later, run `/plugin marketplace update shipwithian-skills`.

### Option 2: claude.ai (web, desktop, or mobile app)

1. Download the skill's zip from the [`dist`](dist) folder, e.g. [`direction-grill.zip`](dist/direction-grill.zip).
2. In claude.ai, open **Settings → Customize → Skills**.
3. Click **Add**, choose upload, and select the zip.

Skills on claude.ai need a paid plan.

### Option 3: Manual copy (Claude Code)

Copy a skill folder into your personal skills folder:

```
git clone https://github.com/ianlabicani/skills
cp -r skills/plugins/direction-grill/skills/direction-grill ~/.claude/skills/
```

## How to use direction-grill

Start a chat and describe your situation in a sentence or two:

> Grill me on my direction. I'm 24, I work full-time, I support my family, and I want more time freedom. My ideas are a kiosk, freelancing, and farming.

Then:

1. Claude asks a **round** of numbered questions, each with its recommended answer.
2. You reply by number: `1. agree`, `2. no, because...`.
3. Claude looks up facts itself (prices, trends, weather) and only asks you for decisions.
4. Each round builds on your answers until every part of the plan is settled.
5. You get a **one-page direction**: your main bet, money targets, roles, rules, a timeline, and a dated test for "is it working?".

Be honest about money, family, and the things you avoid. The plan is only as good as the answers.

## Repo layout

```
.claude-plugin/marketplace.json   list of skills Claude Code can install
plugins/<skill>/                  one plugin per skill
  .claude-plugin/plugin.json      plugin name, version, description
  skills/<skill>/SKILL.md         the skill's instructions
dist/<skill>.zip                  upload-ready zip for claude.ai
```

## Adding a new skill

1. Create `plugins/<name>/skills/<name>/SKILL.md` with `name` and `description` in the frontmatter.
2. Add `plugins/<name>/.claude-plugin/plugin.json`.
3. Add an entry to `.claude-plugin/marketplace.json`.
4. Zip the skill folder into `dist/<name>.zip` (the zip should contain `<name>/SKILL.md`).
5. Add a row to the table above.
6. Check it with `claude plugin validate .`

## License

[MIT](LICENSE). Use, share, and adapt freely. A credit to shipwithian is appreciated.
