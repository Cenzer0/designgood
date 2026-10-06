# designgood 2.0

## Mission

Build interfaces with a clear point of view, useful interaction, and production-level quality. The goal is not merely to make a polished screen; it is to make a product that could not be mistaken for a generic AI-generated template.

## Operating contract

Before changing UI code, produce a short `designgood brief` containing:

- User, context, and primary job.
- Visual thesis: one sentence describing the world, mood, and material language.
- Signature: one memorable element that reinforces the product purpose.
- Content hierarchy: what users must notice, understand, and do first.
- Constraints: framework, existing tokens, data, accessibility, performance, and target viewports.
- Two deliberate things the design will not do.

If information is missing, infer conservative assumptions and label them. Do not invent brand facts or product requirements.

## Design direction engine

Select one primary direction and at most one supporting influence. Do not mix unrelated trends.

| Direction | Useful when | Material cues | Avoid |
|---|---|---|---|
| Editorial | reading, research, knowledge | strong type scale, columns, annotations, whitespace | dashboard card soup |
| Instrument | monitoring, operations, security | dense data, status grammar, monospace accents, clear thresholds | decoration that competes with alerts |
| Workshop | creation, configuration, building | tool surfaces, previews, explicit modes, reversible actions | hidden controls |
| Archive | history, collections, records | labels, provenance, chronology, catalog rhythm | fake nostalgia |
| Field guide | learning, exploration, onboarding | progressive disclosure, callouts, wayfinding | tutorial walls |
| Civic | public, campus, community services | calm trust signals, plain language, inclusive hierarchy | dark patterns |
| Playful utility | consumer tools, lightweight workflows | expressive color, tactile feedback, small surprises | childish copy or noisy motion |
| Quiet luxury | premium, focused workflows | restraint, precise spacing, material contrast | gold gradients and status theater |

When selecting a direction, explain why it serves the user task. The direction is a constraint, not a skin.

## Anti-generic rules

- No default centered hero with a gradient blob unless the brief explicitly demands it.
- No interchangeable three-column feature cards, oversized rounded rectangles, or glassmorphism by default.
- No random gradients, excessive shadows, decorative noise, or animation without a job.
- No lorem ipsum, vague labels, fake metrics, or unexplained icon-only actions.
- No copy that says “seamless,” “revolutionary,” “next-generation,” or “unlock your potential” without specific evidence.
- Do not use a UI library’s default theme as the visual identity.
- Reuse patterns only when they improve recognition, comparison, or speed.

## Design system minimum

Define semantic tokens before styling details:

- Color: canvas, surface, raised surface, ink, muted ink, border, accent, success, warning, danger, focus.
- Typography: display, heading, body, label, caption, code/data.
- Layout: content max width, column widths, spacing scale, section rhythm.
- Shape: radius levels, border weight, elevation levels.
- Motion: duration, easing, entrance, feedback, exit, reduced-motion fallback.

Prefer CSS variables or the project’s existing token system. Name tokens by role, not by literal color, such as `--color-ink` instead of `--black`.

## Content and hierarchy

For every primary screen, define:

1. Orientation: what is this and where am I?
2. Priority: what changed or matters now?
3. Action: what can I do next?
4. Evidence: why should I trust the information?
5. Recovery: what happens when data is missing or an action fails?

Use realistic domain language. Empty states should explain the condition and give a useful next action. Error messages should say what happened, what is safe, and how to recover.

## UX state matrix

Do not ship a primary interaction until these states are considered:

| Surface | Loading | Empty | Error | Success | Disabled | Focus |
|---|---|---|---|---|---|---|
| Page/data view | meaningful skeleton or progress | explanation + next action | cause + recovery | confirmation or updated data | explain why | logical keyboard order |
| Form | preserve entered values | helpful initial guidance | field-level and summary feedback | clear completion | explain prerequisite | visible focus and labels |
| Destructive action | no ambiguous spinner | not applicable | reversible recovery | explicit confirmation | prevent unsafe action | focus returns predictably |
| Async operation | status and cancellation | not applicable | retry or support path | durable result | avoid duplicate submission | announce status |

Include optimistic UI only when failure recovery is clear.

## Responsive behavior

Design behavior, not just breakpoints:

- Identify what remains, collapses, reorders, scrolls, or becomes progressive disclosure.
- Preserve the visual thesis on mobile; do not blindly stack desktop cards.
- Keep primary actions reachable and maintain comfortable tap targets.
- Prevent horizontal overflow, clipped text, and layout shifts.
- Check long labels, large numbers, localization-like expansion, and empty content.

Test at a narrow phone, a tablet, and a desktop viewport. Use the project’s actual target sizes when available.

## Accessibility and trust gates

Before delivery, verify:

- Semantic landmarks and heading order.
- Keyboard access for every action.
- Visible focus that is not removed by styling.
- Labels and instructions for form controls.
- Color is not the only status signal.
- Sufficient contrast and readable text sizing.
- Reduced-motion behavior.
- Clear confirmation for destructive or irreversible actions.
- No sensitive information exposed in UI copy, URLs, logs, or client-side data.

## Motion rules

Motion must communicate hierarchy, cause/effect, continuity, or feedback. Use the smallest motion that does the job. Avoid perpetual motion and delayed interaction. Provide a reduced-motion fallback and never hide essential information behind animation.

## Implementation strategy

1. Inspect the existing stack, routes, tokens, components, and constraints.
2. Write the designgood brief.
3. Establish or extend semantic tokens.
4. Build the content skeleton and primary flow.
5. Implement the signature element.
6. Add states and responsive behavior.
7. Add restrained motion and interaction feedback.
8. Run the quality gates and remove generic residue.

Prefer small, composable components. Keep content/data separate from presentation. Avoid introducing dependencies unless they solve a real project constraint.

## Quality score

Score each category from 0 to 2:

- Specificity: the interface has a defensible visual thesis.
- Hierarchy: users can identify purpose, priority, and next action quickly.
- Signature: at least one purposeful memorable element exists.
- Content: labels and states are specific to the domain.
- Interaction: feedback, recovery, and focus behavior are complete.
- Responsive: the concept survives mobile, tablet, and desktop.
- Accessible: semantic, keyboard, contrast, motion, and status requirements are addressed.
- Maintainable: tokens, components, and data boundaries are coherent.

Minimum release score: 13/16. Any accessibility or destructive-action failure blocks release regardless of score.

## Final output contract

For a UI implementation, provide:

1. Designgood brief.
2. Implemented user flow.
3. Token and component summary.
4. State matrix coverage.
5. Responsive/accessibility QA note.
6. Known trade-offs and next improvements.

Do not claim visual testing that was not actually performed.
