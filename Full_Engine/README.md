# Flywheel & LED Cylinder Mini Embedded System

## Overview

This project simulates an engine + flywheel system controlled via a joystick, with LED cylinder visualization and Hall sensor RPM feedback. It is structured as a modular “mini embedded system” with separate hardware interface modules and logic modules.

This project is the first step towards building a more complete Arduino-based inline-4 engine simulation, integrating a crankshaft and DOHC camshafts.

Present code is all WIP, v0 will be pushed when basic functionality is achieved.

---
## Current Status: Rebuild

- 1st draft built successfully on Arduino CLI.

- Hardware integration and live verification testing: system is responsive but desired behaviour was not achieved.

- Rebuilding from the inside out: isolated module causing issues (cylinder header), rewriting/refactoring to address them

---
## Modules

- **Drive, Cylinder, CylinderVisuals** – handles engine logic and LED display

- **Flywheellib** – flywheel simulation and dynamics

- **Halllib** – Hall sensor input interface

- **Joystick** – joystick input abstraction

- **Servolib** – servo control

- **Rpmlib** – RPM calculation

- **Plotter** – serial output for visualization/debugging

- **Global** – shared timing variables (`now`, `timewindow`)

---
### Design Notes

- Logic and internal objects (`.c` modules) are hardware-agnostic and can be tested independently of Arduino.

- Hardware interface modules (`.cpp`) handle Arduino-specific functionality like LEDs, servos, and serial I/O.

- Clear separation of concerns allows safe refactoring and modular testing.
