# skills

My Claude Code skills for building apps from a phone, version by version.

- **`/plan-version <idea>`**: grills me, agrees what "looks right" before any code, and writes one spec issue with slices, ✋ checkpoints and a decision log.
- **`/build-version <issue>`**: builds that spec with parallel `slice-builder` agents (at most 3 at once), reviews and merges each, and stops after two failed looks to ask me.

Lessons baked in: agree the look first, options before polish, two strikes then simplify, record every decision in the issue, builders read only their own slice.

## Install (in a Claude Code session on the project)

Ask Claude: "install my skills from darrenkim05/skills". It runs:

```
npx skills add darrenkim05/skills -s '*' -a claude-code -y --copy
```

then commits `.claude/skills/` and starts a new session so the skills load. The first `/plan-version` adds a `## Version builds` section to the project's `CLAUDE.md`, and the first `/build-version` installs the `slice-builder` agent.

To update later: "update my skills" (`npx skills update -p -y`).
