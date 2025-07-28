
# PICAXE-Powered Automatic Braking System

A self-contained automatic braking system for model vehicles, built using PICAXE microcontrollers and digital logic gates. This project uses binary logic and sensor input to activate a braking mechanism and display proximity warnings via LEDs.

## Overview

This braking system is designed to demonstrate basic embedded control, logical processing, and safety feedback mechanisms using simple hardware. It uses a PICAXE 08M2+ and PICAXE 14M2 to process inputs and drive outputs including a traffic light-style LED warning system and an analogue servo for braking.

| Distance to Object | Motor State | Buzzer State | System Response          |
|--------------------|-------------|--------------|---------------------------|
| > 50 cm            | stopped     | Off          | Normal operation          |
| 34–50 cm           | Stopped     | Off          | Warning stage             |
| < 34 cm            | Running     | On           | Emergency braking         

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


## Development Diary

### Research Stage
1. Researched Existing Systems and created an initial research page
2. Explored the use of an ultrasonic sensor versus LDR
3. Studied about the use of different buzzers and loudspeakers and their viability
4. Analysis of all inputs, processes and anaylsis.
5. Final Analysis of research
### Specification
•	Power Supply will be 6V. 4 AA batteries.
-	Enough voltage for the ultrasonic sensor to be triggered.	
•	Current Output will be 135mA – 150mA.
-	To ensure car battery lifespan.
•	The Ultrasonic sensor must be triggered and controlled by a PIC.
-	This is because it needs to be triggered to start detecting before the brake is  
•	System will be armed once distance to object is ¾ of a metre.
-	To ensure comfortable braking distances
•	A servo will activate the braking mechanism.
-	A servo has the same plane of motion as a wheel.
•	Buzzer must buzz at 400Hz
-	To create an effect of severity.
•	LED’s must be on before 1 metre before collision.
-	To give driver time to react
•	There will be 3 LED’S
-	As you get closer to the object the different LED’s turn on to show severity

## Circuit Generation & Analysis

The first official draft of the circuit diagramand comprehensive analysis of each subsystem and their role in the larger system. Embellished with minor analysis of the BOOLEAN logic and output signals of the Microcontroller. Finally a showcase of conditions and outputs for the servo.

## Progression 

Visual representation of the process of seting up the complete functional breadboard. With a final product after development.

## Testing & Analysis

Testing signals using multimeters and an oscilloscope.

## Potential for development

## Function Desc

My circuit uses an Ultrasonic Range finder to measure and calculate distance between itself and an object. The signal it produces is used buy a PIC to control an array of logic which in turns can turn on three LED’s: Green, yellow, red (increasing in danger). If danger is close enough to trigger the red LED. A second PIC is triggered and controls an electromagnetic servo to act as a braking mechanism. This whole process is fully automated as it doesn’t require any input from the driver.

## License

This project is open-source and intended for educational and non-commercial use.
