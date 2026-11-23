
# 🚦 Traffic Light Controller using Verilog HDL

## FSM-Based Traffic Signal Control System using Artix-7 FPGA

---

## 📌 Project Overview

This project implements an automated traffic light control system using a Finite State Machine (FSM) in Verilog HDL.

The system is designed for the Nexys A7 Artix-7 FPGA development board. It controls traffic signals for two directions: North-South and East-West.

The controller operates using four different states to manage traffic signals. It provides GREEN, YELLOW, and RED indications for both directions based on a predefined timing sequence.

The system ensures that both directions never receive a GREEN signal simultaneously, improving traffic safety and controlling vehicle movement efficiently.

---

## ✨ Features

- FSM-based traffic light controller design
- Four-state finite state machine
- North-South and East-West traffic signal control
- Automatic GREEN, YELLOW, and RED signal switching
- Clock-based timing control
- 100 MHz FPGA clock support
- 10 seconds GREEN signal duration
- 3 seconds YELLOW signal duration
- Automatic state transition
- Reset functionality
- LED-based traffic signal indication
- Verilog testbench for functional verification
- Nexys A7 Artix-7 FPGA implementation

---

## 🛠️ Hardware Requirements

- Nexys A7 Artix-7 FPGA Development Board
- USB Programming Cable
- Computer or Laptop
- Xilinx Vivado Design Suite

---

## 💻 Software Requirements

- Xilinx Vivado Design Suite
- Verilog HDL
- Vivado Simulator

---

## 🔄 FSM State Sequence

The traffic light controller consists of four states:

| State | North-South | East-West |
|-------|-------------|-----------|
| S0 | GREEN | RED |
| S1 | YELLOW | RED |
| S2 | RED | GREEN |
| S3 | RED | YELLOW |

After completing State S3, the controller automatically returns to State S0.

---

## ⚙️ Working Principle

1. Initially, the North-South direction receives a GREEN signal.
2. After 10 seconds, the signal changes to YELLOW.
3. After 3 seconds, North-South changes to RED and East-West changes to GREEN.
4. After 10 seconds, East-West changes to YELLOW.
5. After 3 seconds, East-West changes to RED and North-South changes to GREEN.
6. The process continues automatically.

---

## 📂 Project Structure

```text
Artix7-Traffic-Light/
│
├── src/
│   └── traffic_light.v
│
├── testbench/
│   └── traffic_light_tb.v
│
├── constraints/
│   └── traffic_light.xdc
│
└── README.md
```

---

## 🧪 Simulation and Verification

The Verilog testbench is used to verify the complete traffic light sequence.

The testbench checks:

- North-South GREEN and East-West RED
- North-South YELLOW and East-West RED
- North-South RED and East-West GREEN
- North-South RED and East-West YELLOW
- Automatic repetition of the sequence

Expected simulation result:

**ALL TEST CASES PASSED!**

---

## 🔌 FPGA Implementation

The project is implemented on the Artix-7 FPGA using Xilinx Vivado.

Implementation steps:

1. Create a new RTL project in Vivado.
2. Select the Nexys A7 Artix-7 FPGA.
3. Add the Verilog source file.
4. Add the testbench file.
5. Add the XDC constraints file.
6. Run Behavioral Simulation.
7. Perform Synthesis and Implementation.
8. Generate the Bitstream.
9. Program the FPGA board.

---

## 🎯 Expected Output

The six LEDs represent the traffic signals for two directions.

The LEDs automatically change according to the FSM sequence:

- GREEN: Vehicles can move.
- YELLOW: Prepare to stop.
- RED: Vehicles must stop.

The traffic signal sequence repeats continuously.

---

## 🚀 Applications

- Smart Traffic Management Systems
- Automated Road Junction Control
- FPGA-Based Embedded Systems
- Digital System Design
- VLSI and FSM Applications

---

## 👩‍💻 Developed Using

**Language:** Verilog HDL

**FPGA:** Artix-7 (Nexys A7)

**Design:** Finite State Machine (FSM)

**Tool:** Xilinx Vivado

---

## 📌 Conclusion

The Artix-7 Traffic Light Controller successfully demonstrates the implementation of a Finite State Machine using Verilog HDL.

The design provides automatic traffic signal switching with clock-based timing control and can be implemented on an FPGA development board.
