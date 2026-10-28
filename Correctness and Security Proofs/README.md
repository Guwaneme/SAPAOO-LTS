# Correctness and Security Proofs

Supplementary material for **Section VI: Correctness and Security Proofs** of *State-Assisted Preprocessing-Aware Offline-Online Lattice-Based Threshold Signatures*.

## Documents

- [Correctness and Security Proofs.pdf](Correctness%20and%20Security%20Proofs.pdf)
- [Correctness and Security Proofs.tex](Correctness%20and%20Security%20Proofs.tex)

The document brings the correctness and parameter analysis together with the security proofs and their supporting generation and sampling analysis.

## Correspondence with the Main Paper

| Main-paper subsection | Supplementary material |
| --- | --- |
| VI-A. Correctness | Subgaussian norm bounds, mask cancellation, Shamir reconstruction, rounding error, honest verification, and pointwise and uniform correctness. |
| VI-B. Illustrative Parameter Profile for Tokenized TalonG | Verification thresholds, width checks, extraction bounds, encoding budgets, heuristic attack-cost estimates, and their scope. |
| VI-C. Security of the Abstract Framework | State invariants and exclusion of incompatible-context acceptance under persistent ideal bindings. |
| VI-D. Security of the Tokenized Talon Instantiation | Aggregate-equivalent views, mask distributions and partial responses, incomplete-context security, scaled-lifting extraction, and the final state-assisted security bound. |

## Security Proofs

The proof part develops:

- Preservation of the state invariant and context bindings across successful responses, erasure, and burning.
- Exclusion of accepting signatures whose context conflicts with an established binding.
- Aggregate-equivalent views and the joint distribution of partial honest responses.
- The reduction for identifiers without a completed signing context, including target selection, nondistinguished-token simulation, Hint-RLWE replacement, forking, and ring-SIS extraction.
- Fixed-input extraction with scaled lifting and the reduction from preprocessing-aware security to incomplete-context security.

## Trapdoor Generation and Sampling

The supporting analysis specifies screened trapdoor generation, its output law, conditional preimage sampling for every target, and the associated statistical-distance bounds. It composes key-replacement, token-opening, capped-generation, and implementation errors across the relevant keys and tokens.

The generation and screened-key properties are explicit assumptions. The trapdoor algorithms are used by the security reduction; honest signers do not receive or use these trapdoors.

## Scope

Correctness uses the sampling and service-availability conditions stated in the paper. The security bounds additionally depend on the stated PRF, Hint-RLWE, normalized ring-SIS, generation, and sampling assumptions, together with static corruption, classical random-oracle access, reliable erasure, and the ideal binding-service contract defined in the [Security Definitions](../Security%20Definitions/) supplement.

The TT-128-R1 estimates are illustrative and do not by themselves establish an end-to-end 128-bit security claim. Encoding budgets in the parameter analysis describe representations rather than measured protocol bandwidth or runtime.

## Reading Guide

Read the correctness and parameter analysis with Sections VI-A and VI-B, followed by the security proofs with Sections VI-C and VI-D. References explicitly marked as main-paper sections, equations, lemmas, or theorems use the numbering of the main paper. Equations in this supplement use an `S` prefix.

## File Layout

```text
Correctness and Security Proofs/
├── README.md
├── Correctness and Security Proofs.pdf
└── Correctness and Security Proofs.tex
```

[Repository overview](../README.md)
