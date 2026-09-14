# Verification Plan

The verification strategy is intentionally lightweight but rigorous enough to support eventual ASIC implementation.

## Levels

1. Processing-element tests
2. Array data-movement and skew tests
3. Accumulation and signed-arithmetic tests
4. Requantization / saturation / activation tests
5. Full-array directed tests
6. Randomized bit-exact comparison against the Python golden model
7. Reset and pipeline fill/drain tests

## Sign-off intent

Before front-end freeze, the RTL should pass deterministic regression tests across normal cases, signed corner cases, saturation boundaries, timing-sensitive wavefront cases, and randomized matrices. Any architectural assumptions used by the testbench should be documented alongside the design.
