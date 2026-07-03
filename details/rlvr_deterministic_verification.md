# Deterministic Verifiable Rewards (RLVR)

Deterministic Verifiable Rewards (RLVR) use hard program execution and compiler checks rather than soft neural feedback.

## Overview
RLVR integrates sandboxed compilers and unit tests to verify logic correctness programmatically.

```mermaid
flowchart LR
    ModelOutput["Model Output"] --> Sandbox["Sandboxed Environment"]
    Sandbox --> Compiler["Lean 4 / Python Compiler"]
    Compiler --> TestSuite["Unit Tests / Proof Checkers"]
    TestSuite --> Reward["Deterministic Reward (1.0 or 0.0)"]
```

## Key Characteristics
- **Zero Reward Hacking:** Outputs must pass compiler verification or exact equivalence test.
- **Strict Scalar Limits:** Provides binary or exact accuracy scores.
- **Reasoning Focus:** Ideal for Math, Coding, and Symbolic Logic.

[Back to README](../README.md)
