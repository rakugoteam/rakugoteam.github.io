---
permalink: /addons/emojis-for-godot
title: "Emojis for Godot"
excerpt: "Make possible to use emojis in your Godot projects."
published: true
author_profile: true
author: "Jeremi Biernacki"
layout: single
header:
  teaser: https://github.com/rakugoteam/Emojis-For-Godot/raw/godot-4/.assets/addon-in-action.png
  overlay_image: https://github.com/rakugoteam/Emojis-For-Godot/raw/godot-4/.assets/addon-in-action.png
  caption: "2.1"
  actions:
    - label: "Download"
      url: "https://github.com/rakugoteam/Emojis-For-Godot/releases/latest"
---

# Emojis for Godot

- [repo](https://github.com/rakugoteam/Emojis-For-Godot)
- [download](https://github.com/rakugoteam/Emojis-For-Godot/releases)
- docs (WIP)

![addon-in-action]

## Important! Upgrading from 2.0 to 2.1

As 2.1 version use font instead of texture atlas in doesn't need so many files.
So to Upgrade in correct way you should:
1. out side of godot
2. remove 2.0 version form *addons/* dir
3. put 2.1  version into *addons/* dir
4. happy using new addon version

## Now compatible with emojis Unicode 15.1

Version 2.1 (Godot 4.x):
- is compatible with emojis Unicode 15.1
- uses [Google Noto Emojis Color font][noto-emoji]
- uses [json data generated using python][emoji-json]

This addon provides the following nodes to use emojis in Godot:
- **EmojiIcon**: A node that displays an Emoji.
- **EmojiButton**: A node that displays an Emoji as a button.

Version 2.x is rewritten to give you access to **EmojisDB** singleton for easier use of emojis anywhere in your project.

It's also adds **EmojiFinder** to the Godot's *Project > Tools* menu.
So you can find the emojis easily.

![EmojiFinder Screen Shot][emoji-finder-screenshot]

## Using it with RichTextLabel
This is the example code of using emojis in RichTextLabel:
```gdscript
@tool
extends RichTextLabel

@export_multiline
var text_with_emojis: String:
	set(value):
		if !is_node_ready():
			return

		text_with_emojis = value
		bbcode_enabled = true
		text = EmojisDB.parse_emojis(value)
	
	get: return text_with_emojis

func _ready() -> void:
	if !Engine.is_editor_hint():
		bbcode_enabled = true
		text = EmojisDB.parse_emojis(text_with_emojis)
```

This is the result of the above code:

![RichTextLabel Example Screen Shot][LabelWithEmojis-screenshot]

## Exporting
For emojis to work in exported projects, you need add `*.json` files to include files settings:
![include files settings][export-screenshot]

[addon-in-action]:https://github.com/rakugoteam/Emojis-For-Godot/raw/godot-4/.assets/addon-in-action.png
[noto-emoji]:https://github.com/googlefonts/noto-emoji/tree/main/png
[emoji-json]:https://github.com/rakugoteam/Emojis-For-Godot/tree/godot-4/addons/emojis-for-godot/emojis/gen_json.py
[emoji-finder-screenshot]:https://github.com/rakugoteam/Emojis-For-Godot/raw/godot-4/.assets/emoji-finder.png
[LabelWithEmojis-screenshot]:https://github.com/rakugoteam/Emojis-For-Godot/raw/godot-4/.assets/label-with-emojis.png
[export-screenshot]:https://github.com/rakugoteam/Emojis-For-Godot/raw/godot-4/.assets/export.png


