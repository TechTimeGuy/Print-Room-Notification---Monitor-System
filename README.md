# Print Room Notification / Monitor System
ESP32 + 2.8" TFT Touchscreen (Home Assistant / ESPHome)

A compact, always-on **2.8" TFT touchscreen status display** built around an **ESP32** and **Home Assistant**.
Designed for print rooms and workshops to provide real-time visibility into **air quality** and **3D printer status** without dashboards, tablets, or cloud services.

This device is display-only: all logic, thresholds, and data come directly from Home Assistant.

## Repository Structure

Print-Room-Notification---Monitor-System/
- stl/        → 3D printable enclosure files
- esphome/    → ESPHome YAML configuration
- docs/       → wiring diagrams and setup documentation
- images/     → screen layouts and project photos
- README.md
- .gitignore
- .gitattributes

## What It Displays

- Air Quality (AQI / eCO2 / TVOC)
- 3D printer status (Idle / Printing / Paused / Finished / Error)
- Print progress percentage
- Remaining print time (when available)
- Layout supports multiple printers and sensors

Originally designed around Bambu Lab printers, but compatible with **any Home Assistant printer integration**.

## Requirements

- ESP32 (required)
- 2.8" SPI TFT display (ILI9341)
- Touch controller (XPT2046)
- Home Assistant
- ESPHome

ESP8266 is **not supported** due to memory and display limitations.

## 3D Printing

Enclosure files are located in the `stl/` folder.

- Designed for standard FDM printers
- No supports required
- PLA or PETG recommended
- Desk and workbench friendly footprint

## Setup Overview

1. Print the enclosure from the `stl/` folder
2. Wire the ESP32 to the TFT display and touch controller (see `docs/`)
3. Flash the ESP32 using ESPHome and the YAML in `esphome/`
4. Confirm the device appears in Home Assistant
5. Verify sensor and printer entities are available
6. Adjust layout or displayed entities as desired

## Documentation

See the `docs/` folder for:
- Wiring references
- Display pin mapping
- ESPHome configuration notes

Screenshots and layout references can be found in the `images/` folder.

## Example Use Cases

- Print room air quality monitoring
- Live printer status and progress display
- Workshop environmental visibility
- Quiet, always-on status screen for Home Assistant


## Notes

This project was designed to be reliable, local, and distraction-free —
a purpose-built status display for environments where information needs
to be visible at a glance.

Happy building.
