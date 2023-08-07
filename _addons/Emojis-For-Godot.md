---
permalink: /addons/emojis-for-godot
title: "Emojis for Godot"
excerpt: "Make possible to use emojis in your Godot projects."
published: true
author_profile: true
author: "Jeremi Biernacki"
layout: single
header:
  teaser: assets/addons/emojis.png
  overlay_image: assets/addons/emojis.png
  caption: "2.0"
  actions:
    - label: "Download"
      url: "https://github.com/rakugoteam/Emojis-For-Godot/releases/latest"
---

# Emojis for Godot

- [repo](https://github.com/rakugoteam/Emojis-For-Godot)
- [download](https://github.com/rakugoteam/Emojis-For-Godot/releases)
- docs (WIP)

Emoji mode use [Twemoji](https://twemoji.twitter.com/).

Now compatible with both Godot 3.4+ (version 1.x) and 4.0+ (version 2.x).

This addon provides the following nodes to use emojis in Godot:
- **EmojiIcon**: A node that displays an Emoji.
- **EmojiButton**: A node that displays an Emoji as a button.

It's also adds **EmojiFinder** to the Godot editor's toolbar.
So you can find the emojis easily.

![EmojiFinder Screen Shot](/assets/addons/emojis.png)

## Using it with RichTextLabel

From version 1.3 you can use emojis in RichTextLabel.

This is the example code of using emojis in RichTextLabel:
- [Godot 3.4+ (version 1.x)](https://github.com/rakugoteam/Emojis-For-Godot/blob/godot-3/addons/emojis-for-godot/examples/LabelWithEmojis.gd)
- [Godot 4.0+ (version 2.x)](https://github.com/rakugoteam/Emojis-For-Godot/blob/godot-4/addons/emojis-for-godot/examples/LabelWithEmojis.gd)

This is the result of the above code:

![RichTextLabel Example Screen Shot](/assets/addons/emojis_rtl.png)

## Exporting
For emojis to work in exported projects, you need add `*.json` files to include files settings:
![include files settings](/assets/other/screenshot_export.png)

[**TexturePacker**](https://www.codeandweb.com/texturepacker) is used to generate the emoji atlases.


