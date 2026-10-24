# Supplementary Materials for Section VIII

## State-Assisted Preprocessing-Aware Offline-Online Lattice-Based Threshold Signatures

**Authors:** Mengqi Feng, Runze Zhao, Fanqi Kong, Xiaofei Yue, Zhaoxuan Li, Ziming Zhao, and Jianwei Yin.

This supplement provides the full security proofs and supporting trapdoor and sampling analysis for Section VIII of the main paper. It is available as a PDF document and a LaTeX source file.

## Documents

- **PDF:** [VIII.pdf](VIII.pdf)
- **LaTeX source:** [VIII.tex](VIII.tex)

## Security Proofs

The security proofs cover:

- The state invariant and exclusion of incompatible-context acceptance.
- Aggregate-equivalent views.
- The mask distribution and partial responses.
- Incomplete-context security.
- Fixed-input extraction with scaled lifting.
- The final state-assisted preprocessing-aware security theorem.

## Screened Trapdoor Generation and Conditional Sampling

The supporting analysis specifies:

- Screened trapdoor generation and its output distribution.
- Conditional preimage sampling for every target and the associated statistical-distance bounds.
- Error composition over multiple keys and tokens.
- The generation and screened-key assumptions, together with the Hint-RLWE and normalized ring-SIS assumptions used by the security argument.

The trapdoor algorithms serve the reduction; they are not invoked by the honest protocol algorithms.

## Security Model and Scope

The security analysis is conditional on the stated cryptographic and sampling assumptions. Its model uses **static corruption, classical random-oracle access, reliable erasure, and an ideal trusted binding service** with authenticated, linearizable, rollback-protected reads and persistent bindings. A concrete service implementation requires a separate realization argument.

## Reading Guide

Read this document alongside **Section VIII** of the main paper for the full security arguments and their supporting trapdoor and sampling conditions. Open the PDF for reading and the matching `.tex` file for the LaTeX source.

## File Layout

```text
.
├── README.md
├── VIII.pdf
└── VIII.tex
```
