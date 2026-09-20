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

## Currently installed

From [`emilkowalski/skills`](https://github.com/emilkowalski/skills) — design &
animation skills by Emil Kowalski:
`animate`, `animate-expo`, `animation-vocabulary`, `apple-design`, `ask-sonner`,
`emil-design-eng`, `find-animation-opportunities`, `improve-animations`,
`mobile-native`, `pick-ui-library`, `prototype`, `review-animations`,
`write-swift`.
