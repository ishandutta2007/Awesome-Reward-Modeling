# Process Reward Models (PRMs)

Process-Supervised Reward Models evaluate individual reasoning steps rather than just the final outcome.

## Overview
Instead of giving a single reward at the end of the text generation, PRMs grade each step of the reasoning path.

```mermaid
flowchart TD
    Prompt["Prompt"] --> Step1["Step 1: Parse input"]
    Step1 --> Score1["PRM: Correct (+)"]
    Score1 --> Step2["Step 2: Apply formula"]
    Step2 --> Score2["PRM: Incorrect (-)"]
    Score2 --> Cascade["Halt/Correct execution early"]
```

## Key Characteristics
- **Step-by-Step Supervision:** Evaluates every line or reasoning checkpoint.
- **Improved Alignment:** Reduces logical fallacies and cascading errors.
- **Resource Intensive:** Requires step-level annotations.

[Back to README](../README.md)
