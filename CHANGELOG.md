# Changelog

All notable changes to UIPilot are listed here, newest first.

## 1.0.0 (coming soon to the Unity Asset Store)

The first release.

**Build**

- **Build UI** creates a Main Menu, Pause Menu and Settings Menu in one click: canvas,
  EventSystem, panels, buttons, and a `UIPilot_GameManager.cs` script with every
  button wired to it.
- The menus work as a game front end out of the box: Play loads the scene you pick,
  Esc or Start pauses, Esc or B goes back, Quit asks once.
- Settings for volume, fullscreen and quality that work and are remembered.
- Keyboard, mouse and gamepad, with the Input Manager, the Input System, or both.
- Offers to import TextMeshPro's Essential Resources when a project has none.

**Look**

- Nine themes: Soft Club, Soft Club Night, Ink, Fantasy RPG, JRPG Window, Pixel Retro,
  Sci-Fi HUD, Military Shooter and Survival Horror.
- **Apply Theme to Existing Menus** restyles built menus without touching their layout
  or wiring.
- Your own picture behind the menu, or a theme's layered scene that changes with the
  time of day.
- **Restore Default Themes** brings back any of the nine that went missing.

**Checks**

- **UI Health** checks every UI in your open scenes, and every scene in a build, for
  broken click events, EventSystem problems, missing raycasters, blocked buttons,
  unreachable gamepad controls and text too small for Steam Deck. One-click, undoable fixes.
- **Click Debugger** shows what took each click in Play mode, and why.
- **Scan & Repair** audits and repairs UIPilot's own objects in one step.

**Compatibility**

- Unity 6.3 LTS (6000.3) or newer. Built-in Render Pipeline and URP.
