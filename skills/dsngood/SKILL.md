# /dsngood — handcrafted interface direction

## Purpose

Use this skill when the interface must feel authored, situated, and made for a particular product—not assembled from familiar AI UI patterns. `/dsngood` is a stricter companion to `designgood`: it prioritizes human intent, local specificity, controlled irregularity, and visible design decisions.

## Core idea: authored, not randomized

A handcrafted interface is not messy by default and is not created by adding random asymmetry. It has a point of view that can be explained. Every unusual detail must support a product idea, cultural context, user behavior, or content structure.

Do not simulate human work with fake paper grain, arbitrary doodles, random rotation, fake cursor marks, or decorative imperfections. Use authentic specificity instead: domain language, meaningful provenance, deliberate composition, custom icon geometry, editorial rhythm, and interaction shaped around the real workflow.

## Anti-AI-slop gate

Before coding, identify and remove generic residue:

- Hero copy that could belong to any startup.
- Centered headline plus gradient orb plus two buttons.
- Three equal feature cards with generic icons.
- Excessive rounded containers with no hierarchy.
- Purple/blue gradients used as a substitute for direction.
- Glass panels, floating blobs, abstract 3D shapes, and noise overlays without product meaning.
- Interchangeable dashboard cards with invented metrics.
- Excessive use of pill badges, sparkle icons, and “AI-powered” language.
- Default component-library spacing, radius, typography, and shadows treated as the brand.
- Stock illustrations or decorative images that do not explain the product.

If two screens could be swapped between unrelated products without rewriting the layout, copy, and interaction model, the design is not specific enough.

## Human-origin protocol

### 1. Find the source material

Extract at least three real anchors from the product:

- A task users actually perform.
- A noun, verb, or phrase from the domain.
- A meaningful object, process, place, artifact, or constraint.
- A trust signal users need before acting.
- A real frustration or hesitation the interface should resolve.

If the user has not provided these, ask for them or state assumptions explicitly. Never invent fake customer research.

### 2. Write the author’s note

Before implementation, write five short lines:

- This interface is for…
- It helps them…
- It should feel like…
- The visual metaphor comes from…
- It deliberately refuses…

This prevents the design from becoming a collection of disconnected effects.

### 3. Choose one material language

Choose one primary material language that fits the product: field notebook, instrument panel, workshop bench, library index, printed bulletin, map, ledger, laboratory label, studio canvas, or another defensible source.

Translate it into layout, type, color, borders, density, and interaction. Do not literally decorate the page with props unless the props improve understanding.

### 4. Establish a tension

Strong authored design usually has a controlled tension:

- Dense evidence with generous breathing room.
- Serious information with a warm accent.
- Precise data with an expressive marker.
- Institutional trust with a human voice.
- Historical material with modern interaction.

Name the tension and use it consistently. Do not add competing visual moods.

## Specificity requirements

Every primary screen must contain:

- One domain-specific content decision.
- One non-default layout decision.
- One memorable signature element.
- One interaction that reflects the real task.
- One explicit reason for the chosen type, color, or material language.

“Non-default” does not mean strange. It may be a reading rail, an evidence strip, a chronological spine, a command surface, a split annotation layout, or a carefully chosen density shift.

## Controlled irregularity

Use irregularity only when it creates hierarchy or authorship:

- Break a grid once to signal priority.
- Vary rhythm between sections when content importance changes.
- Use one expressive shape or mark as a recurring signature.
- Let text, not decoration, create visual personality.
- Prefer hand-authored SVG icons or simple geometry when a product concept demands it.

Never randomize positions, rotations, colors, or component styles merely to appear human.

## Copy and naming

Write copy as if a real team owns the product:

- Use concrete verbs: review, compare, resolve, annotate, export, verify.
- Name states precisely: “No evidence collected yet,” not “Nothing here.”
- Explain consequences before irreversible actions.
- Use local or domain vocabulary only when it helps comprehension.
- Remove inflated claims and generic marketing language.

## Component behavior

Components should expose the product’s mental model. Prefer:

- Evidence rows over metric cards when users investigate.
- A work queue over a generic activity feed when users resolve tasks.
- A timeline over disconnected timestamps when sequence matters.
- Inline annotation over hidden detail pages when context matters.
- Reversible controls over destructive toggles.

Do not abstract a component until the repeated pattern is proven. Premature abstraction often creates uniform AI-looking surfaces.

## Visual QA: slop detection

Review the result at real viewport sizes and ask:

1. What could be removed without losing the product idea?
2. Which detail proves this was made for this domain?
3. Where does hierarchy change based on importance?
4. Is any visual irregularity arbitrary?
5. Can a user explain the next action without interpreting decoration?
6. Does the interface still feel authored with content removed?
7. Are empty and error states as specific as the success state?
8. Would a human designer defend every major visual choice?

## Release gate

Score 0–2 for each:

- Source material extracted.
- Author’s note is coherent.
- Material language is consistent.
- Product-specific content is present.
- Layout has intentional authorship.
- Signature element serves the task.
- Copy is concrete and non-generic.
- States and recovery are complete.
- Accessibility is preserved.
- No arbitrary decoration remains.

Minimum: 16/20. Any generic hero/card system, inaccessible interaction, fake research claim, or arbitrary decoration blocks release.

## Required final report

Return:

- Author’s note.
- Source material and assumptions.
- Material language and controlled tension.
- Signature element.
- Anti-slop changes made.
- State and accessibility coverage.
- Score out of 20.
- Remaining compromises.
