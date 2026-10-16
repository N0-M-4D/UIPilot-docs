# Troubleshooting

| What you see | Why | What to do |
|---|---|---|
| UIPilot asks to import TextMeshPro Essentials, or menu text is invisible | TMP Essential Resources are not imported. | Click **Import**, wait for it to finish, then click **Build UI** again. If text was already built without them, **Quick Clear** first. |
| "Waiting for Unity to compile..." and nothing more, or a red *Stalled* row | Another script in your project has a compile error. | Fix the errors in the Console. The buttons are wired after the next successful compile. |
| "UIPilot_GameManager type could not be resolved" | The generated script is inside a folder with an Assembly Definition. | Keep `UIPilot_GameManager.cs` directly under `Assets/`, then click **Build UI** again. |
| Buttons do not react in Play mode | Usually something [UI Health](ui-health.md) checks for: a wrong input module, a missing raycaster, something covering the buttons. | Look at UI Health and click **Fix**. Still stuck? Click the button in Play mode and read the [Click Debugger](click-debugger.md). |
| The UI Health lamp is not on the main toolbar | Unity hides toolbar items that packages add. | Right-click an empty part of the main toolbar and tick **UIPilot → UI Health**. |
| **Esc** does not open the pause menu | The main menu is showing, or the scene has no pause menu. | Press **Play** first. If there is no pause menu, tick **Pause Menu** and click **Build UI**. |
| Gamepad **Start** does not pause | The project uses the old Input Manager only. | Install the Input System package and set **Active Input Handling** to *Both*. |
| **Play** only writes a warning | The scene picked under **Play loads** is not in the scene list. | Add it in **File → Build Profiles**, or pick another scene. |
| After updating UIPilot, the menus still have the old look | Complete panels are never rebuilt, to protect your edits. | **Quick Clear**, then **Build UI**. |
| Scan says an object is missing, but it is in the scene | The object was renamed. | Restore its `UIPilot_...` name. |

Not listed here? [Open an issue](../../../issues/new/choose) with your Unity version and
the Console output, or email NomadStudios47@outlook.com.

---

## Limitations

- UGUI only. UI Toolkit is not supported.
- One `UIPilot_Canvas` per scene, with up to three menus: Main, Pause, Settings.
- The Settings menu ships with volume, fullscreen and quality. Others, such as key
  bindings, are yours to add.
- The menus are tuned for desktop and console screens (1920 x 1080 reference). On
  phones, raise the buttons' **Preferred Height** for comfortable touch targets.
- UI Health checks the scenes open in Edit mode, and every scene in a build. It does
  not see UI your scripts create at runtime, or a prefab open in Prefab Mode.
- The Click Debugger lists listeners set in the Inspector. Listeners added from code
  still run, but are not listed.
- A theme's scene and picture are drawn for 16:9 and cropped, not stretched, on other
  screen shapes.
- Tested on Unity 6000.3.11f1 (Windows) with the Built-in Render Pipeline, and in a new
  URP project.
