
# PICAXE-Powered Automatic Braking System

A self-contained automatic braking system for model vehicles, built using PICAXE microcontrollers and digital logic gates. This project uses binary logic and sensor input to activate a braking mechanism and display proximity warnings via LEDs.

## Overview

This braking system is designed to demonstrate basic embedded control, logical processing, and safety feedback mechanisms using simple hardware. It uses a PICAXE 08M2+ and PICAXE 14M2 to process inputs and drive outputs including a traffic light-style LED warning system and an analogue servo for braking.

## Features

- Traffic-light-style warning system using red, amber, and green LEDs
- Automatic braking using an analogue servo when an object is dangerously close
- Binary logic implementation using NOT and AND gates (4049 and 4081)
- PICAXE BASIC code structure for simplicity and modularity
- Suitable for educational use and model car demonstrations
- Servo calibration included and refined in firmware

## Hardware Used

| Component             | Quantity |
|-----------------------|----------|
| PICAXE 08M2+          | 1        |
| PICAXE 14M2           | 1        |
| NOT Gate (IC 4049)    | 1        |
| AND Gate (IC 4081)    | 1        |
| 10kΩ Resistor         | 1        |
| 330Ω Resistors        | 3        |
| Red LED               | 1        |
| Yellow LED            | 1        |
| Green LED             | 1        |
| Analogue Servo        | 1        |
| Breadboard and Wires  | Various  |
| Power Supply (4.5–6V) | 1        |

## System Logic

The system processes digital inputs corresponding to proximity thresholds. The 08M2+ handles binary evaluation while the 14M2 drives the output devices. Logic gates (NOT and AND) simplify signal pathways to determine when to apply the brake and which LED to activate:

- Green LED indicates a safe distance
- Yellow LED indicates caution
- Red LED indicates danger and triggers the braking servo

## Calibration

Servo calibration is handled in software, and fine-tuning has been implemented in the firmware. Users can modify values in the code if different servo models are used or if response tuning is needed for specific braking mechanisms.

## Applications

- Safety systems for model vehicles
- Robotics and embedded control demonstrations
- Education: introduction to logic gates, microcontroller programming, and servo actuation
- Prototyping for automotive safety concepts

## Known Limitations

- Inconsistent detection at certain angles or with non-reflective objects
- Servo braking speed may not be sufficient for fast-moving systems
- Logic gate operation depends on clean digital signals; noise may affect behavior

## Getting Started

1. Assemble the circuit based on the provided schematic (not included in this file).
2. Program both PICAXE microcontrollers using the PICAXE Editor and BASIC files.
3. Connect a stable 4.5V–6V power supply.
4. Place objects at various distances and observe LED transitions and braking behavior.

## License

This project is open-source and intended for educational and non-commercial use.
