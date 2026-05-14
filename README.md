# epicEFI Console and TunerStudio plugin  ![GitHub Release](https://img.shields.io/github/v/release/epicEFI/epic-console)

<img width="888" height="625" alt="image" src="https://github.com/user-attachments/assets/2a14188c-bc0f-4f0d-8836-22d5c63e4b76" />

A TunerStudio plugin and standalone application for the [epicEFI](https://epicefi.com). It covers the parts of running an epicEFI ECU that TunerStudio itself does not: firmware flashing, ECU backup, online updates, Lua scripting, and diagnostics.

### [Get the latest release](https://github.com/epicEFI/epic-console/releases/)  

## Features

- **ECU identification** - Enables identification of the connected ECU, if it is active or in recovery (DFU), along with reboot to recovery or firmware.
- **Online firmware updates** - Enables automatic identification and firmware updates for ECUs, with automatic backup before flashing the latest firmware.
- **ECU backup** - Reads the current firmware off the controller and saves it locally, including the tune. Flashing these updates back restores the ECU fully.
- **Image flashing** - Enables flashing custom images or backups back to the ECU. Enables recovering of bricked ECUs
- **Fault codes** - Reads the fault codes from the ECU and displays a industry-standard error message.
- **Lua** - A built-in Lua IDE with syntax highlighting, error checking with inline markers, and autocomplete, plus Load and Burn directly to the controller.
- **Dark mode** - Automatic dark-light mode switching according to system theme

## How it runs

The console is a single executable with two entry points:

- **Inside TunerStudio.** Open the plugin from TunerStudio using Plugins -> epicEFI Plugin.
- **As a standalone console.** Launch the console from the desktop shortcut or start menu.

## Installation

A Windows installer is the recommended way to install. It bundles the plugin together with the STM32, ST-Link, and VCP drivers required for flashing on Windows, registers the plugin with TunerStudio, and places a desktop shortcut that opens the standalone console.

Download the latest installer (and the raw JAR, if you prefer to install it manually) from the [Releases](../../releases) page.

