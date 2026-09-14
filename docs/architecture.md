# Architecture

This document will hold the architecture specification for PennSilicon.

## Goals

- Small, understandable AI inference accelerator
- Integer datapath suitable for quantized inference
- Regular matrix-multiply / systolic-array architecture
- Straightforward bit-exact verification against a software model
- Scope appropriate for a two-person student team
- Clean path from RTL to physical implementation

## Open decisions

- Array dimensions
- Operand precision
- Accumulator width
- Dataflow choice
- Weight-loading scheme
- Input/output protocol
- On-chip buffering strategy
- Requantization format and rounding policy
- Supported activation functions
- Clock target
- Process / shuttle target

These should be frozen before the RTL is considered complete.
