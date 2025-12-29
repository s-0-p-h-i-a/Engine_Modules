# ECU-Inspired Engine Timing Prototype

## Overview

This project is a **simplified ECU firmware prototype** focusing on engine timing, RPM calculation, and cylinder visualization. The emphasis is on **system design, integration, debugging, and observing system behavior** rather than physical engine simulation.

---

## Hardware

* Arduino MCU (ECU side)
* Flywheel (servo with a magnet)
* Hall sensor for RPM calculation
* Breadboard LED matrix for cylinder visualization
* Joystick for control

---

## Project Status & Next Steps

* **V0**: fully functioning version, verified and validated hardware integration. Documentation coming soon
* **V1 (WIP)**: ongoing semantic rework, adding in-code comments, and localised logic / architecture refactors

---

## Code Architecture

* **Flywheel module**			: tracks angle and speed
* **Hall sensor module**		: provides timing events
* **RPM calculation**			: converts timing data to speed
* **Cylinder module**			: computes cylinder state
* **Cylinder visualization**	: breadboard LED output
* **Joystick module**			: reads joystick input
* **Drive module**				: on/off and speed control for the flywheel and cylinder
* **Plotter interface modules**	: expose processed subsystem data for plotting and diagnostics.
* **Plotter module**			: displays data on serial plotter

Modules are designed to be testable in isolation, with integration exposing timing and logic issues for refinement.

---

## Next Steps

* **Fault injection**: timing lag, jitter, dropped events, snapshot logging
* **Expanded engine structure**: crank + cylinder head module with DOHC, valves, injectors, plugs
* **CAN integration**: second MCU handles user input and logging

Additional documentation, diagrams, demos, and design notes will be added as the project evolves.
