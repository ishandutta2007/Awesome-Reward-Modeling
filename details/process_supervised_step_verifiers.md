# Process-Supervised Step Verifiers

Process-Supervised Step Verifiers grade each logical step in multi-turn or multi-step reasoning tasks.

## Overview
Unlike standard reward models that score the end state, step verifiers inspect token boundaries indicating progress.

```mermaid
flowchart LR
    StepToken["Step Segment (tags)"] --> Verifier["Step Verifier"]
    Verifier --> Probability["Confidence/Correctness Score"]
    Probability --> RL_Signal["Step-Level Policy Optimization"]
```

## Key Characteristics
- **Token boundaries:** Segmented by newlines or logic tags.
- **Granular optimization:** Pinpoints exact points of logical failure.

[Back to README](../README.md)
