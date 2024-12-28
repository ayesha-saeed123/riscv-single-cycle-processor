# Guidelines
This repository will contain all the code for the design and implementation of a RISC-V processor with Control and Status Register (CSR) functionality. The project includes single-cycle processor implementation along wih 5-stage pipelined architecture to improve performance.

## 1. Tools Used
### 1.1 Venus Simulator:

Converts RISC-V assembly into hexadecimal format and generates .hex files for program memory initialization.It is simple and efficient tool for writing and testing RISC-V assembly.
### 1.2 VS Code:

Main IDE for writing, editing, and debugging SystemVerilog files, with extensions installed for Verilog/SystemVerilog syntax highlighting.
### 1.3 ModelSim:

Used for compilation, simulation, and generating .vcd files.
### 1.4 GTKWave:

Opens .vcd files for waveform visualization, also used to verify signal behavior and pipeline operations.
##  2. Compilation

RTL can be compiled with the command: vlog names_of_all_system_verilog_files

or simply:
```bash
  vlog *.sv
```
Compilation creates a work folder in your current working directory in which all the files generated after compilation are stored.

## 3. Simulation

The compiled RTL can be simulated with command:
```bash
  vsim -c name_of_toplevel_module -do "run -all"
```
Simulation creates a .vcd file. This files contains all the simulation behaviour of design.

## 4. Viewing the VCD Waveform File

To view the waveform of the design run the command:

```bash
 gtkwave dumfile_name.vcd 
```
This opens a waveform window. Pull the required signals in the waveform and verify the behaviour of the design.
