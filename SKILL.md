---
name: photo-alchemy
description: "Transform ordinary supplied photographs into distinctive, source-aware raster artworks through one or more selectable methods: abstraction, extend, and reduction. Use when the user wants to elevate a photo into art, requests an artistic reinterpretation, names one supported method, or wants to compare several methods without copying a fixed reference style."
---

# Photo Alchemy

Create one or more finished artworks from a photograph. Let the user choose a method, request several, or ask the skill to select the most suitable direction. When generating more than one, share only the source analysis; do not share layouts, edge treatments, mark systems, or style shortcuts between methods.

## Core workflow

1. Inspect the photograph and build a compact Scene Card:
   - core subject or event;
   - dominant axis, gesture, gaze, rhythm, or movement;
   - key spatial relationship and visual-weight map;
   - native palette and meaningful minor accent;
   - semantic minimum that must survive;
   - descriptive detail that should disappear.
2. Read [references/branches.md](references/branches.md), select the requested or most suitable method, and compile a separate contract for each selected method.
3. Choose the output ratio from the source orientation and composition. Never force a preset poster ratio.
4. Generate each selected method from the original photograph only. Do not use another artist's output or a prior result as a visual reference unless the user explicitly supplies it for that purpose.
5. Read [references/review.md](references/review.md). Inspect each result at normal and thumbnail scale.
6. Regenerate at most once per branch, and only for a concrete failure. State the correction and freeze everything else.
7. Save every requested raster file and return it with a concise method-specific rationale.

## Shared constraints

- Preserve relationships before surface detail.
- Keep each visible element traceable to a source fact or a necessary compositional function.
- Use a single meaningful accent hue when the source supports one; never add detached color decoration.
- Treat an internal working title as a disposable semantic check, not a reusable prompt constant. Derive it from the current photo, do not render it unless requested, and never reuse a prior image's title.
- Avoid oil-paint styling, generic vintage decoration, arbitrary marks, logos, watermarks, fabricated metadata, and promotional text.

## Branch independence

- **`abstraction`** communicates the dominant perceptual event without retaining photo pixels or copying the original silhouette.
- **`extend`** preserves a truthful photographic action or scene field and creates a materially independent extension.
- **`reduction`** redraws the semantic scene completely, retaining enough structure to remain specific without becoming either a trace or an empty icon.

Treat method names as selectors, not intensity commands. In particular, `reduction` means selective semantic and visual reduction: remove photographic description while preserving expressive information. Never interpret it as reducing image dimensions, resolution, or every visual layer.

If multiple results begin to resemble one another, restore method separation before polishing them.
