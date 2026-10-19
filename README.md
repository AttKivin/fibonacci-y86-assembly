# Fibonacci Checker, Y86-64 Assembly

A university assembly programming project for the Computer Systems course at the University of Oulu (Autumn 2024).

## Overview

The program checks numbers in a zero-terminated sequence stored at memory address `0x700`. It uses the mathematical property that a positive integer n is a Fibonacci number if either `5n² + 4` or `5n² − 4` is a perfect square.

The intended output is the first non-Fibonacci number in `%rax`, or `0` if all numbers pass. Each number is checked independently; the sequence does not need to follow Fibonacci order.

## Implementation

- Y86-64 assembly with inputs up to 1000.
- Custom multiplication using bit masks and repeated doubling.
- Integer square root calculation using a bitwise algorithm.
- Software right shifts implemented using basic Y86-64 instructions.
- Finnish code comments and an implementation reflection.

## Running

Use a compatible Y86-64 assembler and simulator. For local testing, initialize a zero-terminated sequence at `0x700` before entering `main`. The program initializes its own stack.

## Credits

The software right-shift routines were adapted from an approach shared by Peter Cordes on Stack Overflow, as credited in the source comments.
