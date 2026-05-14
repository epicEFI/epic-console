# epicEFI Console and TunerStudio plugin

<img width="928" height="582" alt="image" src="https://github.com/user-attachments/assets/b00856d3-de12-440d-ac4c-73616657bf5c" />

A TunerStudio plugin and standalone application for the [epicEFI](https://epicefi.com) fork of rusEFI. It covers the parts of running an epicEFI ECU that TunerStudio itself does not: firmware flashing, ECU backup, online updates, Lua scripting, and diagnostics.

This repository hosts the released binaries. The source lives in a separate repository.

## What it does

- **Flashes epicEFI firmware to the ECU.** Reads the rusEFI signature off the connected controller, identifies the board and firmware version, reboots into DFU, then erases and writes the new image.
- **Online firmware updates.** Checks for the latest release for your specific board, downloads it, installs the matching TunerStudio INI definition, and flashes the firmware.
- **ECU backup.** Reads the current firmware off the controller and saves it locally, so there is always a known-good image to roll back to.
- **Flash an arbitrary firmware file.** For development builds, custom firmware, or restoring from backup.
- **Diagnostic trouble codes.** Reads DTCs from the running ECU.
- **Lua scripting for the ECU.** A built-in editor with syntax highlighting, error checking with inline markers, and autocomplete, plus Load and Burn directly to the controller.

## How it runs

The console is a single executable with two entry points:

- **Inside TunerStudio.** Open the plugin from TunerStudio using Plugins -> epicEFI Plugin.
- **As a standalone console.** Launch the console from the desktop shortcut or start menu.

## Installation

A Windows installer is the recommended way to install. It bundles the plugin together with the STM32, ST-Link, and VCP drivers required for flashing on Windows, registers the plugin with TunerStudio, and places a desktop shortcut that opens the standalone console.

Download the latest installer (and the raw JAR, if you prefer to install it manually) from the [Releases](../../releases) page.

