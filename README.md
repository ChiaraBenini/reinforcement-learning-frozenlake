# Reinforcement Learning on FrozenLake (DP, MC, TD Methods)

## Overview

This project implements and compares several core Reinforcement Learning algorithms on the **FrozenLake-v1** environment from Gymnasium.

The main goal is to study how different learning paradigms behave in a stochastic grid-world setting and to compare their convergence, stability, and performance.

The project includes implementations from scratch using NumPy, along with visualizations of learned policies, value functions, and training dynamics.

---

## Objectives

- Implement fundamental RL algorithms from scratch
- Understand and compare model-based and model-free methods
- Analyze learning behavior in stochastic environments
- Visualize policies, value functions, and training performance

---

## Environment

- **Environment:** FrozenLake-v1 (Gymnasium)
- **Grid size:** 8×8
- **Dynamics:** Slippery (stochastic transitions enabled)
- **Goal:** Reach the terminal goal state while avoiding holes

---

## Implemented Algorithms

### Dynamic Programming (Model-Based)
- Policy Iteration
- Value Iteration

### Monte Carlo Methods
- First-Visit Monte Carlo Prediction
- First-Visit Monte Carlo Control (ε-soft policy)

### Temporal Difference Learning
- TD(0) Prediction
- Expected SARSA (on-policy control)
- Q-Learning (off-policy control)

---

## Key Features

- Full RL pipeline implemented from scratch (no high-level RL libraries)
- Stochastic environment handling via Gymnasium
- Exploration strategies (ε-greedy and ε-soft policies)
- Training diagnostics and evaluation tools

---

## Visualizations

The project includes several visual outputs:

- State-value heatmaps
- Learned policy grids (arrows on grid world)
- Learning curves (reward per episode)
- Step count evolution over training
- Cumulative success plots
- Comparison of algorithm performance

---

## Key Observations

- **Policy Iteration / Value Iteration**
  - Fastest convergence
  - Requires full knowledge of environment dynamics

- **Monte Carlo Methods**
  - Unbiased estimates
  - High variance and slower convergence

- **TD Methods (SARSA, Q-Learning)**
  - Good balance between stability and efficiency
  - Q-Learning performs well in long-term learning

- Exploration (ε-greedy) is critical for convergence in stochastic environments

---

## Results Summary

| Algorithm        | Performance | Stability | Sample Efficiency |
|----------------|------------|----------|-------------------|
| Policy Iteration | High       | Very High | N/A (model-based) |
| Value Iteration  | High       | Very High | N/A (model-based) |
| Monte Carlo      | Medium     | Low       | Low               |
| Expected SARSA   | High       | Medium    | Medium            |
| Q-Learning       | High       | Medium    | High              |

