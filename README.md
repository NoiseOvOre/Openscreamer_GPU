# OpenScreamer GPU

**A GPU-enhanced version of OpenScreamer, bringing Screamer (1995) and Screamer 2 (1996) to modern Windows PCs with improved OpenGL rendering, widescreen support, and configurable graphics settings.**

Based on the original **OpenScreamer** project developed by **Danik**.

## 🎬 OpenScreamer GPU v1.01 — Gameplay Showcase

[![Watch OpenScreamer GPU v1.01 on YouTube](https://img.youtube.com/vi/VIDEO_ID/hqdefault.jpg)](https://www.youtube.com/watch?v=VIDEO_ID)
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
| Display mode | Borderless fullscreen / Windowed / Exclusive fullscreen |
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
- Playback of original CD audio music from extracted files.

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
- Original in-game options.
- Playback of original CD audio music from extracted files.

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
- The original game data for Screamer and/or Screamer 2.
- Windows PowerShell for the graphical launcher.
- The required SDL2 and runtime libraries.

### Step 1 — Download

Download the latest available archive from the project's GitHub Releases page:

[OpenScreamer GPU Releases](https://github.com/NoiseOvOre/OpenScreamer_GPU/releases)

Extract the archive to a folder of your choice.

### Step 2 — Prepare the Game Data

OpenScreamer GPU does not include the original commercial game files.

You must supply the game data from your own copies of Screamer and Screamer 2.

Place the game data folders next to `openscreamer.exe`.

Example installation structure:

```text
OpenScreamer_GPU_1.0/
├── openscreamer.exe
├── launcher.cmd
├── Lanceur_OpenScreamer_GPU.ps1
├── SDL2.dll
│
├── screamer/
│   ├── [original Screamer game data]
│   └── music/
│       ├── track_02.ogg
│       ├── track_03.ogg
│       └── ...
│
├── screamer2/
│   ├── [original Screamer 2 game data]
│   └── music/
│       ├── track_02.ogg
│       ├── track_03.ogg
│       └── ...
│
└── music/                   (optional shared fallback)
    └── track_02.ogg
```

The `screamer` and `screamer2` directories contain the original game data. Both are needed if you want both games available from the selection menu.

The `music` directories contain extracted audio tracks from the original game CDs.

### Step 3 — Launch the Game

1. Double-click `launcher.cmd`.
2. Select your preferred language.
3. Configure the graphics settings.
4. Click the launch button.
5. Select Screamer or Screamer 2 from the game's selection menu.

Your graphics settings will be saved for future sessions.

**Note:** If your downloaded package contains source code but no compiled `openscreamer.exe`, you must compile the engine before launching it.

## Music and Audio Support

Both **Screamer (1995)** and **Screamer 2 (1996)** use music from their original game CDs.

OpenScreamer GPU supports playing the original CD audio tracks directly from extracted audio files, without requiring the physical CDs during gameplay.

### Supported Audio Formats

| Format | Extension | Supported |
|---|---|---|
| Ogg Vorbis | `.ogg` | Yes |
| MP3 | `.mp3` | Yes |
| WAV | `.wav` | Yes |
| FLAC | `.flac` | No |
| AAC / M4A | `.aac` / `.m4a` | No |

OGG Vorbis is recommended for its good audio quality and efficient file size.

WAV can be used when preserving the original CD audio without lossy compression is preferred.

### Music Folder Structure

Each game has its own dedicated music directory.

**Screamer (1995):**

```text
screamer/
├── [original game data]
└── music/
    ├── track_02.ogg
    ├── track_03.ogg
    ├── track_04.ogg
    └── ...
```

**Screamer 2 (1996):**

```text
screamer2/
├── [original game data]
└── music/
    ├── track_02.ogg
    ├── track_03.ogg
    ├── track_04.ogg
    └── ...
```

### Audio Track Naming

Audio files must follow this naming convention:

`track_NN.extension`

Where `NN` represents the original CD audio track number.

Examples:

- `track_02.ogg`
- `track_03.mp3`
- `track_04.wav`

Preserve the original CD track numbering. Do not renumber tracks simply to make the sequence start at 01.

### Music Folder Search Order

For the selected game, OpenScreamer GPU searches for music in the following locations:

1. The selected game's `music/` directory.
2. The selected game's main data directory.
3. The shared `music/` directory next to the engine executable.

For example:

```text
screamer/music/track_02.ogg
screamer/track_02.ogg
music/track_02.ogg
```

Or for Screamer 2:

```text
screamer2/music/track_02.ogg
screamer2/track_02.ogg
music/track_02.ogg
```

The recommended setup is to use separate `music` directories for Screamer and Screamer 2 to avoid mixing their soundtracks.

Within a directory, the supported formats are checked in the following order:

1. `.ogg`
2. `.mp3`
3. `.wav`

If multiple versions of the same track exist in the same directory, the first supported format found will be selected.

### Extracting the Original CD Music

To enable the original music:

1. Obtain your original Screamer or Screamer 2 CD, or your own disc image.
2. Extract the CD audio tracks using a suitable CD audio extraction program.
3. Save or convert the tracks to OGG, MP3, or WAV.
4. Rename the files using the `track_NN` naming convention, preserving their original CD track numbers.
5. Copy the tracks into the corresponding game's `music` directory.
6. Launch the game normally.

The original CD audio tracks are copyrighted game content and are **not distributed with OpenScreamer GPU**.

### Troubleshooting Missing Music

If the game runs but the music is missing:

- Verify that the audio files are in the correct game's `music` directory.
- Check that filenames use two-digit track numbers, such as `track_02.ogg`.
- Make sure the extensions are `.ogg`, `.mp3`, or `.wav`.
- Verify that the audio files are valid and playable.
- Preserve the original CD track numbering.
- Check the in-game music volume and CD player settings.

FLAC files must be converted to a supported format before use.

## Building from Source

The project includes scripts for building the Windows version of OpenScreamer GPU.

### Windows Build Requirements

The provided build scripts are designed for the MSYS2 UCRT64 environment.

Required tools and libraries include:

- MSYS2 UCRT64.
- GCC.
- CMake.
- Ninja.
- SDL2 development libraries.

### Compilation

1. Install MSYS2 and the required UCRT64 development packages.
2. Extract the OpenScreamer GPU source archive.
3. Open the `01_MOTEUR_GPU` directory.
4. Run `Compiler_OpenScreamer_Windows.bat`.
5. Wait for the build to finish.

The script invokes the MSYS2 build environment and compiles the engine.

The resulting executable and required runtime libraries are placed in the generated `OpenScreamer_GPU_1.0` directory.

The compilation script also creates a build log that can be used to investigate compilation errors.

## Configuration Files

The Windows launcher saves user preferences in:

```text
%LOCALAPPDATA%\OpenScreamerGPU\launcher.json
```

This file stores the selected language and graphics settings.

Settings are loaded automatically on subsequent launches.

Deleting this configuration file resets the launcher to its default settings.

## Original Game Assets

OpenScreamer GPU is not a standalone commercial game.

It is a source-code project that requires original Screamer game data to run.

No original commercial game assets, copyrighted game music, or complete game distributions are provided as part of this project.

Users are responsible for obtaining the required game data from legitimate copies.

## Project Philosophy

The development of OpenScreamer GPU follows several principles:

**Preserve the original experience.** The original driving physics, gameplay, menus, and visual identity should remain recognizable.

**Modernize the rendering.** Modern GPUs and displays should be able to present the games at higher resolutions and with improved graphical filtering.

**Avoid unnecessary changes.** The goal is not to redesign Screamer or Screamer 2, but to improve their presentation and compatibility.

**Maintain compatibility.** Changes to the rendering engine should avoid introducing regressions into the existing games.

**Respect the original work.** OpenScreamer GPU exists thanks to the reverse-engineering and development efforts behind the original OpenScreamer project.

## Known Limitations

- The project is focused on Windows.
- Original commercial game data is required.
- Original CD music must be extracted separately for both Screamer and Screamer 2.
- FLAC audio is not currently supported for CD music playback.
- Some graphical behavior may still differ from the original DOS releases.
- Rendering compatibility may vary depending on GPU drivers and hardware.
- Certain graphics options may not affect every scene in the same way.
- The Windows executable launcher experiment is not part of the stable 1.0 release; the supported launcher is `launcher.cmd`.

## Credits

### Original OpenScreamer Project

**Danik — Original OpenScreamer author and developer.**

OpenScreamer GPU is based on Danik's original OpenScreamer source code and reverse-engineering work.

The original engine implementation provides the foundation on which the GPU rendering enhancements have been developed.

Full credit for the original OpenScreamer project belongs to Danik and its respective contributors.

### OpenScreamer GPU

GPU rendering enhancements, graphical configuration integration, widescreen presentation improvements, and additional development based on the original OpenScreamer engine.

### Original Games

**Screamer (1995)** and **Screamer 2 (1996)** were developed by Milestone.

All original game names, assets, music, and trademarks remain the property of their respective owners.

This is an independent fan development project and is not an official release by the original game developers or publishers.

## License

OpenScreamer GPU is distributed under the **GNU General Public License version 3.0 (GPL-3.0)**, following the license of the original OpenScreamer project.

See the `LICENSE` file for the complete license text.

The GPL-3.0 covers the relevant project source code, not the original games or their commercial data.

Third-party components retain their respective licenses:

- `port/src/nuked/` — LGPL 2.1 or later.
- `port/src/third_party/` — Public Domain or MIT-0, as specified in their respective source files.

All existing copyright notices and third-party license information must be preserved.

---

**OpenScreamer GPU — Bringing classic arcade racing to modern hardware while preserving the spirit of the originals.**
