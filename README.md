# Escoria Simple Dialog

![Escoria Logo](https://raw.githubusercontent.com/godot-escoria/escoria-demo-game/main/addons/escoria-core/design/escoria-logo-small.png)

[![Join our Discord](https://img.shields.io/discord/884336424780984330.svg?label=Join%20our%20Discord&logo=Discord&colorB=7289da&style=for-the-badge)](https://discord.com/invite/jMxJjuBY5Z)

Libre framework for the creation of point-and-click adventure games with the multi-platform game engine [Godot Engine](https://godotengine.org).

It is designed to be extended with the specific requirements for your game.

Check out the [Escoria documentation](https://docs.escoria-framework.org) for 
further details.

## Simple Dialog Manager

This is the stock [dialog manager](https://docs.escoria-framework.org/en/devel/advanced/create_dialog_manager.html) 
addon for Escoria. It supports the following view types:

* floating: Dialog text is displayed near the character speaking (LucasArts-Style)
* avatar: Dialog text is displayed in a panel with an optional Avatar (Sierra-Style)

This addon is meant to be an example implementation of the dialog manager so that
developers can use it as a basis for their own dialog manager implementations.

The stock dialog manager is fully functional and is a good choice for prototypes and
jam games.

## Dialog position for the 'floating' view type

The floating view type expects the character scene to have a Position2D child node
named "dialog_position". Any dialog text for the character will be displayed at the
position indicated by this Position2D node.

If the current room has no character, any dialog text will be shown in the middle
of the screen.

## Configuration

The addon supports some basic configuration in its own project settings 
subcategory under the "Escoria" category:

* **Avatars Path**: Path in which avatar textures with the same name as the global
  IDs of the characters are stored.
* **Text Speed Per Character**: In both view types, the dialog lines are displayed 
  character by character. This setting controls the speed with which they are
  revealed.
* **Fast Text Speed Per Character**: If the dialog is sped up (the player clicked
  twice), this is the speed at which the characters are displayed.
* **Max Time To Disappear**: After all characters in a line of dialog are displayed,
  the text disappears after the amount of time specified by this setting
  (in seconds).
