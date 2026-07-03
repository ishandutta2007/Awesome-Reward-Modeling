# Direct Preference Optimization (DPO)

Direct Preference Optimization (DPO) reparameterizes the RLHF objective, training the policy directly on preference data without an explicit reward model.

## Overview
DPO shows that the policy's log-ratio mathematically maps to the reward, allowing direct gradient updates.

```mermaid
flowchart LR
    PrefData["Preference Dataset (x, y_w, y_l)"] --> DPO_Loss["DPO Loss Optimization"]
    DPO_Loss --> PolicyWeights["Update Active Policy directly"]
    style DPO_Loss fill:#f9f,stroke:#333,stroke-width:2px
```

## Key Characteristics
- **No Reward Model VRAM:** Saves massive GPU memory.
- **Reference Model Anchor:** Uses a reference model ratio to constrain drift.

[Back to README](../README.md)
