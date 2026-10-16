# Flight-Controller-OMO

A custom designed, minimalistic STM32F411-based flight controller built from scratch for custom drone and aerospace experimentation.

## What is this project?

Flight Controller OMO: is a custom made circuit board designed specifically to act as an stabilization unit for stabilising platforms. It breaks away from bulky flight controllers by packing only the essential, minimal form factor powered by an STM32 microcontroller and a modern BMI270.

## Purpose & What it does

The primary purpose of this board is to process real-time orientation data and translate pilot control inputs into precise motor commands. 
- Attitude: Reads high speed gyro and accelerometer data via the BMI270 sensor to keep the aircraft stable.
- Motor Control: Provides 4 dedicated motor output attachments to drive electronic speed controllers (ESCs) or micro motors.
- Firmware: Designed to run standard flight controller firmware like Betaflight.
- Flashing: Includes a 12 pin USB-C interface for seamless connection to a PC for configuration and flashing.

## Why does it exist?

Building an off the shelf drone is fun, but designing the core avionics from the ground up teaches you how hardware, firmware, and circuit layout actually interact in the real world. 

- The Learning Curve: Moving away from older, obsolete sensors like the MPU6050 to the modern BMI270 was a major step in modernizing the design.
- Aerospace Passion: As a personal stepping stone for aerospace and rocketry drone payloads having total control over a custom flight controller design opens up endless possibilities for tailored form factors.
- Just for Fun: Pure engineering curiosity testing whether a self routed PCB built in KiCAD can successfully boot, communicate, and stabilize a flight platform. (As of now, it's a first prototype fingers crossed that everything works as intended!)

## Bill of Materials

| Designator | Component / Value | Footprint / Package | LCSC Part Number | Description / Notes |
| :--- | :--- | :--- | :--- | :--- |
| U2 | STM32F411CEU6 | QFN-48 (7x7mm) | C60420 | Main MCU |
| U4 | BMI270 | 14-LGA (3x2.5mm) | C2836813 | Gyro + Accel |
| U3 | ME6211C33M5G-N | SOT-23-5 | C82942 | 3.3V Voltage Regulator |
| J1 | USB4105-GF-A-120 | USB-C 16-Pin SMT | C5184243 | USB-C Receptacle |
| Y1 | 16MHz Crystal | SMD 3225-4P | C13738 | Crystal Oscillator |
| C5, C6 | 10µF | 0603 (1608 Metric) | C19702 | Ceramic Capacitor |
| C7 | 2.2µF | 0603 (1608 Metric) | C23630 | Ceramic Capacitor |
| D1, D2 | LED | 0603 (1608 Metric) | C2290 | Status / Power LEDs |
| R3 | 1MΩ | 0603 (1608 Metric) | C22935 | Resistor |
| R4, R5 | 5.1kΩ | 0603 (1608 Metric) | C23186 | USB-C Resistors |
| R6, R7 | 10kΩ | 0603 (1608 Metric) | C25804 | Config Resistors |
| R8, R9 | 1kΩ | 0603 (1608 Metric) | C21190 | LED Current Limiting Resistors |

## Tools & Technologies

- PCB Design: KiCAD
- Firmware: Betaflight
- Design Highlights: Features a custom silkscreen layout including things like Mewo.

## Schematics & PCB Layout

## Schematic

<img width="525" height="641" alt="Schematic Overview" src="https://github.com/user-attachments/assets/f63c56b4-273c-4061-a75c-507f337dad24" />
<img width="544" height="262" alt="Power & MCU Details" src="https://github.com/user-attachments/assets/98c3d2bc-819a-4625-8390-9b1c7c13e985" />

## PCB

<img width="590" height="470" alt="PCB Top View" src="https://github.com/user-attachments/assets/beaa8b7b-2234-4282-ad69-a504e8533080" />
<img width="590" height="470" alt="PCB Bottom View" src="https://github.com/user-attachments/assets/41b5ce0c-abc6-49dc-96f1-d5257a507132" />

## Extras

I liked this way more than id like to admit making this was really fun for me and it was just so freeing.

## Bonus

Before settling on the BMI270, early iterations used the older MPU6050. Transitioning away from it was a major hurdle due to its age and lack of modern integration support, making the shift to the BMI270 a much cleaner and more reliable choice for modern layouts.

<img width="431" height="397" alt="Old MPU6050 Iteration" src="https://github.com/user-attachments/assets/0b2d92ee-48ac-4365-8c29-1a148eaae829" />
