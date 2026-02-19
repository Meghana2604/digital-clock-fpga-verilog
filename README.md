# digital-clock-fpga-verilog
Digital Clock – Verilog/SystemVerilog RTL Design
Project Description

This project implements a fully functional Digital Clock (HH:MM:SS format) using Verilog/SystemVerilog. The design follows a modular RTL architecture and is fully synthesizable. The clock correctly handles second, minute, and hour rollovers in 24-hour format and is verified through simulation.

DESIGN FEATURES:

Modular RTL design

24-hour time format (00:00:00 – 23:59:59)

Proper rollover logic:

59 → 00 (seconds and minutes)

23 → 00 (hours)

Reset functionality

Synthesizable code

Clean non-blocking sequential logic

Simulation-verified behavior

DESIGN ARCHITECTURE:

The clock is divided into the following modules:

Clock Divider – Generates 1 Hz clock from input clock

Seconds Counter – Counts from 0 to 59

Minutes Counter – Counts from 0 to 59

Hours Counter – Counts from 0 to 23

Reset Logic – Initializes clock to 00:00:00

All counters are implemented using synchronous sequential logic.

PROJECT STRUCTURE:
digital-clock-fpga-verilog/
│── rtl
│   └── digital_clock.sv
│
│── sim
│   └──  waveform.png
│
│── tb
│   └── digital_clock_tb.sv
│
│── README.md

Simulation Details

Language: Verilog / SystemVerilog
Simulator: Icarus Verilog / EDA Playground
Waveform Viewer: GTKWave
Dump file format: VCD

The testbench verifies:

Second rollover (59 → 00)

Minute rollover (59 → 00)

Hour rollover (23 → 00)

Reset behavior

Waveform Output

How to Run the Project
Using Icarus Verilog (Command Line)
iverilog -g2012 rtl/digital_clock.sv tb/digital_clock_tb.sv
vvp a.out
gtkwave dump.vcd

Using EDA Playground

Paste RTL code in the Design section

Paste Testbench in the Testbench section

Enable waveform dump

Run simulation

Key Highlights

Fully synthesizable RTL

Clean modular hierarchy

Industry-style coding practices

Simulation-based verification

Organized GitHub project structure

Future Enhancements

12-hour format with AM/PM

Alarm feature

Seven-segment display interface

FPGA board implementation

Parameterized clock frequency

Author
Meghana Bollu
Aspiring RTL Design and Verification Engineer


