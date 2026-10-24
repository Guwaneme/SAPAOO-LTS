# Supplementary Materials

## State-Assisted Preprocessing-Aware Offline-Online Lattice-Based Threshold Signatures

**Authors:** Mengqi Feng, Runze Zhao, Fanqi Kong, Xiaofei Yue, Zhaoxuan Li, Ziming Zhao, and Jianwei Yin.

This repository provides the supplementary security definitions, correctness and parameter analysis, and full security proofs for the manuscript. The documents expand the corresponding sections of the main paper and are available as both PDF documents and LaTeX sources.

## Documents

File names follow the section numbering of the main paper.

| Main-paper section | Supplementary document | PDF | LaTeX source |
| --- | --- | --- | --- |
| IV-B | Full Preprocessing-Aware Security Experiment | [IV-B.pdf](IV-B.pdf) | [IV-B.tex](IV-B.tex) |
| VII | Correctness and Parameter Analysis | [VII.pdf](VII.pdf) | [VII.tex](VII.tex) |
| VIII | Security Proofs, including Screened Trapdoor Generation and Conditional Sampling | [VIII.pdf](VIII.pdf) | [VIII.tex](VIII.tex) |

## Contents

### Section IV-B: Full Preprocessing-Aware Security Experiment

This document specifies the complete experiment underlying the security definitions in the main paper:

- The ideal public binding service, persistent context bindings, and authenticated, linearizable binding reads.
- The adversary, token-generation, response, binding-read, and burn oracles.
- Identifier lifecycle rules, atomic response generation and token consumption, and private-state erasure.
- The terminal-state convention and definitions of context authorization and identifier completion.
- Adaptive-message security, one-time-token security, and their combined preprocessing-aware unforgeability notion.

### Section VII: Correctness and Parameter Analysis

This document supplies the detailed correctness derivations and parameter checks:

- Subgaussian norm bounds for independent sums, pairwise-mask cancellation, and Shamir reconstruction.
- Rounding-error analysis, verification thresholds, and reconstruction of the honest aggregate and challenge.
- Pointwise correctness for a fixed active set and uniform correctness for active-set selection after observing public tokens.
- Composition of implemented sampling errors over the relevant joint sampling distribution.
- The illustrative TT-128-R1 parameter profile, extraction bounds, width checks, encoding budgets, and heuristic attack-cost estimates.
- The scope of those estimates and the remaining proof and implementation obligations.

### Section VIII: Security Proofs and Supporting Sampling Analysis

This document combines the material previously presented in Appendices C and D.

**Security proofs** cover the state invariant, exclusion of incompatible-context acceptance, aggregate-equivalent views, the mask distribution and partial responses, incomplete-context security, fixed-input extraction with scaled lifting, and the final state-assisted preprocessing-aware security theorem.

**Trapdoor and sampling analysis** specifies screened trapdoor generation and its output distribution, conditional preimage sampling for every target, statistical-distance bounds, and error composition over multiple keys and tokens. It also states the generation and screened-key assumptions, together with the Hint-RLWE and normalized ring-SIS assumptions used by the security argument. The trapdoor algorithms serve the reduction; they are not invoked by the honest protocol algorithms.

## Security Model and Scope

The security analysis is conditional on the stated cryptographic and sampling assumptions. Its model uses **static corruption, classical random-oracle access, reliable erasure, and an ideal trusted binding service** with authenticated, linearizable, rollback-protected reads and persistent bindings. A concrete service implementation requires a separate realization argument.

## Reading Guide

Read these documents alongside the corresponding sections of the main paper:

1. **IV-B** for the full experiment, oracle interfaces, and state semantics.
2. **VII** for correctness bounds and the interpretation of candidate parameters.
3. **VIII** for the full security arguments and their supporting trapdoor and sampling conditions.

Open the PDF files for reading and the matching `.tex` files for the LaTeX sources. The [`.github/workflows`](.github/workflows/) directory contains the repository's PDF build workflow configuration.

## Repository Layout

```text
.
├── README.md
├── IV-B
    └── IV-B.pdf
    └── IV-B.tex
├── VII
    └── VII.pdf
    └── VII.tex
├── VIII
    └── VIII.pdf
    └── VIII.tex
└── .github/
    └── workflows/
```
