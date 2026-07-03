# Group-Wise Length Normalization

Group-Wise Length Normalization combats verbosity bias by penalizing overly long candidate generations relative to their group.

## Overview
Instead of rewarding absolute length, it scales or normalizes scores across a group of sampled responses.

```mermaid
flowchart LR
    CandidateGroup["Candidate Group [Y1, Y2, Y3]"] --> GroupStat["Compute Mean & Std Dev of Length/Reward"]
    GroupStat --> Normalize["Apply Group-Relative Normalization"]
    Normalize --> FinalReward["Length-Normalized Reward Tensor"]
```

## Key Characteristics
- **Length Neutrality:** Discourages generating conversational fillers.
- **Group-Relative:** Used in algorithms like GRPO (Group Relative Policy Optimization) to adjust step values.

[Back to README](../README.md)
