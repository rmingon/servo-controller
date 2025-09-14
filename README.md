# Dual Servo Test Board

This repository contains the design files, schematics, and PCB layout for a compact, custom-made dual-servo testing platform.
It is designed for engineers, makers, and robotics developers who need a reliable and convenient way to drive and test two RC servos simultaneously from a PC.

## Overview

This board is built around the ATmega328P microcontroller (the same MCU used in Arduino Uno), making it extremely flexible and easy to program.
Communication with the host PC is handled via an onboard CH340 UART-to-USB bridge, enabling simple plug-and-play connectivity over USB.

The board includes XT60 and XT30 connectors for safe and reliable power input, making it suitable for lab bench setups or battery-powered applications.

## Features

- Dual Servo Control  
  Two independent PWM channels allow you to control and test two RC servos simultaneously.
  
- Robust Power Delivery  
  - XT60 and XT30 connectors for battery/power input  
  - Onboard LM1117-5 voltage regulator for a stable 5V rail  

- USB-to-UART Interface  
  - CH340 USB-to-serial converter  
  - Direct connection to PC for programming and control

- Microcontroller  
  - ATmega328P running at 16 MHz  
  - Fully Arduino-compatible for easy firmware development  

- Test Points & Expandability  
  - Breakout headers for ISP programming  
  - Extra I/O pins available for debugging or future expansions  

## Connectors & Interfaces

| Connector | Function |
|----------|----------|
| XT60 | Primary power input (+BAT, GND) |
| XT30 | Secondary power option |
| USB-C | UART communication with PC |
| J3 | AVR-ISP programming header |
| J4 / J5 | Servo PWM outputs |

## Electrical Characteristics

| Parameter | Value |
|----------|-------|
| Input Voltage | 6 – 12 V (recommended) |
| Logic Voltage | 5 V |
| PWM Frequency | ~50 Hz (standard RC servo) |
| MCU Clock | 16 MHz |

## Software & Usage

1. Connect Power via XT60/XT30 (or USB for low-power testing).
2. Connect to PC via USB-C cable.
3. Flash firmware using the Arduino IDE or `avrdude` over ISP.
4. Use the provided PC software or your own serial commands to control PWM output and test servo movement.

## Project Files

This repository contains:
- KiCad PCB Layout (`hardware.kicad_pcb`)
- Schematic (`hardware.kicad_sch`)
- Project Configuration Files (`.kicad_pro`, `.kicad_prl`)
- 3D Render and PCB previews

## Applications

- Servo quality testing (batch verification)
- Robotics development and debugging
- Educational tools for learning PWM and MCU programming
- Rapid prototyping for motion-control projects

## Future Improvements

- Add current sensing for each servo channel  
- Optional I²C/UART expansion for external sensors  
- Integrate reverse-polarity protection on power input  
