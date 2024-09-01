# Deadlock Optimization Guide

This guide is designed to enhance your gameplay experience in **Deadlock** through detailed configurations and optimizations for video settings, Windows settings, and NVIDIA settings. The goal is to reduce micro stutters and FPS lags, ensuring a smooth and responsive gaming experience.

## Table of Contents
- [Deadlock Guide](#deadlock-optimization-guide)
  - [Steam Game Launch Options](#steam-game-launch-options)
  - [Video Configuration](#video-configuration)
  - [Autoexec Configuration](#autoexec-configuration)
- [Windows Settings](#windows-settings-guide)
  - [Ultimate Performance](#ultimate-performance-mode-in-windows)
  - [Improve Internet performance](#improve-internet-performance-with-the-right-mtu-size)
- [NVIDIA Settings](#nvidia-guide)
  - [NVIDIA New Driver](#new-nvidia-driver)
  - [NVIDIA Display](#nvidia-display-settings)
  - [NVIDIA 3D Settings](#nvidia-3d-settings)

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
| `-console` | 
| `-noassert`| 
|` +@panorama_min_comp_layer_cache_cost_TURNED_OFF 256 `|
| ` -convars_visible_by_default `|




Example of full command line: `-m_rawinput 1 +exec autoexec.cfg -console -noassert +@panorama_min_comp_layer_cache_cost_TURNED_OFF 256 -convars_visible_by_default -fps_max 0 -high -dev -preload -fullscreen `

### Video Configuration

This section explains the purpose and effects of various settings in the `videoconfig.txt` file for **Deadlock** to improve game performance and visual quality:

Other recommended adjustments:
- **Particle Levels**: Reduced for minimal distraction and improved performance.
- **Ragdoll Effects**: Disabled to decrease CPU load.
- **Shadow and Lighting Effects**: Minimized to enhance FPS.

You can download the example [Videoconfig.txt](https://github.com/w0nxyApex/Deadlock-Tweaks-config/blob/main/video.txt). Make sure to check which FPS you are targeting and adjust frame times accordingly. Also, set the correct resolution for your display.

**Tip:** Set the file to read-only to prevent the game from overwriting your settings.

### Autoexec Configuration

The `autoexec.cfg` file pre-loads specific commands to enhance performance and in-game behavior for **Deadlock**:
[autoexec.cfg](https://github.com/w0nxyApex/Deadlock-Tweaks-config/blob/main/autoexec.cfg)

- Default startup settings.
- Graphical adjustments.

Place this file in your Steam or Origin storage location in the cfg folder. Download it [here](C:\Program Files (x86)\Steam\steamapps\common\Deadlock\game\citadel\cfg).

## Windows Settings Guide

### Ultimate Performance Mode in Windows

#### Overview
The Ultimate Performance Mode in Windows optimizes power settings to enhance system performance. This mode is particularly beneficial for **Deadlock** players who require maximum performance from their systems.

#### Activation Command

To activate Ultimate Performance Mode, which is not visible by default in Windows, use the following command in your command prompt:

```bash
powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61
```

After running the command, follow these steps to activate the Ultimate Performance Mode:

    Open Control Panel.
    Navigate to Hardware and Sound > Power Options.
    Under Choose or customize a power plan, select Ultimate Performance.

Improve Internet performance with the right MTU size
Calculating the Optimal MTU Size

To determine the optimal MTU size without packet loss, use the ping command. Start with a high MTU size and adjust as necessary:
