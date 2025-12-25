---
title: "Bed Occupancy Sensor"
date: "2025-01-01"
description: "Low cost bed occupancy sensor made with an esp32-c3 super mini and a $10 resistor."
summary: "Low cost bed occupancy sensor made with an esp32-c3 super mini and a $10 resistor."
tags: ["esphome", "esp32", "home assistant"]
categories: ["Smart Home"]
cover:
  image: "/images/bedOccupancy1.jpeg"
  relative: false # To use relative path for cover image, used in hugo Page-bundles
---

---



## Hardware

- ESP32-C3 Super Mini
- Force Sensitive Resistor (FSR)
- 10K ohm Resistor

## 3D-Printed Case
As I often use ESP32-C3 Super Minis in a lot of my projects due to their extremely small size I had already designed a slim case for them which worked prefectly for this application. The case can be found **[here](https://makerworld.com/en/models/797722-esp32-c3-super-mini-slim-case#profileId-737146)** on my **[MakerWorld Profile Page](https://makerworld.com/en/@PureRandom)**.

## Wiring
The wiring was very simple, I just soldered one pin of the FSR to 3.3v and then the other pin to a analog pin, in my case pin 4, with the resistor connecting pin 4 and ground.

![ESP32-C3 Super Mini with resistor and wires](/images/bedOccupancy2.jpeg)

## Software
Using Esphome I wrote a basic yaml code to publish a resistor value as well as a binary occupancy value to HomeAssistant that can be found **[here](https://github.com/PureRandomGit/Esp32-Bed-Occupancy-Sensor/tree/main)**.

---

