# PennSilicon

PennSilicon is a two-person student hardware project focused on building a small, practical AI inference accelerator and taking it through the full design flow from a software reference model to RTL, verification, and eventually physical implementation.

The initial target is a compact integer matrix-multiply / systolic-array accelerator rather than a full production NPU. The design will be kept intentionally scoped so that the architecture, RTL, verification, and back-end work can all be understood and owned by the team.

## Project structure

```text
pennsilicon/
├── model/       # Python golden/reference models
├── rtl/         # SystemVerilog RTL
├── verif/       # cocotb/SystemVerilog verification
├── docs/        # Architecture and verification documentation
├── scripts/     # Utility and automation scripts
└── physical/    # Physical-design and tapeout-related work
```

## Initial technical direction

- Integer inference datapath
- Systolic-array / matrix-multiply core
- Wide accumulation
- Requantization, saturation, and activation support
- Python golden model for bit-exact reference
- SystemVerilog RTL
- cocotb-based verification
- Physical implementation after front-end freeze

Exact array dimensions, interfaces, memory organization, and tapeout target are intentionally left open until the architecture is finalized.

## Workflow

Development should happen on feature branches and merge into `main` through pull requests. Keep `main` in a working state and add tests alongside new RTL whenever practical.
