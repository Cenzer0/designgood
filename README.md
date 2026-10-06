# designgood

A design-direction and UI engineering skill for Codex, Antigravity, and Claude Code. It helps agents create interfaces with a recognizable point of view instead of generic AI aesthetics.

## What changed in 2.0

- Design direction engine with eight task-oriented visual directions.
- Designgood brief required before implementation.
- UX state matrix for loading, empty, error, success, disabled, and focus states.
- Responsive behavior rules instead of breakpoint-only instructions.
- Accessibility, trust, motion, and maintainability release gates.
- A 16-point anti-generic quality score with a 13-point minimum.
- Explicit output contract and honest QA reporting.

## Compatibility

- Codex: load `SKILL.md` as a project skill or from the configured skills directory.
- Claude Code: use `CLAUDE.md` and `.claude/skills/designgood/SKILL.md`.
- Antigravity: use `AGENTS.md` and `.agent/skills/designgood/SKILL.md`.

## Usage

Tell your coding agent to read `SKILL.md` before implementing or reviewing UI. For an existing project, ask it to inspect the stack first, write a designgood brief, then implement and score the result.

## License

MIT
