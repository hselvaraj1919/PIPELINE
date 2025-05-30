#PIPELINE-PROCESSOR-DESIGN

*COMPANY*: CODETECH IT SOLUTIONS

*NAME*: H.SELVARAJ

*INTERN ID*:CTO4DL1346

*DOMAIN*: VLSI

*DURATION*:4 weeks

*MENTOR*:NEELA SANTOSH

##DETAILED DESCRIPTION
Introduction
A pipelined processor is a type of CPU design that improves instruction throughput by overlapping the execution of multiple instructions. Pipelining divides the instruction execution process into stages, each handled by a separate hardware unit. This allows a new instruction to start executing in every clock cycle.

A 4-stage pipeline breaks the instruction cycle into four main stages:
Instruction Fetch (IF)
Instruction Decode (ID)
Execute (EX)
Write Back (WB)
This pipelined architecture helps achieve higher performance by increasing instruction throughput compared to a single-cycle or multi-cycle processor.
Pipeline Stages in Detail
1. Instruction Fetch (IF)
The program counter (PC) fetches the instruction from instruction memory.
It is then passed to the next stage along with the incremented PC (PC + 1).
Components: Program Counter, Instruction Memory.
2. Instruction Decode (ID)
The fetched instruction is decoded to determine the operation type.
Source operands are read from the register file.
Control signals are generated to guide execution.
Components: Instruction Decoder, Register File, Control Unit.
3. Execute (EX)
Performs arithmetic or logic operations using the ALU.
Computes memory addresses for load/store instructions.
For branches, evaluates conditions.
Components: ALU, Forwarding Unit (optional), Branch Unit.
4. Write Back (WB)
The result from the ALU or memory is written back to the register file.
Final step in the instruction life cycle.
Components: Write Logic, Register File Interface.
Pipeline Registers
Between each stage, pipeline registers are required to hold intermediate values (such as operands, instruction fields, and control signals). These registers isolate stages and allow simultaneous execution of different instructions.
IF/ID register: Holds instruction and PC.
ID/EX register: Holds decoded operands and control signals.
EX/WB register: Holds result to be written back.
