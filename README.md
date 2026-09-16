# ESP32 OLED Video Converter — English Adaptation

This is an **English-language adaptation inspired by** [Tri Wahyu's ESP32 OLED Video Converter](https://github.com/triwahyu45/ESP32-OLED-Video-Converter). The interface text and documentation were converted into English for easier use by English-speaking makers.

It runs in the browser and converts uploaded video frames into monochrome C/C++ bitmap arrays for ESP32 projects using 128×64 SSD1306 or SH1106 OLED displays.

## Features

- Upload a local video in the browser
- Rotate the video by 90 degrees
- Choose threshold, Bayer, Floyd–Steinberg, or Atkinson dithering
- Fit, cover, stretch, or manually scale the image
- Adjust FPS, thickness, threshold, contrast, brightness, and inversion
- Preview the result on a simulated 128×64 OLED canvas
- Generate `VideoFrame.h` data for Arduino IDE projects
- Copy a ready-to-adapt `Main.ino` example

## How to use

1. Open `index.html` in a modern browser.
2. Choose a local video file.
3. Select the OLED size and conversion settings.
4. Preview the frames.
5. Click **Extract Frames**.
6. Copy the generated array into `VideoFrame.h`.
7. Copy the main sketch into `Main.ino`.
8. Install the required Adafruit libraries in Arduino IDE and select either SSD1306 or SH1106 in the sketch.

## Hardware target

The generated example targets an ESP32 connected to a 128×64 I2C OLED module. It supports common SSD1306 and SH1106 variants at I2C address `0x3C`; confirm your module's controller, voltage, wiring, and address before powering it.

## Attribution

This project was **converted into English and inspired by** the original work. It is not presented as an entirely original project. See [`ATTRIBUTION.md`](./ATTRIBUTION.md) for source links and provenance. Please consult the upstream repository for the authoritative version, current license terms, and updates.
