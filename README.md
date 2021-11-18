# Escoria Simple dialog

![Escoria Logo](https://raw.githubusercontent.com/godot-escoria/escoria-demo-game/main/addons/escoria-core/design/escoria-logo-small.png)

[![Join our Discord](https://img.shields.io/discord/884336424780984330.svg?label=Join%20our%20Discord&logo=Discord&colorB=7289da&style=for-the-badge)](https://discord.com/invite/jMxJjuBY5Z)

Libre framework for the creation of point-and-click adventure games with the multi-platform game engine [Godot Engine](https://godotengine.org).

It is designed to be extended with the specific requirements for your game.

Check out the [Escoria documentation](https://docs.escoria-framework.org) for 
further details.

## Simple Dialog Manager

This is the stock [dialog manager](https://docs.escoria-framework.org/en/devel/advanced/create_dialog_manager.html) 
addon for Escoria. It supports the following view types:

* floating: The text is displayed near the character speaking (LucasArts-Style)
* avatar: The text is displayed in a panel with an optional Avatar (Sierra-Style)

It is meant to be an example implementation of the dialog manager, so that 
developers can use it as a basis for their own dialog manager implementation.

It is fully functional and is a good choice for prototype or jam games, though.

## Dialog position for the floating type

The floating type expects the character node to have a Position2D child node 
named "dialog_position". It will display the dialog at that position.

If the current room has no character, the text will be shown in the middle of
the screen.

## Configuration

The addon supports some basic configuration in its own project settings 
subcategory under the "Escoria" category:

* Avatars Path: Path in which avatar textures named like the global id of the 
  character are stored.
* Text Speed Per Character: In both types, the dialog lines are displayed 
  character by character. This setting controls the speed with which they are
  revealed
* Fast Text Speed Per Character: If the dialog is sped up (the player clicked
  twice), this is the speed by which the characters are displayed
* Max Time To Disappear: After all characters are displayed, the dialog waits
  this amount of seconds before disappearing
