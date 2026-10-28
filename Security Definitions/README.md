# Security Definitions

Supplementary material for **Section III: Security Definitions**, particularly **Section III-B: Preprocessing-Aware Security Model**, of *State-Assisted Preprocessing-Aware Offline-Online Lattice-Based Threshold Signatures*.

## Documents

- [Security Definitions.pdf](Security%20Definitions.pdf)
- [Security Definitions.tex](Security%20Definitions.tex)

## Contents

The supplement specifies the full preprocessing-aware security experiment:

- **Ideal public binding service.** Persistent context bindings, the public binding-read interface, and the consistency and authentication requirements used by state-assisted verification.
- **Adversary, oracles, and shared state.** Static corruption, independent label and challenge random oracles, token-generation and response queries, public binding reads, and identifier burning.
- **State-transition and failure rules.** Atomic response generation and token consumption, one-time private-state use, erasure, and the behavior of rejected or failed queries.
- **Authorization and completion.** The terminal-state convention, recorded honest responses, authorized contexts, and completed identifiers.
- **Security notions.** Adaptive-message forgery, incompatible reuse of a one-time identifier, and their combined preprocessing-aware unforgeability experiment.

## Model and Scope

The experiment assumes static corruption, classical random-oracle access, reliable erasure, and an ideal trusted binding service with authenticated, linearizable, rollback-protected reads. Adaptive corruption, exposure of honest private state, and service corruption are outside this model.

A binding remains persistent after private-state erasure or identifier burning. Incompatible-context acceptance is excluded by the ideal binding check. Security for unbound identifiers and incomplete response collections still requires the cryptographic argument given in the [Correctness and Security Proofs](../Correctness%20and%20Security%20Proofs/) supplement.

## Reading Guide

Read this document alongside Section III of the main paper. It expands the experiment summarized in Section III-B; it does not define a separate protocol or a different service model.

## File Layout

```text
Security Definitions/
├── README.md
├── Security Definitions.pdf
└── Security Definitions.tex
```

[Repository overview](../README.md)
