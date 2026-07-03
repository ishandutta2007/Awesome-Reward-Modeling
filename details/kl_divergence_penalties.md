# Implicit KL Divergence Penalties

KL divergence penalties constrain policy updates to prevent the language model from diverging too far from a baseline.

## Overview
By penalizing the Kullback-Leibler divergence between the active policy and a frozen reference model, we prevent reward hacking.

```mermaid
flowchart TD
    Policy["Active Policy Token Logits"] --> KL_Calc["Calculate KL Divergence"]
    Reference["Frozen Reference Model Logits"] --> KL_Calc
    KL_Calc --> Penalty["Subtract penalty from Reward"]
```

## Key Characteristics
- **Policy Anchoring:** Keeps behavioral distribution stable.
- **Reduces Degeneracy:** Prevents the model from outputting repetitive gibberish that tricks the RM.

[Back to README](../README.md)
