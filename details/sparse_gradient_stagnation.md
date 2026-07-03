# Sparse Gradient Stagnation Wall

Sparse gradients occur in hard-verifier environments when the model fails nearly all tests early on, preventing optimization.

## Overview
A warm-start curriculum schedule or initial supervised fine-tuning (SFT) establishes a baseline pass rate before launching full RL.

```mermaid
flowchart TD
    ColdStart["RL directly on hard tests"] --> ZeroGrad["0% Success = Sparse Gradients"]
    ZeroGrad --> Stall["Training Stalls"]
    WarmStart["SFT / Curriculum Learning"] --> InitialSuccess["Establish Baseline Pass Rate"]
    InitialSuccess --> SmoothRL["Stable RL Loop"]
```

## Key Characteristics
- **Curriculum Schedule:** Gradually increases test difficulty.
- **SFT Bootstrapping:** Ensures initial policy hits valid outputs.

[Back to README](../README.md)
