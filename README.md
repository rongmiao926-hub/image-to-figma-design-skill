# Image to Figma Design Skill

Codex skill for converting screenshots, reference images, wireframes, UI mockups,
webpage captures, or app screenshots into Figma-ready design specs and editable
layer plans.

## What It Does

- Checks that Figma MCP is connected before attempting direct Figma creation.
- Guides the user to connect or configure Figma MCP when the required tools are
  not available.
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
The skill uses `https://mcp.figma.com/mcp` as the Figma MCP endpoint when
configuration guidance is needed.

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
Use $image-to-figma-design to check Figma MCP access and turn this screenshot into a Figma-ready design spec.
```

When Figma write tools are available, Codex can create frames, layers,
components, variables, and assets directly in Figma. Otherwise, it will produce a
structured construction spec for manual implementation.

---

# Image to Figma Design Skill（中文版）

这是一个 Codex skill，用于把截图、参考图、线框图、UI mockup、网页截图或
App 截图转换成 Figma 可用的设计规格和可编辑图层方案。

## 功能

- 在尝试直接创建 Figma 文件前，先检查 Figma MCP 是否已经连通。
- 如果缺少必要工具，会引导用户连接或配置 Figma MCP。
- 分析源图片的画布尺寸、布局、字体、颜色、间距、素材和可见文案。
- 输出包含语义图层、组件、设计 token、素材、约束和校验说明的 Figma
  画板方案。
- 当 Figma 写入工具可用时，使用原生 Figma 对象创建画板、图层、组件、变量
  和素材。
- 对照片、复杂 logo、不可稳定矢量化的图形保留为位图素材，不强行描摹。

## 依赖

- Codex skills 支持。
- 如果需要直接创建或编辑 Figma 文件，需要可用的 Figma MCP。

仓库中的 `agents/openai.yaml` 已声明 Figma MCP 依赖。需要配置时，skill 会使用
`https://mcp.figma.com/mcp` 作为 Figma MCP endpoint。

## 安装

把仓库克隆到 Codex skills 目录：

```bash
git clone https://github.com/rongmiao926-hub/image-to-figma-design-skill.git \
  "$CODEX_HOME/skills/image-to-figma-design"
```

如果没有设置 `CODEX_HOME`，通常可以使用默认目录：

```bash
~/.codex/skills/image-to-figma-design
```

## 使用方式

把图片或截图发给 Codex，并要求使用该 skill：

```text
Use $image-to-figma-design to check Figma MCP access and turn this screenshot into a Figma-ready design spec.
```

当 Figma 写入工具可用时，Codex 可以直接在 Figma 中创建画板、图层、组件、
变量和素材。否则，它会输出结构化的 Figma 搭建规格，供手动实现。
