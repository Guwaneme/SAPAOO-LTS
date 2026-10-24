# Supplementary Materials for Section IV-B

## State-Assisted Preprocessing-Aware Offline-Online Lattice-Based Threshold Signatures

**Authors:** Mengqi Feng, Runze Zhao, Fanqi Kong, Xiaofei Yue, Zhaoxuan Li, Ziming Zhao, and Jianwei Yin.

This supplement provides the full preprocessing-aware security experiment underlying the definitions in Section IV-B of the main paper. It is available as a PDF document and a LaTeX source file.

## Documents

- **PDF:** [IV-B.pdf](IV-B.pdf)
- **LaTeX source:** [IV-B.tex](IV-B.tex)

## Full Preprocessing-Aware Security Experiment

This document specifies:

- The ideal public binding service, persistent context bindings, and authenticated, linearizable binding reads.
- The adversary, token-generation, response, binding-read, and burn oracles.
- Identifier lifecycle rules, atomic response generation and token consumption, and private-state erasure.
- The terminal-state convention and definitions of context authorization and identifier completion.
- Adaptive-message security, one-time-token security, and their combined preprocessing-aware unforgeability notion.

## Security Model and Scope

The security analysis is conditional on the stated cryptographic and sampling assumptions. Its model uses **static corruption, classical random-oracle access, reliable erasure, and an ideal trusted binding service** with authenticated, linearizable, rollback-protected reads and persistent bindings. A concrete service implementation requires a separate realization argument.

## Reading Guide

Read this document alongside **Section IV-B** of the main paper for the complete experiment, oracle interfaces, and state semantics. Open the PDF for reading and the matching `.tex` file for the LaTeX source.

## File Layout

```text
.
├── README.md
├── IV-B.pdf
└── IV-B.tex
```
