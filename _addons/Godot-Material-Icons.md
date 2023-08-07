---
permalink: /addons/material-icons
title: "Material Icons for Godot"
excerpt: "Add possible to use Material Icons Font in your Godot projects."
published: true
author_profile: true
author: "Jeremi Biernacki"
layout: single
header:
  teaser: assets/addons/material-icons.png
  overlay_image: assets/addons/material-icons.png
  caption: "2.0"
  actions:
    - label: "Download"
      url: "https://github.com/rakugoteam/Godot-Material-Icons/releases/latest"
---

# Godot-Material-Icons

- [repo](https://github.com/rakugoteam/Godot-Material-Icons)
- [download](https://github.com/rakugoteam/Godot-Material-Icons/releases)
- docs (WIP)

[*Templarian's Material-Design-Icons*](https://github.com/templarian/MaterialDesign) 
is a collection of icons for the [Material Design](https://material.io/) specification.

Now compatible with both Godot 3.4+ (version 1.x) and 4.0+ (version 2.x).

This addon provides the following nodes to use the icons in Godot:
- **MaterialIcon**: A node that displays an icon from the Material Design Icons collection.
- **MaterialButton**: A node that displays an icon from the Material Design Icons collection as a button (without label).

It's also adds **IconsFinder** to the Godot's **Tools** menu.
So you can find the icons easily.

![](/assets/addons/material-icons.png)

## Using it with RichTextLabel
From version 2.0 you can use the icons in RichTextLabel.
*I will backport this feature to version 1.x soon.*
[Example code of using the icons in RichTextLabel here](https://github.com/rakugoteam/Godot-Material-Icons/blob/godot-4/addons/material-design-icons/examples/LabelWithIcons.gd)

## Exporting
For emojis to work in exported projects, you need add `*.json` files to include files settings:
![include files settings](/assets/other/screenshot_export.png)

