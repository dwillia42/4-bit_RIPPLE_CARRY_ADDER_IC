# 4-bit_RIPPLE_CARRY_ADDER_IC
The transistor level schematic and layout of a 4-bit Ripple Carry Adder, capable of both addition and subtraction.

# 4-Bit Signed Ripple Carry Adder (Electric VLSI)

## Overview

This project implements a transistor-level 4-bit signed Ripple Carry Adder (RCA) using CMOS logic in Electric VLSI.

The design was developed hierarchically, beginning with the fundamental XOR gate and CMOS full adder to a complete 4-bit arithmetic circuit. Functional verification and timing analysis were performed using SPICE simulations.

## Project Objectives

- Design CMOS logic circuits at the transistor level.
- Develop a hierarchical arithmetic circuit using reusable building blocks.
- Create corresponding layouts in Electric VLSI.
- Verify functionality through SPICE simulation.
- Analyze propagation delays and circuit behavior.

## Design Hierarchy

```text
XOR Gate
      ↓
Full Adder
      ↓
4-Bit Signed Ripple Carry Adder
```

## Components

### XOR Gate
The project uses the CMOS implementation of a XOR gate 
- XOR
- Inverter (in the xor gate implementation)

These gates serve as the foundation for higher-level arithmetic blocks.

### Full Adder

The Full Adder expands on the Half Adder by accepting:

- Input A
- Input B
- Carry-In

and producing:

- Sum
- Carry-Out

### 4-Bit Signed Ripple Carry Adder

Four Full Adders are connected in series to form a 4-bit Ripple Carry Adder.

One of the addition operands is XOR'd with a mode bit (M)

The carry output from each stage propagates to the next stage, allowing multi-bit addition.

To perform addition, the mode bit is set to 0.

To perform subtraction, the mode bit is set to 1 (twos-complement)

## Design Methodology

The project was created using Electric VLSI and follows a hierarchical design approach:

1. Design transistor-level xor gate schematic and layout.
2. Design transistor-level full adder schematic and layout.
3. Assemble four Full Adders and xor gates into a signed 4-bit Ripple Carry Adder.
4. Perform SPICE simulations for verification and timing analysis.

## Verification

Functional verification was performed through SPICE simulations.

Tests included:

- Logic verification
- Arithmetic verification
- Carry propagation behavior
- Propagation delay measurements

## Repository Contents

```text
4-bit_RCA.jelib
```

Contains all schematics, layouts, cell definitions, and project hierarchy developed in Electric VLSI.

```text
screenshots/
```

Contains images of:

- Transistor Layouts and Schematics
- Simulation results

## Tools Used

- Electric VLSI
- IRSIM
- LTspice / SPICE Simulation

## Key Concepts Demonstrated

- CMOS transistor-level design
- Hierarchical circuit design
- Layout generation
- Arithmetic circuit implementation
- Carry propagation
- Timing and delay analysis
- Digital VLSI design methodology

## Author

Dwann Williams  
Computer Engineering Student  
The City College of New York
