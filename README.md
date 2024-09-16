# Deadlock Optimization Guide
You can follow on X https://twitter.com/cosmicw0nxy

For anyone who needs a bit more explanation, here’s a video. https://www.youtube.com/watch?v=rNxrJaed8vE

This repository contains a collection of configuration files and settings designed to optimize the performance of DeadLock, ensuring a smoother and more responsive gaming experience. The configurations focus on maximizing FPS, reducing input lag, and minimizing visual distractions, making it ideal for competitive gameplay.

## Table of Contents
- [Deadlock Guide](#deadlock-optimization-guide)
  - [Steam Game Launch Options](#steam-game-launch-options)
  - [Video Configuration](#video-configuration)
  - [Autoexec Configuration](#autoexec-configuration)

**Note:** While these settings aim to optimize your gaming performance, individual results may vary based on your specific hardware and peripherals.

## Deadlock Optimization Guide

### Steam Game Launch Options

To optimize your **Deadlock** gameplay, add the following commands to your launch options in Steam:

| Command          | Description |
|------------------|-------------|
| `+exec autoexec.cfg`          | Executes a cfg file on startup |
| `-dev`           | Skips intro on startup, may cause HUD flicker issues on NVIDIA cards |
| `-fullscreen`    | Forces the game to launch in fullscreen mode |
| `-high`          | Prioritizes the game in system processes |
| `-preload`       | Preloads game assets |
| `-forcenovsync`  | Disables vertical sync |
| `-m_rawinput 1`  | Ensures raw input is used for mouse movements |
| `-console` | Opens the developer console |
| `-noassert`| Disables assertion checks |
|` +@panorama_min_comp_layer_cache_cost_TURNED_OFF 256 `| Optimizes UI performance  |
| ` -convars_visible_by_default `| Makes certain console variables visible by default |




Example of full command line: `-m_rawinput 1 +exec autoexec.cfg -console -noassert +@panorama_min_comp_layer_cache_cost_TURNED_OFF 256 -convars_visible_by_default -high -dev -preload -fullscreen `

### Video Configuration

This section explains the purpose and effects of various settings in the `video.txt` file for **Deadlock** to improve game performance and visual quality:

Other recommended adjustments:
- **Particle Levels**: Reduced for minimal distraction and improved performance.
- **Ragdoll Effects**: Disabled to decrease CPU load.
- **Shadow and Lighting Effects**: Minimized to enhance FPS.

You can download the example [Video.txt](https://github.com/w0nxyApex/Deadlock-Tweaks-config/blob/main/video.txt). Make sure to check which FPS you are targeting and adjust frame times accordingly. Also, set the correct resolution for your display.

**Tip:** Set the file to read-only to prevent the game from overwriting your settings.

### Autoexec Configuration

The `autoexec.cfg` file pre-loads specific commands to enhance performance and in-game behavior for **Deadlock**:
[autoexec.cfg](https://github.com/w0nxyApex/Deadlock-Tweaks-config/blob/main/autoexec.cfg)

- Default startup settings.
- Graphical adjustments.

> ### Place this file in your Steam or Origin storage location in the cfg folder. For Windows.
> ` (C:\Program Files (x86)\Steam\steamapps\common\Deadlock\game\citadel\cfg) `
> There is already a video.txt file you just have to change the content. Or copy mine but
> ⚠️ **!! make sure you don't leave**
> **"VendorID" ""**
> **"DeviceID" ""**
> **empty. There is a video.txt with your IDs in there, take them over!!!!**


## Key Features

- **Low-Latency Settings**: Configurations like `r_low_latency 2` and `engine_low_latency_sleep_after_client_tick "true"` help reduce input lag, giving you a competitive edge.
- **Maximized FPS**: The settings are designed to uncap FPS (`fps_max "0"`) while reducing unnecessary graphical load, such as disabling V-Sync, anti-aliasing, and complex particle effects.
- **Optimized Visuals for Performance**: Textures, shadows, and post-processing effects are minimized or disabled to ensure the game runs smoothly on a wide range of hardware.
- **DirectX 11 Support**: Option to run the game with DirectX 11 (`mat_dxlevel 110`) for enhanced graphical features on modern hardware.
- **Customizable Sensitivity and Controls**: Easily adjustable sensitivity and custom key bindings to suit your gameplay style.

## Included Files

- `video.cfg`: Optimized video settings file focusing on high FPS and low latency.
- `autoexec.cfg`: Autoexec script for additional performance tweaks and custom commands.

## How to Use

1. **Download the Config Files**: Clone this repository or download the specific configuration files you need.
2. **Place in Game Directory**: Copy the configuration files into your Deadlock game directory (usually found in `C:\Program Files (x86)\Steam\steamapps\common\Deadlock\game\citadel\cfg`.
3. **Modify as Needed**: Feel free to tweak the settings based on your hardware capabilities and personal preferences.
4. **Launch the Game**: Start Deadlock and enjoy improved performance and responsiveness.

## Contributions

Contributions are welcome! If you have additional tweaks, optimizations, or suggestions, feel free to fork this repository and submit a pull request.

## Disclaimer

These settings are heavily optimized for performance and may significantly reduce visual quality. Adjust settings based on your preferences and hardware capabilities.
