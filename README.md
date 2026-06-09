# Image to Figma Design Skill

Codex skill for converting screenshots, reference images, wireframes, UI mockups,
webpage captures, or app screenshots into Figma-ready design specs and editable
layer plans.

## What It Does

- Inspects source images and records canvas size, layout, typography, color,
  spacing, assets, and visible copy.
- Produces a Figma frame plan with semantic layers, components, tokens, assets,
  constraints, and verification notes.
- Uses native Figma objects when write access is available.
- Keeps complex photos, logos, and non-reconstructable artwork as bitmap assets
  instead of tracing them.

## Requirements

- Codex skills support.
- Figma MCP access if you want direct Figma file creation or editing.

The bundled `agents/openai.yaml` declares the Figma MCP dependency.

## Install

Clone this repository into your Codex skills directory:

```bash
git clone https://github.com/rongmiao926-hub/image-to-figma-design-skill.git \
  "$CODEX_HOME/skills/image-to-figma-design"
```

If `CODEX_HOME` is not set, the default is usually:

```bash
~/.codex/skills/image-to-figma-design
```

## Usage

Ask Codex to use the skill with an image or screenshot:

```text
Use $image-to-figma-design to turn this screenshot into a Figma-ready design spec.
```

When Figma write tools are available, Codex can create frames, layers,
components, variables, and assets directly in Figma. Otherwise, it will produce a
structured construction spec for manual implementation.
