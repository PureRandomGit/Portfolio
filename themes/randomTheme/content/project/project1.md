---
title: "ESP32 Super Mini Occupancy Sensor"
date: 2024-11-12
tags:
  - ESPHome
  - Home Assistant
  - Sensor
draft: false
---
The ESP32-C3 Super Mini is a compact, cost-effective solution for IoT projects, and its low power consumption makes it ideal for continuous monitoring applications. When paired with a Force Sensitive Resistor (FSR) and ESPHome, it can be transformed into a reliable bed occupancy detector.
Why Use an FSR for Bed Occupancy?

FSRs are pressure-sensitive components that change resistance based on applied force, making them perfect for detecting presence on a surface like a bed. Combined with the ESP32-C3, they offer a simple and scalable way to track occupancy without invasive or complex setups.
Components Required

## ESP32-C3 Super Mini
FSR (e.g., Interlink FSR 400 series)
Resistor (e.g., 10 kΩ for a voltage divider circuit)
Breadboard or PCB for prototyping
Power supply (USB or battery)
ESPHome installed on the ESP32-C3

## Circuit Setup
Connect the FSR in series with a 10 kΩ resistor to form a voltage divider.
Attach the junction of the FSR and resistor to an ADC pin on the ESP32-C3.
Connect the other ends of the FSR to 3.3V and GND.
Power the ESP32-C3 through USB or a battery source.