# Supplementary Materials for Section VII

## State-Assisted Preprocessing-Aware Offline-Online Lattice-Based Threshold Signatures

**Authors:** Mengqi Feng, Runze Zhao, Fanqi Kong, Xiaofei Yue, Zhaoxuan Li, Ziming Zhao, and Jianwei Yin.

This supplement provides the detailed correctness derivations and parameter analysis supporting Section VII of the main paper. It is available as a PDF document and a LaTeX source file.

## Documents

- **PDF:** [VII.pdf](VII.pdf)
- **LaTeX source:** [VII.tex](VII.tex)

## Correctness and Parameter Analysis

This document supplies:

- Subgaussian norm bounds for independent sums, pairwise-mask cancellation, and Shamir reconstruction.
- Rounding-error analysis, verification thresholds, and reconstruction of the honest aggregate and challenge.
- Pointwise correctness for a fixed active set and uniform correctness for active-set selection after observing public tokens.
- Composition of implemented sampling errors over the relevant joint sampling distribution.
- The illustrative TT-128-R1 parameter profile, extraction bounds, width checks, encoding budgets, and heuristic attack-cost estimates.
- The scope of those estimates and the remaining proof and implementation obligations.

## Scope

The correctness guarantees use the sampling and service-availability conditions stated in the document. The parameter analysis distinguishes heuristic attack-cost estimates from the mathematical and implementation obligations required by the security argument.

## Reading Guide

Read this document alongside **Section VII** of the main paper for correctness bounds and the interpretation of candidate parameters. Open the PDF for reading and the matching `.tex` file for the LaTeX source.

## File Layout

```text
.
├── README.md
├── VII.pdf
└── VII.tex
```
