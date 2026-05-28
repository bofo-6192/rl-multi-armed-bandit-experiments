# RL Multi-Armed Bandit Experiments

This project explores the **multi-armed bandit problem**, a classic reinforcement learning problem focused on the trade-off between **exploration** and **exploitation**.

The notebook demonstrates how an agent learns to choose better actions over time by receiving rewards, updating estimated action values, and comparing different learning strategies.

## Project Overview

The project uses a **10-armed bandit environment**, where each arm has a hidden true reward value. The agent does not know the best arm at the beginning and must learn from experience.

The notebook includes experiments on:

* Greedy action selection
* Epsilon-greedy exploration
* Random tie-breaking argmax
* Average reward over time
* Optimal action selection percentage
* Sample-average update rule
* Constant step-size update rule
* Alpha learning-rate comparison
* Stationary vs non-stationary environments
* Visual demo of one agent learning step by step

## Key Concepts

### Exploration vs Exploitation

* **Exploitation** means choosing the action that currently looks best.
* **Exploration** means trying other actions to discover if they may be better.

A good reinforcement learning agent needs a balance between both.

### Epsilon-Greedy Agent

The epsilon-greedy agent usually chooses the best-known action, but sometimes explores randomly.

The notebook compares different epsilon values:

* `epsilon = 0`
* `epsilon = 0.01`
* `epsilon = 0.1`
* `epsilon = 0.4`

### Learning Rate Alpha

The project also compares different constant step-size values:

* `alpha = 0.01`
* `alpha = 0.1`
* `alpha = 0.5`
* `alpha = 1.0`

Lower alpha values learn slowly, while higher alpha values adapt faster but can become unstable.

## Main Findings

* Greedy agents can get stuck because they do not explore.
* Epsilon-greedy agents perform better because they balance exploration and exploitation.
* Too little exploration slows learning.
* Too much exploration lowers reward.
* Sample-average updates work well in stationary environments.
* Constant step-size updates are better in non-stationary environments because they give more weight to recent rewards.

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Jupyter Notebook

## How to Run

Open the notebook:

```text
multi_armed_bandit_rl.ipynb
```

Then run all cells from top to bottom in Jupyter Notebook, JupyterLab, VS Code, or Google Colab.

## Project Purpose

This project was created as a reinforcement learning portfolio notebook to demonstrate core RL concepts, experimental comparison, and visual analysis using Python.
