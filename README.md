# designgood

![designgood logo](assets/designgood-logo.svg)

> Design with a point of view. Ship with intention.

A design-direction and UI engineering skill for Codex, Antigravity, and Claude Code. `designgood` helps coding agents create memorable, useful, accessible interfaces instead of polished-but-generic AI screens.

## New: /dsngood handcrafted mode

Use `/dsngood` when you want UI/UX that feels **authored, contextual, and made for a real product**. It is stricter than the base skill and adds:

- Real source-material extraction before coding.
- An author’s note that explains the design origin.
- A defensible material language such as field notebook, instrument panel, library index, or workshop bench.
- Controlled tension and intentional irregularity.
- Stronger anti-AI-slop detection.
- A 20-point handcrafted release gate with a minimum score of 16/20.

Human-feeling design does not mean random decoration. `/dsngood` explicitly rejects fake imperfections, random rotations, arbitrary asymmetry, decorative noise, generic copy, and trend stacks. The interface should feel handmade because its decisions are specific—not because it pretends to be messy.

## Quick start

```bash
git clone https://github.com/Cenzer0/designgood.git
```

For normal design direction, load `SKILL.md`. For the stricter handcrafted mode, load both:

```text
Read SKILL.md and skills/dsngood/SKILL.md before editing the UI. Apply /dsngood mode. Extract real source material, write the author’s note, choose one material language, create one purposeful signature element, remove AI-slop patterns, and finish with the 20-point handcrafted score.
```

## Compatibility

- **Codex:** place `SKILL.md` and `AGENTS.md` in the project, then reference `skills/dsngood/SKILL.md` for handcrafted mode.
- **Claude Code:** place the canonical skill under `.claude/skills/designgood/` and ask the agent to load `skills/dsngood/SKILL.md`.
- **Antigravity:** place the skill under `.agent/skills/designgood/` and reference the same handcrafted mode file.

## What designgood prevents

- Default centered heroes with gradient blobs.
- Three equal feature cards with generic icons.
- Excessive pills, sparkle icons, glass panels, and floating shapes.
- Invented metrics and vague empty states.
- UI-library defaults presented as product identity.
- Random “handmade” effects that do not improve comprehension.

## Authored-design workflow

1. Extract the real user task, domain nouns, meaningful objects, trust signals, and hesitation points.
2. Write the author’s note: for whom, what task, what feeling, what source material, and what is refused.
3. Choose one material language and one controlled tension.
4. Define semantic tokens and a non-default layout decision.
5. Build the primary flow with domain-specific content.
6. Add a signature element that supports the task.
7. Cover loading, empty, error, success, disabled, focus, async, permission, and reduced-motion states.
8. Review for generic residue, arbitrary decoration, accessibility, responsive behavior, and maintainability.
9. Score the result. Handcrafted mode requires at least 16/20.

## Example prompt

```text
Use /dsngood for this campus cybersecurity incident workspace. Do not use a generic SaaS dashboard, neon cyberpunk decoration, or random “handmade” effects. Extract the real investigation workflow, write the author’s note, use an instrument-panel material language with archive support, and make the signature an evidence timeline with confidence bands. Cover keyboard, mobile, loading, empty, error, recovery, and reduced-motion states. Report the 20-point score honestly.
```

## Repository map

```text
designgood/
├── SKILL.md
├── skills/dsngood/SKILL.md
├── dsngood/SKILL.md
├── AGENTS.md
├── CLAUDE.md
├── examples/
├── assets/
└── LICENSE
```

## License

MIT
