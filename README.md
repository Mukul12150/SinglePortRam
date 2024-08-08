
Single Port RAM Project in Verilog
Overview
This project implements a single-port RAM module using Verilog. Single-port RAM allows both read and write operations through a single data port. This design is useful for various digital systems where a simple and efficient memory module is needed.

Features
Single port for read and write operations
Configurable memory depth and data width
Synchronous read and write operations
Simple and efficient design
Directory Structure
css
Copy code
single_port_ram/
├── src/
│   ├── single_port_ram.v
│   └── tb_single_port_ram.v
├── docs/
│   └── README.md
└── Makefile
Files
src/single_port_ram.v
This file contains the Verilog code for the single-port RAM module. The module includes:

Parameters:
DATA_WIDTH : Width of the data bus (default: 8 bits)
ADDR_WIDTH : Width of the address bus (default: 4 bits)
Ports:
clk : Clock input
we : Write enable signal
addr : Address input
din : Data input (for write operations)
dout : Data output (for read operations)
src/tb_single_port_ram.v
This is the testbench file used to simulate and verify the functionality of the single-port RAM module. It includes various test cases to ensure the RAM operates correctly under different scenarios.

Usage
Prerequisites
Verilog simulation tool (e.g., ModelSim, VCS, Icarus Verilog)
Simulation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/single_port_ram.git
cd single_port_ram
Compile the Verilog source and testbench files:

bash
Copy code
iverilog -o single_port_ram.out src/single_port_ram.v src/tb_single_port_ram.v
Run the simulation:

bash
Copy code
vvp single_port_ram.out
View the waveform (optional):

bash
Copy code
gtkwave single_port_ram.vcd
Makefile
A Makefile is provided to simplify the build and simulation process. Use the following commands:

make : Compile the Verilog source and testbench files
make run : Run the simulation
make view : View the waveform using GTKWave