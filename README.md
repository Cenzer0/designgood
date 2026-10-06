# designgood

![designgood logo](assets/designgood-logo.svg)

> Design with a point of view. Ship with intention.

A design-direction and UI engineering skill for **Codex, Antigravity, and Claude Code**. `designgood` helps coding agents create memorable, useful, accessible interfaces instead of polished-but-generic AI screens.

[![Version](https://img.shields.io/badge/version-2.0.0-ff6b4a.svg)](SKILL.md)
[![Compatible](https://img.shields.io/badge/Codex%20%7C%20Antigravity%20%7C%20Claude%20Code-compatible-173f5f.svg)](SKILL.md)
[![License](https://img.shields.io/badge/license-MIT-2a9d8f.svg)](LICENSE)

## Why designgood?

AI can produce a clean interface in seconds. The hard part is producing one that feels made for a particular product, audience, and moment.

`designgood` adds a point-of-view layer before implementation:

- Starts with a design brief instead of immediately generating components.
- Chooses a visual direction based on the user task.
- Creates a signature element that reinforces the product purpose.
- Forces realistic content and complete interaction states.
- Reviews the result with responsive, accessibility, and anti-generic quality gates.

## What makes it different

### 1. Direction before decoration

The agent must select a primary visual direction—such as Editorial, Instrument, Workshop, Archive, Civic, or Quiet Luxury—and explain why it serves the user task. A direction is a design constraint, not a theme pasted on top.

### 2. Signature over sameness

Every important interface should have at least one memorable, purposeful detail: an evidence timeline, an unusual navigation rhythm, a strong information composition, a tactile interaction, or a domain-specific visual metaphor.

### 3. States are part of the product

Loading, empty, error, success, disabled, focus, async, permission, and reduced-motion states are considered before delivery—not after the screenshot looks good.

### 4. Honest quality scoring

The skill scores specificity, hierarchy, signature, content, interaction, responsive behavior, accessibility, and maintainability. A result needs at least **13/16**, and accessibility or destructive-action failures block release.

## Quick start

### Codex

Copy the repository or its canonical skill into your project’s configured skills directory:

```bash
git clone https://github.com/Cenzer0/designgood.git
cp designgood/SKILL.md ./SKILL.md
cp designgood/AGENTS.md ./AGENTS.md
```

Then ask:

```text
Read SKILL.md. Apply designgood to this interface. Inspect the existing stack first, write the designgood brief, implement the primary flow, cover all important states, and report the final quality score honestly.
```

### Claude Code

Place the skill adapter in your project:

```bash
mkdir -p .claude/skills/designgood
cp designgood/SKILL.md .claude/skills/designgood/SKILL.md
cp designgood/CLAUDE.md ./CLAUDE.md
```

Prompt example:

```text
Use the designgood skill before editing the UI. Do not start from a generic SaaS layout. Produce the brief, choose a visual direction, implement the signature element, and run the quality gates.
```

### Antigravity

Use the Antigravity-compatible adapter:

```bash
mkdir -p .agent/skills/designgood
cp designgood/SKILL.md .agent/skills/designgood/SKILL.md
cp designgood/AGENTS.md ./AGENTS.md
```

Prompt example:

```text
Load the designgood skill and redesign the dashboard as an Instrument direction supported by Archive. Preserve the data hierarchy, add a memorable evidence timeline, and cover mobile, keyboard, loading, empty, and error states.
```

## Recommended workflow

1. **Inspect** — identify framework, routes, components, tokens, data, and constraints.
2. **Brief** — write the user, task, visual thesis, signature, hierarchy, constraints, and non-goals.
3. **Direction** — choose one primary visual direction and at most one supporting influence.
4. **System** — define semantic color, typography, spacing, shape, elevation, and motion tokens.
5. **Flow** — build the main user path with realistic content.
6. **States** — implement loading, empty, error, success, disabled, focus, async, and recovery states.
7. **Signature** — add one purposeful element that makes the interface recognizable.
8. **QA** — test narrow mobile, tablet, desktop, keyboard navigation, contrast, overflow, and reduced motion.
9. **Score** — reach 13/16 or higher; fix blockers before calling the work complete.

## Design directions

| Direction | Best for | Signature opportunities |
|---|---|---|
| Editorial | Research, reading, knowledge | annotations, columns, strong type hierarchy |
| Instrument | Monitoring, security, operations | timelines, thresholds, status grammar |
| Workshop | Creation and configuration | modes, previews, reversible controls |
| Archive | Records, history, collections | provenance, chronology, catalog rhythm |
| Field guide | Learning and onboarding | wayfinding, progressive disclosure, callouts |
| Civic | Campus and public services | trust signals, plain language, inclusive hierarchy |
| Playful utility | Lightweight consumer tools | tactile feedback, expressive micro-interactions |
| Quiet luxury | Premium focused workflows | restraint, material contrast, precise spacing |

## Prompt patterns

```text
Apply designgood to this page. First inspect the existing implementation and write a brief. Choose a visual direction based on the task, not personal preference. Avoid generic hero/card layouts. Implement realistic loading, empty, error, success, focus, and mobile states. Finish with an honest 16-point score and list unresolved trade-offs.
```

```text
Review this interface using designgood only. Identify generic residue, hierarchy problems, missing states, accessibility risks, responsive failures, and unnecessary decoration. Propose the smallest high-impact changes before editing code.
```

```text
Use designgood for a cybersecurity monitoring screen. Pick Instrument with Archive support. The signature must be a confidence-banded evidence timeline. Do not use neon cyberpunk decoration or hide the recommended next action in a data wall.
```

## Repository map

```text
designgood/
├── SKILL.md                         # Canonical skill
├── AGENTS.md                        # Codex / Antigravity adapter
├── CLAUDE.md                        # Claude Code adapter
├── examples/
│   ├── brief.md                     # Complete brief example
│   └── review-checklist.md          # Manual QA checklist
├── assets/
│   ├── designgood-logo.svg         # Full logo
│   └── designgood-mark.svg         # Compact mark
└── LICENSE
```

## Quality gate

Score each category from 0 to 2:

| Category | Question |
|---|---|
| Specificity | Does the interface have a defensible visual thesis? |
| Hierarchy | Can users find purpose, priority, and next action? |
| Signature | Is there a purposeful memorable element? |
| Content | Are labels and states specific to the domain? |
| Interaction | Are feedback, recovery, and focus complete? |
| Responsive | Does the concept survive phone, tablet, and desktop? |
| Accessible | Are semantic, keyboard, contrast, status, and motion needs addressed? |
| Maintainable | Are tokens, components, and data boundaries coherent? |

**Release threshold:** 13/16 or higher. Any accessibility or destructive-action blocker means the interface is not ready.

## Contributing

Useful contributions include new domain examples, framework-specific adapters, accessibility test cases, and before/after case studies. Keep the core principles framework-agnostic and avoid adding trend recipes that encourage generic output.

1. Fork the repository.
2. Add a focused improvement or example.
3. Explain the user problem it solves.
4. Check that the writing remains tool-agnostic.
5. Open a pull request with before/after reasoning.

## License

MIT
