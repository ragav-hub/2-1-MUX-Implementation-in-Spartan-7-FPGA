# 4:1 Multiplexer Implementation in Spartan-7 FPGA

## Aim
To design, simulate, synthesize, and implement a 4:1 Multiplexer using Verilog HDL on a Spartan-7 FPGA using Xilinx Vivado Design Suite.

---

## Apparatus Required
| S.No | Apparatus / Software | Specification / Description |
|------|----------------------|-----------------------------|
| 1 | FPGA Board | Xilinx Spartan-7 development board (modify pin names for your board) |
| 2 | Software | Xilinx Vivado Design Suite 2023.1 or later |
| 3 | Cable | USB Programming Cable (JTAG/USB-JTAG) |
| 4 | Power Supply | As required by the development board |
| 5 | Accessories | Breadboard/wires (optional), LEDs and switches present on board used for I/O |

---

## Theory
A **4:1 multiplexer** selects one of four data inputs (D0..D3) and routes it to a single output Y, based on two select lines S[1:0].

**Truth table**

| S1 | S0 | Y   |
|----|----|-----|
| 0  | 0  | D0  |
| 0  | 1  | D1  |
| 1  | 0  | D2  |
| 1  | 1  | D3  |

**Logic Diagram:**
<img width="463" height="368" alt="image" src="https://github.com/user-attachments/assets/7e2b9a82-5482-4265-8007-4c3761706314" />

---

## Procedure (Vivado Design Suite)

1. **Create Project**
   - Open Vivado → *Create New Project*.
   - Name project `MUX_4to1_Spartan7`. Select *RTL Project*, enable *Do not specify sources at this time* (or add immediately).
   - Choose the correct Spartan-7 device/board for your hardware.

2. **Create Design Source**
   - Flow Navigator → *Add Sources* → *Add or Create Design Sources*.
   - Create file `mux4to1.v` and type the Verilog code.

3.  **Add Constraints**
   - Add XDC file `mux4to1.xdc` and map inputs/outputs to board pins.

4.  **Synthesize & Implement**
   - Run *Synthesis* → inspect warnings/errors.
   - Run *Implementation* → review timing and utilization.

7. **Generate Bitstream & Program**
   - Generate Bitstream.
   - Open *Hardware Manager* → connect to target → Program device with `.bit` file.
   - Verify outputs on LEDs/scope.
---
## Verilog Program (`mux4to1.v`)

```verilog
`timescale 1ns / 1ps
module mux4to1 (
    input  wire d0,
    input  wire d1,
    input  wire d2,
    input  wire d3,
    input  wire [1:0] sel,
    output wire y
);
    //
--
--
--

   endmodule
```
## Constraint file for Seven-Segment Display
```

```
## FPGA Implementation Output




---

## Conclusion

The 4:1 multiplexer was successfully designed,synthesized, and implemented (bitstream generated) in the Spartan-7 FPGA. The output matches the expected truth table.
