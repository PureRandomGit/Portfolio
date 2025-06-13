---
title: "Smart Blinds"
date: "2025-01-01"
description: "Cheap, simple and effective smart blinds made from and old IKEA roller shades and a few electronic components."
summary: "Cheap, simple and effective smart blinds made from and old IKEA roller shades and a few electronic components."
tags: ["esphome", "esp32", "home assistant"]
categories: ["Smart Home", "syntax"]
---

---

I wanted an automated blind solution that wouldn't rely on cloud services or expensive commercial products. By repurposing an IKEA roller shades and designing my own controller system, I was able to build a cheap local solution.

## Hardware
The smart blind consists of four main components:

- **28BYJ-48 stepper motor**
- **ULN2003 stepper motor driver board**
- **ESP32 microcontroller**
- **IKEA roller shade**

I chose these because they were very cheap off of Amazon or Aliexpress and because the ULN2003 was supported by Esphome's stepper component which I was planning on using to program the esp32.

## 3D-Printed Case
To mount and house the motor and eletronics I designed a 3d printed case in Fusion360. This was my first time cading gears so it took me a bit to get the correct gear ration that would allow the motor to have enough torque to raise the blinds without skipping. After that it was just a matter of blocking out where each component would go and build the case around them.

## Wiring
The wiring for the ULN2003 was rather straight forward and only needed 4 wires connected to the esp32 and then power and ground for both the  driver and esp32

## Software
To test that everything was working I wrote a quick arduino program to spin the motor in both directions for a few seconds. After confirming my wiring was correct and the code ran I started to write the Esphome code. During this process, I discovered that RoadKillUK had published a [Github](https://github.com/RoadkillUK/Motor-on-a-Roller-Blind-for-ESPHOME) that was very similar to what I was trying to accomplish. I only had to modify the code slightly to work with an esp32 but it was pretty much perfect.

## Usage & Future Improvements
I've been running the blind for a little over a year now and have had no issue with it so far. There are a few things that I would change if I made a second version. First, the blinds are slow, they take over a minuet to raise/lower about 3 feet. Second, the stepper motor loses its memory of the blind position if it loses power and will need to be re-homed.

---

