# 🌀 8-bit Barrel Shifter – Verilog Implementation on Basys 3 FPGA

This project implements an **8-bit barrel shifter** using Verilog HDL, deployed and tested on the **Basys 3 FPGA development board**. The design performs **right rotation (circular shift)** of input bits based on a 3-bit shift amount. This is useful in various digital signal processing and cryptographic applications.

---

## 📐 Functionality

The barrel shifter takes:

- `a` (8-bit input vector)
- `amt` (3-bit shift amount: `000` to `111`)
- Outputs `y` (8-bit result), which is the **right-rotated** version of `a` by `amt` positions.

### 👉 What is Right Rotation?

A **right rotation** moves all bits to the right, and the least significant bits wrap around to the front.

#### Example:
Input (a): 8'b10110010<br/>
Shift Amt : 3<br/>
Output (y): 8'b01010110<br/>


Here, the lower 3 bits are rotated to the MSB side.

---

## 🔧 Hardware Setup (Basys 3)

The design is implemented on the **Basys 3 FPGA board** with the following mapping:

| Component | Function              |
|----------:|-----------------------|
| SW0–SW7   | 8-bit input `a`       |
| SW13–SW15  | 3-bit shift amount    |
| LED0–LED7 | 8-bit output `y`      |

You can rotate the input bits using switches `SW8–SW10`, and observe the result via the onboard LEDs.

---

## 📁 File Structure
📂 barrel_shifter<br/>
├── barrel_shifter.sv # Barrel shifter module (core logic)<br/>
├── constraints.xdc # Xilinx constraints file for pin assignments<br/>
├── schematic.png<br/>
├── FPGA Implementation,mp4<br/>
├── barrel_shifter.bit  # (Optional) Bitstream file for programming FPGA<br/>
└── README.md # This documentation<br/>







