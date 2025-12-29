# ICE Engine Simulations (WIP / PoC)

A collection of learning-focused engine simulation projects in C/C++ and Arduino. These early-stage experiments explore state-machine logic, modular design, and hardware abstraction through CLI and LED-based prototypes. Projects are conceptual and work-in-progress, demonstrating understanding of engine sequencing and embedded systems thinking. They will be iteratively refined and expanded over time.

**Fully functional:** CLI crankshaft simulation.

**Current WIPs:** cylinder and crankshaft simulations.

**Long-term goal:** add DOHC camshafts, fuel injection and spark plug projects, merge into simple Moore machine-like simulation of inline-4 engine control.

---
## Overview

Current projects include:

1. **[Mini Engine Control Embedded Sytem](./Full_Engine)**

	- Ongoing ECU firmware-inspired engine control / behaviour simulation.
	- Combines previously developed servo + Hall sensor flywheel RPM calculation and LED cylinder visualisation "modules". User controls engine on/off and chooses speed setting via joystick.
	- More modules will be progressively integrated: crank, cam, valves, etc.

2. **[Arduino 1-Cylinder Simulation (v0 WIP)](./1_Cylinder)**
    
    - Simulates one cylinder moving through combustion cycle using LEDs and a breadboard.

3. **[Inline-4 Crankshaft Simulations, CLI (functional v0) and Arduino (WIP / PoC)](./Inline4_Crankshaft)**

	- Functional CLI "sandbox" version for practice, using ASCII visuals to represent side view of the crankshaft.

4. **[Inline-4 Engine CLI Simulation (v0 WIP / PoC)](./Engine_Cycle_CLI)**
    
    - A command-line C application simulating a 4-stroke inline-4 engine via text output.

    - Implements a Moore-style finite state machine and a basic firing order (1-3-4-2).

4. **Arduino 4-Cylinder Simulation (Planned)**
    
    - Expansion on the 1-cylinder project, simulating an inline-4 engine using an LED matrix.

6. **Camshafts Simulation (Planned)**
    
    - Simulate valve distribution control in an inline-4 DOHC engine.

7. **Fuel & Spark Simulation (Planned)**
    
    - Simulate fuel injector and spark plug control.

---
## Structure

Each project is contained in its own folder (`v0/PoC`) to clearly separate work-in-progress experiments.

Each project uses modular C/C++ structure, separating state representation, output handling, and core logic to mimic embedded systems best practices.

---
## Learning Goals / Roadmap

- Practice C/C++ programming: structs, enums, arrays, loops, and modular design.

- Explore state-machine logic (Moore and composite multi-lobe concepts).

- Build hardware abstraction awareness via Arduino simulations.

- Iteratively refine projects over time:

    - Enhance timing and cycle accuracy

    - Introduce pointers and dynamic state management

    - Expand LED-based visualizations to multiple cylinders

    - Simulate more realistic engine events (misfires, spark/fuel timing, valve overlap)

---
## Notes

- Projects may be intentionally verbose and are structured for learning and experimentation, not production or real-time control.

- Conceptually models engine behavior and embedded logic, but does not simulate real engine dynamics or timing.

- The repository serves as a portfolio of embedded and simulation concepts, showing progression and understanding of engine control fundamentals.
