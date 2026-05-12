# Advanced Stack Storage System — DLD Project 8

A modified stack data structure implemented in LogicWorks based on the 
Last In First Out (LIFO) principle with automatic overflow handling.

## Features
- 4-element stack capacity storing 4-bit values (0–15)
- Push: stores new value, automatically discards oldest when full
- Pop: returns values in LIFO order (newest first)
- Full and Empty indicators
- Circular buffer design using HEAD counter and register file

## How It Works
When the stack is full and a new value is pushed, the oldest element 
is discarded automatically. For example, pushing 2, 4, 6, 8 fills 
the stack. Pushing 10 discards 2, leaving 4, 6, 8, 10. Popping 
returns 10, 8, 6, 4.

## Components Used
- 16 D flip-flops (4-bit register file)
- 4-bit up/down counters (HEAD and size tracking)
- 2x4 decoder and quad 2x1 multiplexers (write enable logic)
- 4-to-1 multiplexers and 4-bit adder (pop output logic)
- Combinational logic gates (full/empty detection, wraparound)

## Files
- `project.cct` — LogicWorks circuit file
- `DLD_Project_Report.pdf` — Written report

## Tools
LogicWorks 5
