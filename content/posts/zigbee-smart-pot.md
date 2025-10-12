---
title: "Zigbee Smart Pot"
date: "2025-09-07"
description: "3D-Printed, self-watering Smart Pot controlled via Zigbee!"
summary: "."
tags: ["zigbee", "esp32", "home assistant"]
categories: ["Smart Home"]
draft: true
cover:
  image: "/images/bedOccupancy1.jpeg"
  relative: false
---

---

One of the common frustrations with smart home automation is when routines trigger at inconvenient or unintended times. For example, I have daily morning and evening automations that activate at fixed times, regardless of whether anyone is actually in bed. This often means the routines either run when no one is in bed or too late after someone has already settled in, forcing me to trigger them manually.

To solve this, I implemented an inexpensive and reliable bed occupancy sensor. Using a compact ESP32-C3 Super Mini board combined with a long Force Sensitive Resistor (FSR), I implimented a cheap and reliable solution to detect when someone is in bed. This allows me to run my routines exactly when I want them as well as new automations such as turning on the LED strip under my bed if I get up during the night.

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

