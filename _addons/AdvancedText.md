---
permalink: /addons/advanced-text
title: "Advanced Text"
excerpt: "Extends RichTextLabel, adds support for Markdown, RenPy and much more."
published: true
author_profile: true
author: "Jeremi Biernacki"
layout: single
header:
  teaser: images/AdvancedText.gif
  overlay_image: images/AdvancedText.gif
  caption: "3.0.1-docs"
  actions:
    - label: "Download"
      url: "https://github.com/rakugoteam/AdvancedText/releases/latest"
---

- [🌳 repo](https://github.com/rakugoteam/AdvancedText)
- [⬇️ download](https://github.com/rakugoteam/AdvancedText/releases/latest)
<!-- - [📚 docs](https://rakugoteam.github.io/advanced-text-docs/2.0/) -->

Extends RichTextLabel and adds support for Markdown and RenPy
Soon there will be docs for most of the features.

## Features

- Supports Markdown and RenPy
- Variables use RakuVars `<var>` in Markdown, Ren'Py Markup and BBCode
- Adds headers supports RenPy and BBCode
- Support [Godot-Icons-Fonts](/addons/icons-fonts)

### Nodes

- **AdvancedTextLabel** - A label that supports Markdown and RenPy

### Resources

- **TextParser** - base class for our TextParsers
- **ExtendedBBCodeParser**:
  - base of for our Ren'Py Markup and Markdown parsers
  - includes support for things mentioned in [Features](#features)
- **RenPyMarkup** - RenPy Markup Parser with extra tags so it is 100% replaceable with Godot's BBCode
- **MarkdownParser** - Markdown Parser with extra stuff so it is mostly replaceable with Godot's BBCode
