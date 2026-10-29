# JP-32
starting out somekind of cpu 
# JP-32 — Experimental 32-bit CPU Architecture

JP-32 is an experimental computer architecture project focused on designing an original 32-bit instruction set architecture (ISA), implementing it in software, and eventually realizing it as a hardware processor.

The goal is to explore computer architecture from first principles: instruction encoding, register organization, datapath design, control logic, memory systems, and execution models.

This project is developed as an independent engineering and learning project.

## Project Goals

- Design an original 32-bit instruction set architecture.
- Define precise instruction semantics and binary encodings.
- Build a Python reference emulator.
- Develop an assembler for the JP-32 instruction set.
- Implement the processor in Verilog or VHDL.
- Verify the hardware implementation against the reference emulator.
- Experiment with alternative execution mechanisms and evaluate their trade-offs.

## Architectural Overview

The initial design proposes:

| Property                  | Initial specification |
| ------------------------- | --------------------- |
| Architecture              | Custom 32-bit ISA     |
| Instruction width         | 32 bits, fixed-width  |
| General-purpose registers | 16 × 32-bit           |
| Predicate registers       | 4 × 1-bit             |
| Memory addressing         | Byte-addressable      |
| Byte order                | Little-endian         |
| Execution model           | In-order, unpipelined |
| Reference implementation  | Python emulator       |
| Hardware implementation   | Verilog or VHDL       |

These specifications are provisional and may change during development. The authoritative design will be maintained in the architecture documentation.

## Experimental Direction

JP-32 will investigate predicate-driven execution as an alternative way to express conditional operations.

The architecture is intended to support comparisons that explicitly update predicate registers and instructions that execute conditionally based on those predicates.

The purpose is to study instruction dependencies, control flow, implementation complexity, and potential performance trade-offs rather than assume that this approach is inherently superior.

## Development Roadmap

- [ ] Finalize the architecture specification.
- [ ] Define the opcode map and instruction encodings.
- [ ] Implement a minimal Python emulator.
- [ ] Implement the complete initial ISA.
- [ ] Develop an assembler.
- [ ] Build automated instruction and program tests.
- [ ] Implement the processor in HDL.
- [ ] Compare hardware simulation against the reference emulator.
- [ ] Evaluate architectural alternatives.
- [ ] Optionally deploy the processor on an FPGA.

## Repository Structure

```text
JP-32/
├── README.md
├── LICENSE
├── .gitignore
├── docs/
│   ├── architecture.md
│   ├── isa-v0.1.md
│   └── instruction-encoding.md
├── emulator/
├── assembler/
├── rtl/
├── tests/
└── programs/
```

Directories and files will be added as the project develops.

## Development Principles

- Document architectural decisions explicitly.
- Keep instruction semantics independent of implementation details.
- Test edge cases, not only ordinary operations.
- Use the Python emulator as the reference model for hardware verification.
- Record incompatible ISA changes with explicit versioning.
- Measure performance and complexity instead of assuming improvements.

## Project Status

**Status:** Early design phase.

The architecture is under development. Instruction encodings, execution semantics, and implementation details are subject to revision.

## License

The project's license will be specified in the `LICENSE` file.

## Contributions

Feedback, architectural discussions, bug reports, and suggestions are welcome. The design is experimental, and proposed changes should include a clear explanation of their technical motivation and trade-offs.
