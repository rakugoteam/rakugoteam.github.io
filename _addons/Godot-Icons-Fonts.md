---
permalink: /addons/icons-fonts
title: "Icons Fonts for Godot"
excerpt: "Add possible to use Icons Font in your Godot projects."
published: true
author_profile: true
author: "Jeremi Biernacki"
layout: single
header:
  teaser: assets/font-icons/mi-docked.png
  overlay_image: assets/font-icons/mi-docked.png
  caption: "1.2.4"
  actions:
    - label: "Download"
      url: "https://github.com/rakugoteam/Godot-Icons-Fonts/releases/latest"
---

![github-top-lang][lang] ![lic] ![lic-font]

![](icon.png)

# Godot Icons Fonts

***Compatible with Godot 4.1+***

Makes easy to find and use icons from popular icon-fonts in your Godot project.

## What problems it solves:

### You only needs this addon - as you don't have:
1. to go online find font
1. then find icon
1. check icon licence - and maybe you need to search for another
1. finally download it

### Better alterative to Godot's build emojis as
- to use them you need to find unicode online
- they don't work on some platforms for example Web
- they are outdated

## Included

### Dependencies
- [Rakugo Nodes](https://github.com/Jeremi360/Rakugo-Nodes)

### Icons Fonts
- [*Templarian's Material-Design-Icons*](https://github.com/templarian/MaterialDesign), </br>
	a collection of icons for the [Material Design](https://material.io/) specification.
- [Google Noto Emojis Color font][noto-emoji]
<!-- feature versions: -->
<!-- - [game-icons.net](https://github.com/toddfast/game-icons-net-font) -->
<!-- - godot-icons -->

*Material-Design-Icons*
![](/assets/font-icons/mi-docked.png)

*Noto-Emojis*
![](/assets/font-icons/emojis-docked.png)

<!-- todo add link to docs when they are ready -->

### Resource
**FontIconSetting** - Resource for setting which and how to display FontIcon.

![](/assets/font-icons/font-icon-settings.png)

### Nodes
- **FontIcon**: Control Node that displays IconFont.
- **FontIconButton**: Button* That have IconFont and can have label.
- **FontIconCheckButton**: CheckButton* That have IconFont and can have label.

\* - Those nodes behaves like button,
but they don't extends from **Button**.

*FontIcon*
![](/assets/font-icons/mi-font-icon.png)

*FontIconButton*
![](/assets/font-icons/emoji-button.png)

*FontIconCheckButton*
![](/assets/font-icons/mi-check-button.png)

### Singleton
**IconsFonts** is singleton for easier use of icons anywhere in your project.

## In Editor
It's adds **IconsFinder** (docked to bottom by default).
So you can find the icons easily, click on icon to get its name to clipboard.
It can be in dock mode at bottom or in window mode.

That can be switched in Godot's **Tools** menu.
![](/assets/font-icons/menu-tools.png)

Or using *Command Pallet* (`Ctrl+Shift+P`)
![](/assets/font-icons/command-pallet.png)

*docked mode*
![](/assets/font-icons/mi-docked.png)

*window mode*
![](/assets/font-icons/emojis-window.png)

## Using it with RichTextLabel
You can use the icons in RichTextLabel.

![](/assets/font-icons/rich-text-icons.png)

```gdscript
@tool
extends RichTextLabel

@export_multiline
var text_with_icons: String:
	set(value):
		if !is_node_ready(): await ready
		text_with_icons = value
		bbcode_enabled = true
		text = IconsFonts.parse_text(value)

	get: return text_with_icons

func _ready():
	bbcode_enabled = true
	text = IconsFonts.parse_text(text_with_icons)
```

## Exporting
For emojis to work in exported projects,
you need add `*.json` files to include files settings:
![](/assets/font-icons/export.png)

## Know Issues
- Window mode is init with empty icons render*

\**To fix just change back-and-forward to icon font you want to use.*

## Compatibility
This addon is replacing our previous to addons:
- [Godot Material Icons](https://github.com/rakugoteam/Godot-Material-Icons)
- [Emojis For Godot](https://github.com/rakugoteam/Emojis-For-Godot)

We had broken backward compatibility with them for those reasons:
- In feature we want to support more IconsFonts so we can use `[icon:icons-name]` in text parsing.
- We redesigned how addon works under the hood
- We had too rename nodes

[lic]: https://img.shields.io/github/license/rakugoteam/Godot-Icons-Fonts?style=flat-square&label=📃%20License&
[lang]: https://img.shields.io/github/languages/top/rakugoteam/Godot-Icons-Fonts?style=flat-square
[lic-font]:https://img.shields.io/static/v1.svg?label=📜%20Font%20License&message=Pictogrammers%20Free%20License&color=informational&style=flat-square
[noto-emoji]:https://github.com/googlefonts/noto-emoji/tree/main/png

