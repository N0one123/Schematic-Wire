# Schematic Wire

A browser-based schematic editor and an early, time-stepped circuit simulator.

## Run
Open `index.html` in a modern browser. No build step or server is required.

## Editor controls
- Click a component in the library, then click the canvas to place it.
- Left-drag a component to move it.
- Drag from one pin to another to create a wire; click one pin and then another also works.
- Repeating the same pin-to-pin connection toggles that wire off; connecting it again restores it.
- Right-drag to pan; mouse wheel to zoom.
- Select a component to edit its reference and value.
- Use **Load example** to load a sample schematic.

## Wiring
Wires use orthogonal grid routing. The router treats component bodies and previously routed wires as obstacles, and recalculates routes when components move. Pins are placed at component edges. Breadboard holes are individually connectable, with five-hole strips and power rails modelled as internally connected groups. Very dense layouts may still need components to be moved to create routing space.

## Electrical simulation
The Run button starts a time-stepped modified-nodal-analysis solver. Current electrical models are implemented for:
- Resistors and potentiometers
- DC voltage sources and a 50 Hz AC voltage source
- Diodes, LEDs and zener diodes (piecewise-linear approximation)
- Capacitors (backward-Euler transient model)
- Open/closed switches, push buttons, toggle, slide and rocker switches
- Simple resistive approximations for lamps, motors and speakers

The solver reports node voltages and branch currents, and component indicators respond to simulated branch current. Capacitor state evolves while the simulation runs.

## Important limitations
This is **not a full SPICE replacement**. Transistors, op-amps, logic gates, microcontrollers, sensors, displays, motor drivers, battery chemistry, and most modules are currently schematic/visual placeholders and do not yet have functional electrical models. The lamp, motor and speaker models are simple resistive approximations. AC analysis is a basic 50 Hz time-domain source, not frequency-domain analysis. Do not use this prototype for safety-critical or real-world electrical design.

## Library
The library contains common passive parts, semiconductors, boards, sensors, actuators, power modules, switches, displays, instruments, and connectors. Some entries are generic visual representations rather than exact manufacturer footprints or pinouts.

## Project direction
A clean, direct schematic workspace with reliable orthogonal wiring and progressively deeper, verifiable simulation models.
