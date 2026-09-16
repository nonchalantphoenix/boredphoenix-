<div align="center">

<img src="./project-banner.svg" alt="ESP32 OLED Video Converter banner" width="100%">

# ESP32 OLED Video Converter

### English adaptation inspired by the original project by Tri Wahyu

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Open%20Converter-0ea5e9?style=for-the-badge&logo=github)](https://nonchalantphoenix.github.io/boredphoenix-/)
[![ESP32](https://img.shields.io/badge/Board-ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)](https://www.espressif.com/en/products/socs/esp32)
[![Arduino](https://img.shields.io/badge/Framework-Arduino-00979D?style=flat-square&logo=arduino&logoColor=white)](https://www.arduino.cc/)
[![OLED](https://img.shields.io/badge/Display-SSD1306%20%7C%20SH1106-111827?style=flat-square)](https://learn.adafruit.com/monochrome-oled-breakouts)
[![Browser](https://img.shields.io/badge/Runs%20in-Browser-4285F4?style=flat-square&logo=googlechrome&logoColor=white)](./index.html)
[![Attribution](https://img.shields.io/badge/Source-Attributed%20Adaptation-f59e0b?style=flat-square)](./ATTRIBUTION.md)

</div>

## Overview

A browser-based tool for converting local video into monochrome bitmap data suitable for ESP32 projects with 128×64 I2C OLED displays. The converter previews the result, applies configurable image processing, and generates C/C++ data that can be adapted for Arduino IDE sketches.

> **Provenance:** This is an **English-language adaptation inspired by and converted from** [Tri Wahyu's ESP32 OLED Video Converter](https://github.com/triwahyu45/ESP32-OLED-Video-Converter). It is not presented as an entirely original implementation. See [`ATTRIBUTION.md`](./ATTRIBUTION.md) for source details.

## Live demo

Open the converter in your browser:

**[Launch ESP32 OLED Video Converter →](https://nonchalantphoenix.github.io/boredphoenix-/)**

All video processing is performed locally in the browser. Your selected video is not uploaded by this page.

## Features

- Upload a local video in your browser
- Rotate the video by 90 degrees
- Use threshold, Bayer 8×8, Floyd–Steinberg, or Atkinson dithering
- Fit, cover, stretch, or manually scale the image
- Adjust FPS, thickness, threshold, contrast, brightness, and inversion
- Preview the result on a 128×64 monochrome canvas
- Generate `VideoFrame.h` bitmap output
- Copy a ready-to-adapt `Main.ino` example
- Support SSD1306 and SH1106 OLED displays
- Use the optional Wokwi simulation panel

## Quick start

1. Open [`index.html`](./index.html) or use the [live demo](https://nonchalantphoenix.github.io/boredphoenix-/).
2. Select a local video file.
3. Choose your OLED settings.
4. Preview the output.
5. Click **Extract Frames**.
6. Copy the generated data into a new Arduino IDE tab named `VideoFrame.h`.
7. Copy the generated sketch into `Main.ino`.
8. Install the required Adafruit libraries.
9. Select your ESP32 board in Arduino IDE.
10. Confirm your OLED wiring and I2C address before uploading.

## Hardware target

| Component | Target |
|---|---|
| Microcontroller | ESP32 development board |
| Display | 128×64 I2C OLED |
| OLED controllers | SSD1306 or SH1106 |
| Typical I2C address | `0x3C` — verify on your module |
| Arduino libraries | Adafruit GFX, Adafruit SSD1306, or Adafruit SH110X |

The generated video data can use significant flash memory. Start with a short, low-FPS video before increasing the number of frames.

## Repository contents

```text
.
├── index.html
├── donate-widget.js
├── thumbnail.jpg
├── project-banner.svg
├── README.md
└── ATTRIBUTION.md
