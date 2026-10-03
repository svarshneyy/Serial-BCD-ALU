# Serial BCD ALU (Verilog)

A Verilog arithmetic logic unit that adds and subtracts 4-digit BCD (binary-coded decimal) numbers over a serial interface. Built for ECE 310 at NC State University (Spring 2025).

## What it does

- Receives each operation as a serial packet, one bit per clock, and sends the result back the same way.
- Adds or subtracts two 4-digit BCD numbers and produces a 5-digit BCD result.
- Recognizes valid packets by their header and ignores malformed ones.
- Handles back-to-back packets with no idle clock cycles between them.

## Verification

Tested in simulation with four test vectors:

1. An addition followed immediately by a subtraction.
2. Operands containing bit patterns that look like a packet header.
3. A packet with an invalid header, which must produce no output.
4. Edge cases: 0000 + 0000 and 9999 + 9999.

Results were checked against the expected values in the simulation waveforms.

## Tools

Verilog and Vivado (simulation and synthesis).

## Author

Sanchit Varshney
