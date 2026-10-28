# Supplementary Materials

## State-Assisted Preprocessing-Aware Offline-Online Lattice-Based Threshold Signatures

**Authors:** Mengqi Feng, Runze Zhao, Fanqi Kong, Zhaoxuan Li, and Ziming Zhao.

This repository contains the extended security definitions, correctness and parameter analysis, and security proofs supporting the main paper. The materials are organized by section title and are provided as PDF documents and matching LaTeX sources.

## Documents

| Main-paper section | Supplement | PDF | LaTeX source |
| --- | --- | --- | --- |
| III. Security Definitions, particularly III-B | Full preprocessing-aware security experiment | [Security Definitions.pdf](Security%20Definitions/Security%20Definitions.pdf) | [Security Definitions.tex](Security%20Definitions/Security%20Definitions.tex) |
| VI. Correctness and Security Proofs | Correctness, parameter analysis, full security proofs, and supporting trapdoor and sampling analysis | [Correctness and Security Proofs.pdf](Correctness%20and%20Security%20Proofs/Correctness%20and%20Security%20Proofs.pdf) | [Correctness and Security Proofs.tex](Correctness%20and%20Security%20Proofs/Correctness%20and%20Security%20Proofs.tex) |

## Contents

### Security Definitions

The [Security Definitions](Security%20Definitions/) supplement expands the preprocessing-aware security model in Section III-B:

- The ideal public binding service and its authenticated, linearizable binding-read interface.
- The adversary, random oracles, token-generation and response queries, public binding reads, and identifier burning.
- Atomic state transitions, one-time token consumption, private-state erasure, and persistent context bindings.
- Terminal-state evaluation, context authorization, identifier completion, and the adaptive-message, one-time-token, and combined preprocessing-aware winning events.

### Correctness and Security Proofs

The [Correctness and Security Proofs](Correctness%20and%20Security%20Proofs/) supplement expands Section VI:

- **VI-A: Correctness.** Detailed norm and rounding bounds, honest reconstruction, and pointwise and uniform correctness for admissible active sets.
- **VI-B: Illustrative Parameter Profile for Tokenized TalonG.** Verification thresholds, width checks, extraction and encoding bounds, and the interpretation of heuristic attack-cost estimates.
- **VI-C: Security of the Abstract Framework.** State invariants and exclusion of incompatible-context acceptance under the ideal binding service.
- **VI-D: Security of the Tokenized Talon Instantiation.** Aggregate-equivalent views, partial honest responses, incomplete-context security, fixed-input extraction with scaled lifting, and the resulting state-assisted security bound.
- **Supporting analysis.** Screened trapdoor generation, conditional preimage sampling, and composition of generation and sampling errors across keys and tokens.

## Model and Scope

The security claims are conditional on the cryptographic, generation, and sampling assumptions stated in the paper and supplements. The model uses static corruption, classical random-oracle access, reliable erasure, and an ideal trusted binding service with persistent bindings and authenticated, linearizable, rollback-protected reads. A concrete service implementation requires its own realization argument.

The TT-128-R1 parameter profile supplies illustrative checks and heuristic estimates. Those estimates alone do not establish an end-to-end 128-bit security claim. The trapdoor algorithms support the reduction; the honest protocol algorithms do not invoke them.

## Reading Guide

1. Read Section III of the main paper together with **Security Definitions** for the full experiment and state semantics.
2. Read Sections VI-A and VI-B together with the correctness and parameter-analysis part of **Correctness and Security Proofs**.
3. Read Sections VI-C and VI-D together with the security-proof and sampling-analysis part of the same supplement.

The PDFs are intended for reading; the `.tex` files provide the corresponding sources. Section and equation references explicitly identified as belonging to the main paper refer to that paper, rather than to the local numbering of a supplement.

## Repository Layout

```text
.
├── README.md
├── Security Definitions/
│   ├── README.md
│   ├── Security Definitions.pdf
│   └── Security Definitions.tex
├── Correctness and Security Proofs/
│   ├── README.md
│   ├── Correctness and Security Proofs.pdf
│   └── Correctness and Security Proofs.tex
└── .github/
    └── workflows/
        └── latex.yml
```

The GitHub Actions workflow builds both supplementary documents and uploads the resulting PDFs as workflow artifacts.
