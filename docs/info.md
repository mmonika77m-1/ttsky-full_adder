## How it works

This project implements an Arithmetic Logic Unit (ALU) that performs a set of basic arithmetic and logical operations on binary inputs. The ALU takes two input operands and a control signal that selects the desired operation.

Supported operations typically include:

* Addition
* Subtraction
* Bitwise AND
* Bitwise OR
* Bitwise XOR
* NOT (optional)
* Shift operations (optional)

The control signal determines which operation is executed. Based on this selection, the ALU processes the inputs and produces the corresponding output along with status flags such as zero, carry, or overflow (if implemented).

The design is synthesized using a standard RTL-to-GDS flow and is intended to be integrated into a larger digital system such as a processor datapath.

## How to test

1. Provide two input operands (`A` and `B`) to the ALU.
2. Set the control signal (`opcode` or `sel`) to select the desired operation.
3. Apply a clock signal if the design is sequential (or directly observe outputs if combinational).
4. Observe the output result (`Y`) and any status flags.

Example test cases:

* Set inputs A = 5, B = 3, operation = ADD → Output = 8
* Set inputs A = 5, B = 3, operation = SUB → Output = 2
* Set inputs A = 5, B = 3, operation = AND → Output = 1

Simulation can be performed using a Verilog testbench, and waveform viewers can be used to verify correctness.

## External hardware

This project does not require any external hardware.

(Optional, if extended to FPGA or demo setup:)

* LEDs to display output
* Switches or buttons for input selection
* FPGA development board for implementation
