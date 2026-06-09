---
name: image-to-figma-design
description: Use when converting screenshots, reference images, wireframes, UI mockups, webpage captures, or app screenshots into Figma-ready design specs, editable layer plans, component inventories, or recreation guidance.
---

# Image to Figma Design

## Overview

Turn a source image into an editable Figma design plan. Prefer semantic Figma layers, auto layout, components, and tokens over pixel tracing; use bitmap crops only for photography, complex logos, or non-reconstructable artwork.

## Required Flow

1. **Confirm inputs**
   - Identify every source image path, URL, screenshot, or attachment.
   - If the image is missing, ask for it before proceeding.
   - Clarify only high-impact unknowns: target canvas size, desktop/mobile breakpoint, or whether exact pixel parity is required.

2. **Inspect the image**
   - Use visual tools for local images and screenshots.
   - Record canvas dimensions, main regions, grid, spacing rhythm, typography, colors, icons, imagery, elevation, borders, and interaction states visible in the image.
   - Preserve visible copy exactly. Mark unreadable text as `[unreadable]` instead of inventing content.

3. **Choose the build path**
   - If a callable Figma write/create API is available, create frames, layers, components, variables, and assets directly in Figma.
   - If only read-only Figma tools are available, say so and deliver a Figma construction spec plus assets or an optional HTML/CSS visual preview. Do not claim a Figma file was created.
   - Keep the original image as a locked reference layer only when working inside Figma; do not use it as the final design background.

4. **Decompose into editable Figma objects**
   - Root frame: exact size, background, layout grid, safe area, breakpoint behavior.
   - Regions: header, navigation, content, panels, modals, lists, cards, forms, controls, and footer.
   - Components: buttons, inputs, tabs, menus, badges, list rows, cards, icons, empty/loading/error states when visible or naturally implied.
   - Tokens: color, typography, spacing, radius, border, shadow, opacity, and image treatment.
   - Constraints: resizing rules and auto-layout direction, gap, padding, alignment, wrapping, and fixed vs hug/fill sizing.

5. **Verify**
   - Compare the recreated output or spec against the source image.
   - Call out material deviations, inferred values, missing fonts/assets, and any text that could not be read.
   - For exact recreations, make a screenshot of the result and iterate until layout, proportions, and visual hierarchy match.

## Deliverable Template

Use this structure unless the user asks for a different artifact:

```markdown
## Source
- File/URL:
- Canvas:
- Goal:

## Figma Frame Plan
| Layer | Type | X | Y | W | H | Layout/Constraints | Style |
| --- | --- | ---: | ---: | ---: | ---: | --- | --- |

## Tokens
- Colors:
- Typography:
- Spacing:
- Radius/borders:
- Effects:

## Components
- Component name: variants, states, key properties

## Assets
- Asset name: crop/vector/source, intended Figma usage

## Build Notes
- Auto layout:
- Responsive behavior:
- Inferred values:

## Verification
- Matches:
- Deviations:
- Open questions:
```

## Quality Rules

- Use native text and vector shapes whenever possible.
- Name layers semantically, not by visual appearance alone.
- Infer fonts conservatively and label font guesses as inferred.
- Convert repeated visual patterns into components or variants.
- Keep dimensions numeric and concrete; avoid vague instructions such as "about the same size."
- If the user asks for "image to Figma" but no Figma-write capability exists, produce the best Figma-ready handoff and explain the limitation in one sentence.
