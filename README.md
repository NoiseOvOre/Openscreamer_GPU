# OpenScreamer GPU

**A GPU-enhanced version of OpenScreamer, bringing Screamer (1995) and Screamer 2 (1996) to modern Windows PCs with improved OpenGL rendering, widescreen support, and configurable graphics settings.**

Based on the original **OpenScreamer** project developed by **Danik**.

---

## About the Project

OpenScreamer GPU is an enhanced version of the OpenScreamer engine, designed to modernize the rendering of two classic arcade racing games developed by Milestone:

- **Screamer (1995)**
- **Screamer 2 (1996)**

The main objective is to preserve the original gameplay, physics, atmosphere, and visual identity of these games while improving their compatibility with modern graphics hardware and displays.

Unlike running the original DOS versions through an emulator, OpenScreamer GPU builds upon the native OpenScreamer engine and introduces a GPU-oriented rendering path.

The project focuses on improving visual presentation without turning the games into remakes or replacing their original assets.

## Main Features

### GPU-Accelerated Rendering

- OpenGL-based rendering designed for modern GPUs.
- Improved rendering of 3D environments, vehicles, and tracks.
- Higher rendering resolutions than the original games.
- Reduced reliance on the original low-resolution software-rendering presentation.
- GPU rendering improvements for game menus, transitions, and races.
- Preservation of the original graphical style and game assets.

### Modern Display Support

- Support for modern widescreen displays.
- 16:9 and other display aspect ratios.
- High-resolution rendering, including 1440p and 4K.
- Borderless fullscreen, windowed, and exclusive fullscreen modes.
- Configurable display refresh rate.
- Optional vertical synchronization.
- Adjustable field of view.
- Configurable HUD presentation.

### Enhanced Graphics Settings

The graphical launcher provides several options to customize the experience:

| Setting | Available Options |
|---|---|
| Resolution | Native display resolution and selectable resolutions up to 4K |
| Display mode | Borderless fullscreen, Windowed, Exclusive fullscreen |
| Refresh rate | Selectable display refresh rate |
| V-Sync | On / Off |
| MSAA | Off / 2x / 4x / 8x |
| Texture filtering | Original sharp pixels / Bilinear / Trilinear with mipmaps |
| Anisotropic filtering | 1x / 2x / 4x / 8x / 16x |
| Draw distance | 100% / 150% / 200% / 250% / 300% |
| Vertical FOV | 75° / 83.5° / 95° / 110° |
| HUD layout | Widescreen / Original centered 4:3 |
| Brightness | 70% to 130% |
| Contrast | 70% to 130% |
| Gamma | 0.70 to 1.30 |

Some options may have different visual effects depending on the selected game, scene, and graphics hardware.

### Improved Rendering and Presentation

OpenScreamer GPU includes work on:

- Widescreen presentation during races.
- HUD positioning and scaling.
- Rendering transitions between menus and gameplay.
- Displaying original 2D and 3D game elements correctly.
- Maintaining consistent GPU output during scene changes.
- Improving the rendering of vehicles and environmental geometry.
- Preserving original menus and in-game options.

The objective is to provide a visually consistent experience while remaining faithful to the original games.

## Supported Games

### Screamer (1995)

The first Screamer is supported through the OpenScreamer engine with GPU rendering enhancements.

Features include:

- Original racing gameplay.
- Original cars and circuits.
- Original game menus and options.
- High-resolution rendering.
- Widescreen display support.
- Improved HUD positioning.
- Modern texture filtering and anti-aliasing options.

**Important:** For the complete track scenery to appear correctly, set the original game's graphical detail options to their highest values.

### Screamer 2 (1996)

Screamer 2 is also supported, with improvements to rendering and presentation.

Features include:

- Original racing gameplay.
- Original cars, tracks, and menus.
- High-resolution GPU rendering.
- Widescreen race presentation.
- Improved HUD scaling and positioning.
- GPU-oriented menu and race transitions.
- Original in-game options and CD music support.

The goal is to preserve the authentic Screamer 2 experience while providing a more suitable visual presentation for modern PCs.

## Graphical Launcher

OpenScreamer GPU includes a dedicated Windows graphical configuration launcher.

The launcher allows users to configure rendering options without manually editing configuration files.

Features:

- French and English interface.
- Language selection using a flag icon.
- Two-column layout with all graphics settings visible.
- Automatic detection of the primary display resolution.
- Save and restore graphics settings.
- Separate buttons to save settings or launch the game.
- Built-in game selection through the original OpenScreamer menu.

The stable 1.0 release uses a Windows command script to start the graphical launcher.

**To open the launcher, double-click `launcher.cmd`.**

The launcher uses Windows PowerShell and Windows Forms.

Graphics preferences are saved locally and automatically restored when the launcher is opened again.

## Installation

### Requirements

- Windows 10 or Windows 11.
- A graphics card supporting the OpenGL features required by the engine.
- The original game data for Screamer and
