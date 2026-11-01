# Schematic Wire

A browser-based schematic editor and early circuit-simulation prototype.

## Run
Open `index.html` in a modern browser. No build step or server is required.

## Editor controls
- Click a component in the library, then click the canvas to place it.
- Left-drag a component to move it.
- Drag from one pin to another to create a wire.
- Repeating the same pin-to-pin connection toggles that wire off; connecting it again restores it.
- Right-drag to pan; mouse wheel to zoom.
- Select a component to edit its reference and displayed value.
- Use **Load example** to load a sample schematic.

## Library
The library is grouped into passive components, semiconductors, development boards, sensors, motors and actuators, power modules, switches and interfaces, displays, instruments, and prototyping connectors. It includes many common hobby parts and module families.

## Visual simulation
When Run is active, wires receive animated current-style particles and voltage-style highlighting, and component symbols receive running-state effects. These are currently visual indicators, not measured per-wire current direction or per-component voltage.

## Electrical simulation scope
The current DC operating-point solver is an early implementation for resistive branches and ideal DC voltage sources. The broader component library is not yet fully electrically modelled. AC/transient analysis, nonlinear diode/transistor models, digital logic execution, microcontroller firmware, sensor behaviour, and motor dynamics are future work. Do not treat this prototype as an engineering validation or safety tool.

## Project direction
A clean, direct schematic workspace with a broad component library, obstacle-aware orthogonal wiring, and progressively deeper simulation models.
