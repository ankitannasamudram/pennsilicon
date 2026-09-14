# Verification

Verification infrastructure lives here.

Primary flow: cocotb drives the RTL and compares results against the Python golden model. Directed tests should cover individual blocks first, followed by randomized and end-to-end tests of the full accelerator.

Important areas to verify include signed arithmetic, wavefront/skew timing, accumulation width, overflow behavior, requantization boundaries, saturation, activation behavior, reset, and pipeline fill/drain timing.
