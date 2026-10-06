# designgood

## Purpose

Build UI/UX that feels intentionally designed rather than generated from a generic template. Every interface must have a recognizable visual thesis, clear hierarchy, purposeful interaction, and a coherent system.

## Non-negotiable rules

1. Do not start from a default SaaS dashboard, centered hero, gradient blob, glassmorphism card grid, or interchangeable component library.
2. Choose a visual thesis before writing JSX: editorial, industrial, playful, archival, cinematic, utilitarian, botanical, brutalist, or another specific direction.
3. Use one memorable signature element: a distinctive navigation pattern, type treatment, data visualization, motion behavior, spatial composition, or visual metaphor.
4. Prefer restraint over decoration. If an effect does not improve hierarchy, feedback, comprehension, or brand character, remove it.
5. Use real content and realistic states. Avoid lorem ipsum, vague labels, empty placeholder cards, and fake metrics.
6. Design all important states: loading, empty, error, success, disabled, hover, focus, mobile, and reduced-motion.
7. Make the first viewport answer three questions: what is this, what matters now, and what can I do next?
8. Do not use icons as unexplained decoration. Pair unfamiliar icons with labels or tooltips.
9. Keyboard navigation, visible focus, contrast, semantic HTML, and responsive behavior are part of the design—not cleanup work.
10. Keep dependencies purposeful. Do not add a library merely to imitate a trend.

## Workflow

### 1. Establish the brief

Before coding, write a compact design brief:

- User and primary task.
- Context and emotional tone.
- Visual thesis in one sentence.
- Signature element.
- Content hierarchy.
- Constraints: framework, viewport, data, accessibility, performance.

If the brief is missing, infer sensible defaults and state the assumptions in a comment or plan.

### 2. Create the design direction

Define:

- Color roles, not a random palette: canvas, surface, text, muted text, border, accent, success, warning, danger.
- Type roles: display, body, label, code/data. Use at most two families unless the concept truly needs more.
- Spacing scale and layout rhythm.
- Radius and elevation language.
- Interaction language: instant, tactile, quiet, theatrical, or deliberate.

Name tokens semantically, for example `--color-canvas`, `--color-ink`, `--color-accent`, and `--space-4`.

### 3. Compose before decorating

Start with content hierarchy and layout. Use grids, columns, asymmetry, whitespace, or controlled density to express the concept. Avoid stacking identical cards unless comparison genuinely requires it.

### 4. Implement with resilient primitives

Use semantic structure and small components. Keep content separate from presentation. Build reusable primitives only after the first meaningful screen proves the pattern.

### 5. Add intentional motion

Motion must communicate state, continuity, or priority. Prefer short transitions, staggered entrance only when it clarifies sequence, and respect `prefers-reduced-motion`. Never make the interface feel slow just to look impressive.

### 6. Validate visually

Check at narrow mobile, tablet, and desktop widths. Inspect hierarchy, overflow, contrast, focus order, tap targets, text wrapping, and empty/error states. Replace anything that looks like a stock template.

## Anti-generic checklist

Before delivery, ask:

- Could this screenshot belong to any startup? If yes, sharpen the thesis.
- Is there one detail users will remember tomorrow?
- Are the most important actions visually dominant?
- Does the content feel written for this product?
- Are cards being used because they help, or because cards are easy?
- Does mobile preserve the concept rather than merely stack desktop blocks?
- Does motion have a reason and an accessible fallback?

## Output expectations

When asked to build UI, return or implement:

1. A short design thesis.
2. The key user flow.
3. Token definitions.
4. The component and state plan.
5. The implementation.
6. A visual QA note listing tested viewport sizes and remaining trade-offs.

## Quality bar

A good result is not merely polished. It is specific, legible, responsive, accessible, technically maintainable, and clearly different from the default output of an AI UI generator.
