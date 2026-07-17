<div align="center">

# STEAXS FILTER PACK

### A curated ReShade preset collection for Dead by Daylight

Bring clearer visibility, richer colors and a carefully tuned atmosphere to every Realm — without replacing any game files.

[![Presets](https://img.shields.io/badge/presets-26-E50914?style=for-the-badge)](#preset-collection)
[![ReShade](https://img.shields.io/badge/ReShade-required-111111?style=for-the-badge)](https://reshade.me/)
[![Platform](https://img.shields.io/badge/platform-Windows-0078D4?style=for-the-badge&logo=windows11&logoColor=white)](#requirements)
[![Game](https://img.shields.io/badge/game-Dead%20by%20Daylight-2B2B2B?style=for-the-badge)](https://deadbydaylight.com/)

[Download latest release](https://github.com/steaxss/STEAXS-FILTER-PACK/releases) · [French video tutorial](https://www.youtube.com/watch?v=9N2fREVt7W4) · [Discord](https://discord.com/invite/6RHPNNVtKw) · [Support the project](https://www.buymeacoffee.com/steaxss)

</div>

---

## Overview

STEAXS Filter Pack is a collection of ready-to-use **ReShade presets made specifically for Dead by Daylight**. It includes a general streaming preset, a gamma preset and individual color profiles for 24 maps or Realms.

The repository also contains an optional performance-oriented DBD configuration and reference screenshots for NVIDIA Control Panel. Each part can be installed independently.

> [!IMPORTANT]
> This repository contains ReShade **preset files only**. ReShade itself and its shader packages must be downloaded separately from the [official ReShade website](https://reshade.me/).

## Highlights

- **26 handcrafted presets** covering generic use and map-specific looks
- Simple `.ini` files — easy to install, switch and customize
- Compatible with the Steam and Epic Games versions of Dead by Daylight
- Optional DBD settings for raw mouse input and a performance-focused baseline
- NVIDIA Control Panel reference settings included as screenshots
- No game assets, executables or ReShade binaries redistributed

## Requirements

- Windows 10 or Windows 11
- [Dead by Daylight](https://deadbydaylight.com/) installed on PC
- A recent version of [ReShade](https://reshade.me/)
- ReShade effect packages installed during setup

The presets reference effects from several collections, including the standard ReShade shaders, SweetFX/legacy effects and [prod80's shader repository](https://github.com/prod80/prod80-ReShade-Repository). The easiest option is to **select all effect packages** when the ReShade installer asks which effects to download.

<details>
<summary><strong>Effects used by this pack</strong></summary>

`ColorIsolation` · `ContrastStretch` · `Deband` · `DeHaze` · `HSLShift` · `LiftGammaGain` · `LumaSharpen` · `PD80 Filmic Adaptation` · `PD80 Contrast / Brightness / Saturation` · `PD80 Selective Color` · `Sepia / Tint` · `Technicolor2` · `Tonemap`

</details>

## Quick installation

### 1. Download the pack

Get the newest archive from the [Releases page](https://github.com/steaxss/STEAXS-FILTER-PACK/releases), then extract it.

Alternatively, clone the repository:

```powershell
git clone https://github.com/steaxss/STEAXS-FILTER-PACK.git
```

### 2. Install ReShade

1. Download and run the installer from [reshade.me](https://reshade.me/).
2. Select the Dead by Daylight executable for your platform.
3. Choose **DirectX 10/11/12** as the rendering API.
4. When prompted for effect packages, select **all packages** to guarantee that every preset dependency is available.
5. Finish the installation.

Common executable locations:

| Platform | Default directory |
|:--|:--|
| Steam | `C:\Program Files (x86)\Steam\steamapps\common\Dead by Daylight\DeadByDaylight\Binaries\Win64` |
| Epic Games | `C:\Program Files\Epic Games\DeadByDaylight\DeadByDaylight\Binaries\EGS` |

Your installation may be on another drive or in a custom library. In that case, open the game installation folder from your launcher and locate the executable inside `DeadByDaylight\Binaries`.

### 3. Add the presets

Copy the complete [`FILTERS`](FILTERS) folder into the directory that contains the game executable selected during ReShade setup.

Your game directory should now contain something similar to:

```text
DeadByDaylight/Binaries/Win64/        # or Binaries/EGS
├── FILTERS/
│   ├── 00.STX.Stream.ini
│   ├── 00A.STX.Gamma.ini
│   └── ...
├── reshade-shaders/
├── ReShade.ini
└── ReShade.log
```

### 4. Select a preset in game

1. Start Dead by Daylight.
2. Press **Home** to open the ReShade overlay (unless you changed its shortcut).
3. Complete the short ReShade tutorial if it appears.
4. In the **Home** tab, use the preset selector at the top and browse to `FILTERS`.
5. Choose the preset matching the current map, or use `00.STX.Stream.ini` / `00A.STX.Gamma.ini` as a general profile.

> [!TIP]
> Once you are happy with the result, enable **Performance Mode** in ReShade to optimize effect compilation. Disable it again before editing individual shader values.

## Preset collection

| # | Preset | # | Preset |
|:--:|:--|:--:|:--|
| `00` | Stream | `00A` | Gamma |
| `01` | Autohaven | `02` | Backwater |
| `03` | Borgo | `04` | Coldwind Farm |
| `05` | Crotus Prenn | `06` | Eyrie |
| `07` | Fallen Refuge | `08` | Garden |
| `09` | Greenville / FNAF | `10` | Hawkins |
| `11` | Léry's | `12` | Macmillan |
| `13` | Midwich | `14` | Nostromo |
| `15` | Ormond | `16` | Ormond Lake |
| `17` | RCPD | `18` | Red Forest |
| `19` | Saloon | `20` | Sleepless District |
| `21` | Springwood | `22` | The Game |
| `23` | Toba Landing | `24` | Yamaoka |

All preset files live in [`FILTERS/`](FILTERS). You can duplicate any `.ini` file before adjusting it if you want to create a personal variation while preserving the original.

## Optional DBD configuration

The [`CONFIG/DBD CONFIG`](CONFIG/DBD%20CONFIG) directory contains a performance-focused `GameUserSettings.ini` and the raw mouse input lines to add to `Input.ini`.

> [!WARNING]
> Back up your current configuration before replacing or editing anything. The included `GameUserSettings.ini` is configured for **2560×1440 at 120 FPS** and must be adapted to your monitor.

Open the active DBD configuration directory with <kbd>Win</kbd> + <kbd>R</kbd>:

```text
%LOCALAPPDATA%\DeadByDaylight\Saved\Config\WindowsClient
```

### Raw mouse input

Append the contents of [`ADD THIS TO YOUR INPUT.ini.txt`](CONFIG/DBD%20CONFIG/ADD%20THIS%20TO%20YOUR%20INPUT.ini.txt) to your existing `Input.ini`:

```ini
[/Script/Engine.InputSettings]
bEnableMouseSmoothing=False
bDisableMouseAcceleration=True
RawMouseInputEnabled=1
```

### Game user settings

Before using the included [`GameUserSettings.ini`](CONFIG/DBD%20CONFIG/GameUserSettings.ini), update every resolution field so it matches your display:

```ini
ResolutionSizeX=2560
ResolutionSizeY=1440
LastUserConfirmedResolutionSizeX=2560
LastUserConfirmedResolutionSizeY=1440
DesiredScreenWidth=2560
DesiredScreenHeight=1440
LastUserConfirmedDesiredScreenWidth=2560
LastUserConfirmedDesiredScreenHeight=1440
```

To use another frame-rate cap, also update both `FPSLimitMode` and `FrameRateLimit` consistently.

You may mark the edited files as **read-only** to stop the game from overwriting them. Remember that this also prevents in-game settings from being saved; remove read-only mode before changing options later.

For the full procedure, read [`CONFIG/README.txt`](CONFIG/README.txt).

## Optional NVIDIA settings

Reference screenshots for the NVIDIA Control Panel are provided in [`CONFIG/NVDIA CONTROL PANEL SETTINGS`](CONFIG/NVDIA%20CONTROL%20PANEL%20SETTINGS). These settings are optional and are **not required** for the ReShade presets to work.

<details>
<summary><strong>View NVIDIA 3D settings — page 1</strong></summary>

![NVIDIA 3D settings — page 1](CONFIG/NVDIA%20CONTROL%20PANEL%20SETTINGS/NVIDIA%203D%20SETTINGS%20-%201.png)

</details>

<details>
<summary><strong>View NVIDIA 3D settings — page 2</strong></summary>

![NVIDIA 3D settings — page 2](CONFIG/NVDIA%20CONTROL%20PANEL%20SETTINGS/NVIDIA%203D%20SETTINGS%20-%202.png)

</details>

<details>
<summary><strong>View NVIDIA 3D settings — page 3</strong></summary>

![NVIDIA 3D settings — page 3](CONFIG/NVDIA%20CONTROL%20PANEL%20SETTINGS/NVIDIA%203D%20SETTINGS%20-%203.png)

</details>

<details>
<summary><strong>View desktop size and position settings</strong></summary>

![NVIDIA desktop size and position](CONFIG/NVDIA%20CONTROL%20PANEL%20SETTINGS/NVIDIA%20DESKTOP%20SIZE%20AND%20POSITION.png)

</details>

## Troubleshooting

<details>
<summary><strong>The ReShade overlay does not appear</strong></summary>

- Confirm that ReShade was installed against the actual DBD executable, not the launcher.
- Run the ReShade installer again and verify that **DirectX 10/11/12** is selected.
- Check for `ReShade.log` beside the game executable; its presence confirms that ReShade attempted to load.
- The default overlay shortcut is **Home**, but it can be changed in `ReShade.ini`.

</details>

<details>
<summary><strong>A preset is missing from the selector</strong></summary>

Use the browse button beside the preset field and select the `.ini` file directly from the copied `FILTERS` directory. Also make sure Windows did not turn the file into `.ini.txt` during extraction or copying.

</details>

<details>
<summary><strong>Some effects are red or fail to compile</strong></summary>

One or more shader packages are missing. Run the ReShade installer again, update the existing installation and select all effect packages. In ReShade's **Settings** tab, also confirm that the effect search path points to your `reshade-shaders\Shaders` directory.

</details>

<details>
<summary><strong>The image is too dark, bright or saturated</strong></summary>

First verify that you selected the preset intended for the current map. Display calibration, HDR, driver color settings and in-game brightness can all affect the final result, so adjust these variables one at a time.

</details>

<details>
<summary><strong>The game keeps restoring my configuration</strong></summary>

Close the game before editing its files. As a last step, mark the relevant `.ini` file as read-only. Remove that attribute whenever you want Dead by Daylight to save settings again.

</details>

## Repository structure

```text
STEAXS-FILTER-PACK/
├── FILTERS/                          # 26 ReShade presets
├── CONFIG/
│   ├── DBD CONFIG/                   # Optional game and input settings
│   ├── NVDIA CONTROL PANEL SETTINGS/ # Optional NVIDIA reference images
│   └── README.txt                    # Detailed configuration guide
├── DBD OVERLAYTOOLS.html             # Shortcut to DBD Overlay Tools
├── FRENCH VIDEO TUTORIAL.html        # Shortcut to the video tutorial
├── JOIN THE DISCORD.html             # Community shortcut
└── SUPPORT ME.html                   # Project support shortcut
```

## Community & links

- **Video guide (French):** [Watch the complete installation tutorial](https://www.youtube.com/watch?v=9N2fREVt7W4)
- **Community:** [Join the Discord server](https://discord.com/invite/6RHPNNVtKw)
- **DBD Overlay Tools:** [dbdoverlaytools.com](https://dbdoverlaytools.com/) · [Discord](https://discord.com/invite/aVdT8rRJKc)
- **Support:** [Buy Me a Coffee](https://www.buymeacoffee.com/steaxss)

## Disclaimer

STEAXS Filter Pack is an independent community project and is not affiliated with or endorsed by Behaviour Interactive, Dead by Daylight, ReShade or NVIDIA. Third-party software and game updates may affect compatibility. Always use current official downloads and review the game's current rules before installing third-party tools.

---

<div align="center">

Made with care by [Steaxs](https://github.com/steaxss)

If this pack improves your experience, consider leaving feedback on Discord or supporting the project.

</div>
