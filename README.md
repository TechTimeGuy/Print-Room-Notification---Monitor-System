# Print Room Notification / Monitor System (ESP32 + 2.8" TFT Touchscreen)

A compact, always-on **2.8" TFT touchscreen status display** built around an **ESP32** and **Home Assistant (ESPHome)**.
Designed for print rooms and workshops to show **Air Quality** and **3D printer status** at a glance.

This is a display-first project: Home Assistant provides the data, the ESP32 renders it on the screen.

## What It Shows

- Air Quality (AQI / eCO2 / TVOC) from Home Assistant sensors
- 3D Printer status (Idle / Printing / Paused / Finished / Error)
- Print progress percentage
- Remaining time (when available)
- Layout can be expanded for additional sensors/printers

## Requirements

- ESP32 (recommended / required)
- 2.8" SPI TFT display (ILI9341)
- Touch controller (XPT2046)
- Home Assistant
- ESPHome

## Repository Structure

(Adjust this section to match your folders)

Print-Room-Notification---Monitor-System/
- stl/        → 3D printable enclosure files
- esphome/    → ESPHome YAML configuration
- docs/       → wiring + setup documentation (PDF)
- images/     → screenshots / photos (optional)
- README.md
- .gitignore
- .gitattributes

## Setup Overview

1. Print the enclosure (see stl/)
2. Wire the ESP32 to the TFT + touch controller (see docs/)
3. Install ESPHome and flash the ESP32 using the YAML in esphome/
4. Confirm the device appears in Home Assistant and your entities are available
5. Tune the display layout and thresholds as needed

## Notes

- ESP32 is recommended because the display + touch stack needs more resources than ESP8266.
- This project is intended as a local, reliable workshop display (no cloud dependency).

## Suggested GitHub Topics

esp32, home-assistant, esphome, tft, ili9341, xpt2046, touchscreen, air-quality, aqi, 3d-printing, bambu-lab, workshop
