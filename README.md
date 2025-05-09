# RISC-V-Processor-Language-used-Verilog-
Implemented a RISC-V processor supporting the RV32I base integer instruction set with a pipelined architecture and hazard handling. Designed a single-port memory system for both data and instructions, optimizing performance with a 2-cycle instruction issuing method to achieve an effective CPI of 2.

==============================================
Project: femtoRV32 - RISC-V FPGA Implementation
Course: CSCE 3301 - Computer Architecture
Fall 2024
Milestone: 3
==============================================

Student Names:
- Saif Abd Elfattah
- Adham Ali

==============================================
Release Notes
==============================================

1. Overview:
   This project implements the femtoRV32, a simplified RISC-V processor for FPGA testing using the Nexys A7 platform. The processor supports the RV32I base integer instruction set and incorporates pipelining with hazard management.

2. Issues: (All Solved)
   - Timing issues observed during certain memory operations on the FPGA.
   - Minor differences in simulation results for specific branch instructions (e.g., ECALL, EBREAK).

3. Assumptions:
   - The processor assumes a byte-addressable memory with word alignment.
   - Branch instructions are executed with simple branch prediction (no dynamic prediction implemented).
   - Custom instructions like ECALL and EBREAK are treated as halting or no-op commands.
   - Single-port memory is used, causing potential delays due to structural hazards.

4. What Works:
   - Full implementation of the RV32I base integer instruction set (42 user-level instructions).
   - Pipelining with proper hazard detection and forwarding mechanisms.
   - Successful simulation and verification of arithmetic, logical, branch, and memory instructions.
   - Test program generator implemented in C++ generates random but valid RISC-V instruction sequences for testing.
   - FPGA testing on Nexys A7 verifies basic functionality and performance of the processor design.

5. References:
   - RISC-V Specifications (https://riscv.org/technical/specifications/)
   - Nexys A7 FPGA Documentation
