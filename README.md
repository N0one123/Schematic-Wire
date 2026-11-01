# THIS IS AN AI VIBE PROJECT!!!

# Schematic Wire

A browser-based schematic editor and early circuit simulator.

## Run
Open `index.html` in a modern browser. No build step or server is required.

## Controls
- Click a component in the library, then click the canvas to place it.
- Left-drag a component to move it.
- Drag from one pin to another to create a wire.
- Right-drag to pan; mouse wheel to zoom.
- Select a component to edit its reference and value.
- Use **Load example** for a small source/resistor/LED circuit.
- Press **Run** for the current DC operating-point solver.

## Current simulation scope
The initial solver supports resistive networks and ideal DC voltage sources using modified nodal analysis. The library includes visual placeholders for a wider range of components; not every listed component has a physical model yet. AC, transient, nonlinear semiconductor, and digital logic simulation are future work.

## Project direction
A clean, direct schematic workspace with a broad component library and progressively deeper simulation models.
