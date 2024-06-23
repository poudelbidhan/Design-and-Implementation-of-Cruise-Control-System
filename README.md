# Design-and-Implementation-of-Cruise-Control-System 

In this project, we familiarize ourselves with the basics of synthesis using design Vision through a simple example "cruise control design". After synthesis, we will do a pre-layout static timing analysis of our synthesized design. We will define constraints for our design and check the timing of all the paths in the design. In the final part, we will use the synthesized Verilog netlist to perform "Place and Route" the circuit on a die.


## Part 1: Logic Synthesis using Synopsys Design Vision
Here we synthesize the logic with a certain specific library for 180nm technology. The Synopsys database format (db) file for a typical 180nm technology is given to us. 

1. Load a design:
   
    • The analyze command reads a VHDL or Verilog file, checks for proper syntax and synthesizable logic, and stores the design in an intermediate format.
2. Elaborate:
   
    • The elaborate command creates a design from the intermediate format produced by analyze. It replaces the HDL operators with synthetic operators. Mainly it translates the Verilog code to Synopsys internal generic library called gtech.
   
3. Read
   
    • The read command is used to load files in formats other than HDL formats, such as db, pla, and other formats supported by Design Compiler.



## Part 2: Static Timing Analysis with Synopsys PrimeTime

•  Timing analysis is to check the timing requirement of the circuit. You can do timing analysis at different design stages - pre-layout with wire-load models or post-layout with actual wires.

• PrimeTime® (PT) is the static timing analysis (STA) tool from Synopsys. It is the most widely used STA engine.

• Though the Design compiler has its own timing engine, it cannot come close to Primetime's accuracy. Moreover, primetime can also consider signal integrity effects like coupling noise due to cross-talk and analysis of complex interconnect structures.  

## Part 3 : Automatic Place and Route with Cadence Innovus


