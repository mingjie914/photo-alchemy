# Photo Alchemy

[简体中文](./README.zh-CN.md)

Most photographs preserve what was seen. Some also hold a gesture, an interval, a color memory, or a tension that has not yet found its final form.

Photo Alchemy looks for that latent character and turns an ordinary photograph into something singular. It does not disguise the source with a preset style. It reinterprets the relationships already inside the image so the familiar can be seen again—and no longer feel ordinary.

It is an Agent Skill for source-aware artistic reinterpretation rather than a filter, fixed style preset, or literal trace.

## One photograph, three ways of seeing

- `abstraction` asks what remains when recognizable forms loosen and the image becomes rhythm, force, interval, and color.
- `extend` asks where the photograph wants to continue beyond its existing boundary.
- `reduction` asks what becomes clearer when incidental description falls away and the essential relationship remains.

## Methods at a glance

| Method | Source pixels in the result | Purpose |
| --- | --- | --- |
| `abstraction` | No | Translate the dominant perceptual event into a complete abstract artwork. |
| `extend` | Yes | Preserve a truthful photographic field and extend it through an independent material language. |
| `reduction` | No | Redraw the scene through selective semantic and visual reduction while retaining expressive structure. |

`reduction` is a method name, not an instruction to lower resolution or minimize every visual layer.

## Design principles

- Preserve relationships before surface detail.
- Derive composition, color, rhythm, and supporting marks from the supplied photograph.
- Keep the three methods visually and materially independent.
- Avoid fixed layouts, copied visual signatures, hard-coded titles, and decorative filler. Do not add or fabricate logos, watermarks, credits, metadata, or promotional text; existing marks inside a truthful `extend` anchor remain source pixels.
- Review each result at normal and thumbnail size, then make at most one targeted correction for a concrete failure.

## Installation

### Codex

Copy the complete `photo-alchemy` folder to a Codex skills directory:

```text
~/.codex/skills/photo-alchemy/
```

On Windows, the usual location is:

```text
%USERPROFILE%\.codex\skills\photo-alchemy\
```

Start a new task after installation so the Skill can be discovered.

### Other Agent platforms

The core workflow uses the portable `SKILL.md` plus relative `references/` files. Agent Skills-compatible platforms may import the folder or a ZIP package according to their own installation process. The host must provide:

- image input and visual analysis;
- reference-image-aware raster generation or editing;
- access to the bundled reference files;
- permission to save and return generated images.

`agents/openai.yaml` contains OpenAI-specific interface metadata and may be ignored by other platforms.

## Usage

Supply one photograph, then choose a method:

```text
$photo-alchemy method=abstraction
$photo-alchemy method=extend
$photo-alchemy method=reduction
```

Natural-language requests are also valid:

```text
Use $photo-alchemy to create an abstraction from this photo.
Use $photo-alchemy to extend this photo into an original material composition.
Use $photo-alchemy to create a reduction while preserving the action and atmosphere.
```

During development or comparison, request all methods explicitly:

```text
$photo-alchemy method=all
```

Without a method, the Skill may select the direction that best serves the photograph.

## Workflow and output

The Skill:

1. identifies the essential source relationship, decisive visual facts, visual weight, quiet areas, source anchors, palette opportunities, and removable detail;
2. resolves a compact method-specific brief for `abstraction`, `extend`, or `reduction`;
3. compiles the brief into a three-part image prompt covering proposition, method construction, and color/reproduction boundaries;
4. chooses an adaptive output ratio from the source composition;
5. generates from the original photograph rather than another method's result;
6. checks semantic integrity, composition, method separation, and visible defects;
7. returns the finished raster image with a concise method-specific rationale.

Each selected method produces one finished raster identified by method, plus a one- or two-sentence rationale in the user's language. The Scene Card, Method Brief, and full generation prompt remain internal unless requested. The Skill adds no title, typography, credits, attribution, metadata, or promotional text unless the user explicitly asks for that content.

The aim is not to make every photograph grand. It is to find the overlooked relationship that makes this photograph singular.

## Source handling

The supplied photograph is used only for the requested generation. The Skill does not browse for it, publish it, add it to the repository, or reuse it in another task unless the user asks. A host platform may still send the image to its configured image-generation service, so that service's privacy and data terms also apply.

## Commercial-use policy

Artwork generated with this Skill is intended for personal, educational, research, and non-commercial use unless the relevant rights holder grants separate permission.

- No commercial-use permission is granted for project-owned demonstration images or artworks distributed with this project.
- Rights in user-supplied photographs remain with their respective rights holders.
- Users must also follow the terms of the model or image-generation service used by the host platform.
- A source-code license does not override photograph, privacy, publicity, trademark, or artwork rights.

This project currently does not use a separate `LICENSE` file. Unless the relevant rights holder grants explicit permission, the repository does not grant rights for commercial use, sale, sublicensing, or commercial redistribution.

## Structure

```text
photo-alchemy/
├── README.md
├── README.zh-CN.md
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── branches.md
    ├── prompt-compiler.md
    └── review.md
```

- `SKILL.md`: triggers, shared workflow, and method separation.
- `references/branches.md`: method-specific creative contracts.
- `references/prompt-compiler.md`: the shared three-part prompt contract and method-specific material boundaries.
- `references/review.md`: quality gates and targeted-correction rules.
- `agents/openai.yaml`: OpenAI interface metadata.
