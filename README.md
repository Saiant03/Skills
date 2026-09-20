# skills

Personal collection of Claude Code / agent skills, kept in one place so they
persist across sessions and can be reused in any project.

## How it's used

In a working session (e.g. another repo), attach this repo so its skills load:
the agent runs `add_repo` + `register_repo_root` for `saiant03/skills`, and the
skills under `.claude/skills/` become available.

## Adding more skills

Installed with the [skills.sh](https://skills.sh) CLI:

```bash
npx skills@latest add <owner>/<repo>
```

This writes the skill into `.agents/skills/`, symlinks it into `.claude/skills/`
for Claude Code, and records the source in `skills-lock.json`. Commit and push
so it persists.

## Source repos

Skills currently installed come from these repos (see `skills-lock.json` for the
full, authoritative per-skill list):

- [`emilkowalski/skills`](https://github.com/emilkowalski/skills) — design & animation
- [`pbakaus/impeccable`](https://github.com/pbakaus/impeccable) — frontend design/polish
- [`Leonxlnx/taste-skill`](https://github.com/Leonxlnx/taste-skill) — design taste, image-to-code, brandkit
- [`microsoft/playwright-cli`](https://github.com/microsoft/playwright-cli) — Playwright CLI + dev
- [`img2threejs/img2threejs`](https://github.com/img2threejs/img2threejs) — image → three.js
- [`thedotmack/claude-mem`](https://github.com/thedotmack/claude-mem) — memory, planning, workflow skills
- [`rebelytics/one-skill-to-rule-them-all`](https://github.com/rebelytics/one-skill-to-rule-them-all) — task-observer
- [`DietrichGebert/ponytail`](https://github.com/DietrichGebert/ponytail) — minimal-code / lazy-senior-dev
- [`nextlevelbuilder/ui-ux-pro-max-skill`](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) — UI/UX design intelligence (styles, palettes, fonts, UX rules)

## Reference skills (added manually, not via the CLI)

These repos ship no `SKILL.md`, so they're wrapped as reference skills:

- **`awesome-design-md`** — 74 brands' design tokens (colors/type/motion), bundled from [`VoltAgent/awesome-design-md`](https://github.com/VoltAgent/awesome-design-md) under `design-md/`.
- **`headroom`** — reference + install notes for [`headroomlabs-ai/headroom`](https://github.com/headroomlabs-ai/headroom), a local context-compression tool for AI agents (the tool itself is installed separately, not vendored here).
