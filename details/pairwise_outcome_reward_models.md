# Pairwise Outcome Reward Models

Pairwise Outcome Reward Models evaluate completion pairs globally to enforce preferences.

## Overview
This approach models human preferences by comparing a pair of candidate completions: a chosen response ($y_w$) and a rejected response ($y_l$).

```mermaid
flowchart LR
    Prompt["Prompt (x)"] --> CompletionW["Chosen (y_w)"]
    Prompt --> CompletionL["Rejected (y_l)"]
    CompletionW --> RM["Reward Model"]
    CompletionL --> RM
    RM --> ScoreW["Score r(x, y_w)"]
    RM --> ScoreL["Score r(x, y_l)"]
    ScoreW & ScoreL --> Loss["Bradley-Terry Loss"]
```

## Key Characteristics
- **Pairwise Preferences:** Learns from binary comparisons.
- **Outcome-Supervised:** Evaluates the final outcome globally.
- **Limitation:** Sycophancy and verbosity bias (reward hacking).

[Back to README](../README.md)
