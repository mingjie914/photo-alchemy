# Photo Alchemy

[简体中文](./README.zh-CN.md)

### Find the artwork already latent in the photograph.

A photograph carries more than its visible subjects. It holds intervals, direction, visual weight, color memory, and relationships that may not yet have found their final form.

Photo Alchemy reads those latent structures and rebuilds them as an original artwork. It is not a preset filter, a fixed house style, or a mechanical trace. The source remains the reason for every decision, while the finished work is free to become something of its own.

*Created and art-directed by **少年老程***

## Selected works

The works below are finished `extend` examples. They are not layout recipes: each begins with a different source relationship and allows the photographic truth to meet a newly constructed material field.

### Gesture against the field

| A turn gathers the surrounding snow into pressure and direction. | A small rider gives scale to an otherwise open field. |
| :---: | :---: |
| ![Snowboarder turning through a layered abstract snow field](examples/snowboard-turn-extend.png) | ![Snowboarder crossing an open snow field extended by sparse horizontal marks](examples/snowboarder-open-snowfield-extend.png) |

### Passage within a frame

| The passenger becomes the quiet center of a layered interior. | Street, wires, traffic, and dusk are compressed into a single passage. |
| :---: | :---: |
| ![White dog inside a car framed by pale green and charcoal material layers](examples/white-dog-passenger-extend.png) | ![Dusk street and overhead wires held inside a converging paper corridor](examples/city-dusk-corridor-extend.png) |

### Light as structure

| A narrow beam opens a resting place inside dense green. | The tower's upward pull continues into color, material, and sky. |
| :---: | :---: |
| ![Seated figure in a forest framed by layered green forms and sunlight](examples/sunlit-forest-bench-extend.png) | ![Red broadcast tower extended through blue white and red material fields](examples/red-broadcast-tower-extend.png) |

These examples show one current path, not the visual limit of the Skill. `abstraction` and `reduction` follow different image logic and do not inherit the collage language shown here.

## Current creative paths

Photo Alchemy is one creative system. Its methods are different routes through the same source, not a fixed bundle of three outputs.

| Method | Source pixels in the result | Creative purpose |
| --- | --- | --- |
| `abstraction` | No | Translate the dominant perceptual event into a complete abstract artwork. Recognizability may dissolve into rhythm, pressure, interval, mass, and color. |
| `extend` | Yes | Preserve a truthful photographic field and let an independent material language continue, counterbalance, or reframe it. |
| `reduction` | No | Reconstruct the scene around its essential source relationship while releasing incidental description. |

`reduction` is a method name, not an instruction to lower resolution or strip every visual layer.

If no method is named, the Skill chooses from the strongest evidence in the photograph: indispensable photographic truth suggests `extend`, a dominant perceptual event suggests `abstraction`, and a source-specific relationship that can survive redraw suggests `reduction`.

## From source to artwork

The process is consistent without becoming a template:

1. **Read the relation** — identify the subject, interval, direction, weight, or tension that governs how the image is seen.
2. **Set the intention** — decide what must remain, what may loosen, and what the new work should make more present.
3. **Recompose the field** — choose a method and rebuild form, color, material, scale, and quiet space around that intention.
4. **Resolve the work** — review semantic integrity, visual hierarchy, method separation, and visible defects; correct only a concrete failure.

The internal Scene Card, Method Brief, prompt compiler, and review gates support this process without imposing a fixed ratio, paper treatment, title system, or house palette.

## Start creating

### Requirements

The host environment needs:

- image input and visual inspection;
- reference-image-aware raster generation or editing;
- access to the bundled `references/` files;
- permission to save and return generated images.

Image quality and source preservation still depend on the model available in the host environment.

### Install for Codex

Windows PowerShell:

```powershell
git clone https://github.com/mingjie914/photo-alchemy.git `
  "$env:USERPROFILE\.codex\skills\photo-alchemy"
```

macOS or Linux:

```bash
git clone https://github.com/mingjie914/photo-alchemy.git \
  ~/.codex/skills/photo-alchemy
```

Start a new task after installation so Codex can discover the Skill.

If you keep a separate development checkout, copy the complete repository folder into the Skills directory only when you want to test that revision. Do not merge two independently edited copies.

### Update

For a clean Git installation on Windows:

```powershell
git -C "$env:USERPROFILE\.codex\skills\photo-alchemy" pull --ff-only
```

For macOS or Linux:

```bash
git -C ~/.codex/skills/photo-alchemy pull --ff-only
```

If the installed copy contains local edits, compare or preserve them before updating. Do not overwrite them blindly.

### Use

Supply one photograph and choose a path:

```text
$photo-alchemy method=abstraction
$photo-alchemy method=extend
$photo-alchemy method=reduction
```

Natural-language requests are equally valid:

```text
Use $photo-alchemy to create an abstraction from this photograph.
Use $photo-alchemy to extend this photograph into an original material composition.
Use $photo-alchemy to create a reduction that preserves its defining relationship.
```

During development or comparison, request all methods explicitly:

```text
$photo-alchemy method=all
```

### Other Agent platforms

The creative workflow is carried by the portable `SKILL.md` and relative `references/` files. Agent Skills-compatible platforms may import the folder or a ZIP package according to their own installation process. `agents/openai.yaml` contains OpenAI-specific interface metadata and may be ignored elsewhere.

## What the Skill returns

Each selected method returns:

- one finished raster image identified by method;
- a concise one- or two-sentence artistic rationale in the user's language.

The Scene Card, Method Brief, and compiled generation prompt remain internal unless requested. The generated artwork itself adds no title, typography, credits, attribution, metadata, watermark, or promotional text unless the user explicitly asks for that content.

## Creative boundaries

- Preserve relationships before surface detail.
- Derive composition, color, rhythm, and supporting marks from the supplied photograph.
- Keep the methods visually and materially independent.
- Avoid fixed layouts, copied visual signatures, generic AI-painterly styling, hard-coded titles, and decorative filler.
- Generate every selected method from the original photograph, never from another method's result.
- Review at normal and thumbnail size, then make at most one targeted correction for a concrete failure.

The aim is not to make every photograph grand. It is to uncover the relation that makes this photograph singular.

## Creator

Photo Alchemy is created and art-directed by **少年老程**. It is an ongoing exploration of how computational image-making can begin with attention, relationship, and visual judgment rather than a preset look.

## Source handling

The supplied photograph is used only for the requested generation. The Skill does not browse for it, publish it, add it to the repository, or reuse it in another task unless the user asks. A host platform may still send the image to its configured image-generation service, so that service's privacy and data terms also apply.

## Commercial-use policy

Artwork generated with this Skill is intended for personal, educational, research, and non-commercial use unless the relevant rights holder grants separate permission.

- No commercial-use permission is granted for project-owned demonstration images or artworks distributed with this project.
- Rights in user-supplied photographs remain with their respective rights holders.
- Users must also follow the terms of the model or image-generation service used by the host platform.
- A source-code license does not override photograph, privacy, publicity, trademark, or artwork rights.

This project currently does not use a separate `LICENSE` file. Unless the relevant rights holder grants explicit permission, the repository does not grant rights for commercial use, sale, sublicensing, or commercial redistribution.

## Repository structure

```text
photo-alchemy/
├── README.md
├── README.zh-CN.md
├── SKILL.md
├── agents/
│   └── openai.yaml
├── examples/
│   └── selected finished artworks
└── references/
    ├── branches.md
    ├── prompt-compiler.md
    └── review.md
```

- `SKILL.md`: triggers, shared workflow, and method separation.
- `references/branches.md`: method-specific creative contracts.
- `references/prompt-compiler.md`: the shared prompt contract and method-specific material boundaries.
- `references/review.md`: quality gates and targeted-correction rules.
- `examples/`: project-owned finished artworks selected to demonstrate current behavior.
- `agents/openai.yaml`: OpenAI interface metadata.
