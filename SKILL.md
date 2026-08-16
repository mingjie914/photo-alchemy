---
name: photo-alchemy
description: "Create source-aware raster artworks from supplied photographs through abstraction (perceptual events without photo pixels), extend (a truthful photographic anchor plus an independent material field), or reduction (a new construction around the essential source relationship without photo pixels). Use when the user wants to elevate a photo into art, requests an artistic reinterpretation, names one supported method, or wants to compare methods without copying a fixed reference style."
---

# Photo Alchemy

Create one or more finished artworks from a photograph. Let the user choose a method, request several, or ask the skill to select the most suitable direction. When generating more than one, share only the source analysis; do not share layouts, edge treatments, mark systems, or style shortcuts between methods.

## Decision order

Resolve conflicts in this order:

1. Obey the selected method's defining rule for photographic material.
2. Embody one source-specific artistic proposition in visible form.
3. Preserve only the relationships and anchors necessary for that proposition.
4. Establish hierarchy, eye movement, and purposeful quiet space.
5. Make color and material perform a structural or emotional role.
6. Prefer omission over decoration, reconstruction, or a recognizable borrowed formula.

## Core workflow

1. Inspect the photograph and build a compact Scene Card:
   - core subject or event, its essential relationship, and the dominant perceptual fact: gesture, interval, rhythm, mass, light, or movement;
   - spatial evidence and visual-weight structure: relative position, direction, scale, overlap, enclosure, natural quiet areas, and likely eye path;
   - emotional residue or visual tension, plus one internal artistic proposition for what the photograph can become;
   - source-specific anchors to evaluate, including at least one relational fact; literal cues survive only when the selected method needs them;
   - what to retain, merge, release, translate, and leave blank;
   - palette and material opportunities that can serve the proposition.
2. Read [references/branches.md](references/branches.md), select the requested or most suitable method, and resolve its Method Brief.
   When no method is named, choose from the strongest source evidence: use `extend` when a truthful photographic anchor is indispensable; `abstraction` when a perceptual event carries the meaning without requiring recognizability; or `reduction` when one essential relationship and a few anchors can remain specific after descriptive reality is redrawn. Choose one; do not blend or generate all methods unless asked.
3. Choose the output ratio from the source orientation and composition. Never force a preset poster ratio.
4. Read [references/prompt-compiler.md](references/prompt-compiler.md). Compile a separate three-part generation prompt for each method and verify that its required fields are resolved.
5. Generate each selected method from the original photograph only. Do not use another artist's output or a prior result as a visual reference unless the user explicitly supplies it for that purpose.
6. Read [references/review.md](references/review.md). Inspect each result at normal and thumbnail scale.
7. Regenerate at most once per branch, and only for a concrete failure. State the correction and freeze everything else.
8. Save every requested raster file and return it with a concise method-specific rationale. Reveal the compiled prompt only when the user asks.

## Source handling and output

- Use a supplied photograph only for the requested generation. Do not browse for it, publish it, add it to the Skill repository, or reuse it in another task unless the user asks.
- By default, return one finished raster for each selected method, identify the method, and give a one- or two-sentence rationale in the user's language. Do not rank the branches unless asked.
- Keep the Scene Card, Method Brief, and compiled prompt internal unless the user asks to inspect them. Do not add a visible title, typography, credits, attribution, metadata, or promotional text unless the user explicitly requests that content.

## Shared constraints

- Treat source analysis as material for an artwork, not as a checklist to reconstruct.
- Preserve relationships before surface detail.
- Keep each visible element traceable to a source fact or a necessary compositional function.
- Allow purposeful omission, recomposition, exaggeration, and palette shift when they strengthen the artwork without replacing the source's meaning.
- Use color as structure or emotional action. It may resonate with, compress, or deliberately counterpoint the source; never add detached color decoration.
- Treat an internal working title as a disposable semantic check, not a reusable prompt constant. Derive it from the current photo, do not render it unless requested, and never reuse a prior image's title.
- Avoid generic painterly rendering, vintage filters, and other preset-style treatments that are not source-derived, as well as arbitrary marks. Do not add or fabricate logos, watermarks, credits, metadata, or promotional text. Existing marks inside a truthful `extend` anchor remain source pixels rather than a new design layer.
- Treat the Skill and its generated artworks as intended for personal, educational, research, and non-commercial use unless the relevant rights holder grants separate permission.

## Branch independence

- **`abstraction`** communicates the dominant perceptual event without retaining photo pixels or copying the original silhouette.
- **`extend`** preserves a truthful photographic action or scene field and creates a materially independent extension.
- **`reduction`** builds a complete original artwork around the essential source relationship, retaining enough specificity without reconstructing the full scene, tracing it, or collapsing into an empty icon.

Treat method names as selectors, not intensity commands. In particular, `reduction` means selective semantic and visual reduction: remove photographic description while preserving expressive information. Never interpret it as reducing image dimensions, resolution, or every visual layer.

If multiple results begin to resemble one another, restore method separation before polishing them.
