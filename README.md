**# Flight-Controller-OMO

A custom designed, minimalistic STM32F411-based flight controller built from scratch for custom drone and aerospace experimentation.

## What is this project?

Flight Controller OMO: is a custom printed circuit board (PCB) designed specifically to act as the central processing and stabilization unit for small quadcopters and stabilising platforms. It breaks away from bulky flight controllers by packing only the essential, minimal form factor powered by an STM32 microcontroller and a modern BMI270.

## Purpose & What it does

The primary purpose of this board is to process real-time orientation data and translate pilot control inputs into precise motor commands. 
- Attitude Stabilization: Reads high speed gyro and accelerometer data via the BMI270 sensor to keep the aircraft stable.
- Motor Control: Provides 4 dedicated motor output attachments to drive electronic speed controllers (ESCs) or micro motors.
- Open Firmware Compatibility: Designed to run standard flight controller firmware like Betaflight.
- Telemetry: Includes a 12 pin USB-C interface for seamless connection to a PC for configuration and flashing.

## Why does it exist?

Building an off the shelf drone is fun, but designing the core avionics from the ground up teaches you how hardware, firmware, and circuit layout actually interact in the real world. 

- The Learning Curve: Moving away from older, obsolete sensors like the MPU6050 to the modern BMI270 was a major step in modernizing the design.
- Aerospace Passion: As a personal stepping stone for aerospace and rocketry drone payloads having total control over a custom flight controller design opens up endless possibilities for tailored form factors.
- Just for Fun: Pure engineering curiosity testing whether a self routed PCB built in KiCAD can successfully boot, communicate, and stabilize a flight platform. (As of now, it's a first prototype fingers crossed that everything works as intended!)

## Bill of Materials (BOM)

| Item | Quantity | Total Price | Link | Description |
| :--- | :---: | :---: | :--- | :--- |
| STM32F411CEUx | 1 | — | [Manufacturer](https://www.st.com/) | Microcontroller core |
| BMI270 | 1 | — | [Bosch Sensortec](https://www.bosch-sensortec.com/) | Gyro & Accelerometer Sensor |
| USB-C Receptacle | 1 | — | [AliExpress / Supplier](https://de.aliexpress.com/) | Power & Data Connection |
| Custom PCB | 1 | 15,00 € | [JLCPCB](https://jlcpcb.com/) | Custom designed circuit board |


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

## Bonus

Before settling on the BMI270, early iterations used the older MPU6050. Transitioning away from it was a major hurdle due to its age and lack of modern integration support, making the shift to the BMI270 a much cleaner and more reliable choice for modern layouts.

<img width="431" height="397" alt="Old MPU6050 Iteration" src="https://github.com/user-attachments/assets/0b2d92ee-48ac-4365-8c29-1a148eaae829" />**
