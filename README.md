# Safe Offline Reinforcement Learning for Sepsis Treatment Decisions

This repository contains a MATLAB® demo:

- `OfflineRLForClinicalDecisions.m`

​​This is a demo that demonstrates how Artificial Intelligence (AI) can learn optimal treatment protocols for disease management by analyzing historical Electronic Medical Records (EMR) data.​

Open `OfflineRLForClinicalDecisions.m` in the MATLAB Live Editor and run it section by section. The file interleaves explanation, code, tables, and figures so you can see what each step does and why it matters.

Click below to open the GitHub repository in MATLAB Online™:
[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?host=insidelabs-git.mathworks.com&repo=fnae/reinforcement-learning-for-clinicians)

The example is for clinicians, clinical AI evaluators, and MATLAB users who want to understand a **safety-focused offline reinforcement learning** workflow. 

## Requirements

- MATLAB R2025a or later, to open the plain-text live script in the Live Editor
- Reinforcement Learning Toolbox™
- `OfflineRLForClinicalDecisions.m`
- `sepsis_training_data.csv`, optional; if this file is missing, the live script generates the synthetic data and saves a new CSV cache

The demo uses Reinforcement Learning Toolbox functionality to construct a tabular DQN agent, load historical records into replay memory, and train the agent offline. The required offline-training APIs were introduced in R2023a; the R2025a version requirement above is set by the plain-text Live Script format, introduced in R2025a.

## Data

The demo uses *synthetic sepsis treatment records*, no real clinical data is used. 

If `sepsis_training_data.csv` exists, the live script loads it as a cache. If the CSV file is missing, the live script generates synthetic data automatically and saves a new cache.

## What You Learn

- How historical records `(state, action, reward, next state)` become offline reinforcement learning experience
- How Reinforcement Learning Toolbox trains a Q-learning policy from historical data
- How a conservative count-based penalty blocks actions that lack historical support
- How bootstrap disagreement and evidence counts help audit a recommendation 

*Copyright (c) 2026, The MathWorks, Inc.*
