# Week 2: Markov Decision Processes
### David Silver's Reinforcement Learning Course

---

## Overview

This week formalises the **environment** in reinforcement learning using the mathematical framework of **Markov Decision Processes (MDPs)**. We build up from the simplest case (Markov Chains) to the full MDP, then introduce the key equations needed to reason about and solve them.

---

## Topics Covered

### 1. Markov Processes
- The **Markov Property**: the future is independent of the past given the present
- **State Transition Matrices**: encoding all transition probabilities compactly
- **Markov Chains**: sampling episodes from a random process

### 2. Markov Reward Processes (MRPs)
- Adding **rewards** and a **discount factor** γ to a Markov Chain
- The **Return** Gₜ: total discounted future reward
- **Value Function** v(s): expected return from state s
- **Bellman Equation** for MRPs: recursive decomposition of value

### 3. Markov Decision Processes (MDPs)
- Adding **actions** and **policies** to an MRP
- **State-value** vπ(s) and **action-value** qπ(s, a) functions
- **Bellman Expectation Equations**: v in terms of q and vice versa
- **Optimal Value Functions** v*(s) and q*(s, a)
- **Bellman Optimality Equations**: the non-linear equations that characterise optimal behaviour

### 4. Extensions (No Exam)
- Infinite and continuous MDPs
- Partially Observable MDPs (POMDPs) and belief states
- Ergodic MDPs and average reward formulations

---

## Notebooks

| Notebook | Description |
|---|---|
| `01_markov_processes.ipynb` | Markov property, transition matrices, chain simulation |
| `02_markov_reward_processes.ipynb` | Returns, discounting, value functions, Bellman equation |
| `03_markov_decision_processes.ipynb` | Policies, Bellman expectation & optimality, solving MDPs |

---

## Key Equations

**Bellman Equation (MRP)**
```
v(s) = Rₛ + γ Σₛ' Pₛₛ' v(s')
```

**Bellman Expectation (MDP — state value)**
```
vπ(s) = Σₐ π(a|s) [Rₛᵃ + γ Σₛ' Pₛₛ'ᵃ vπ(s')]
```

**Bellman Optimality (state value)**
```
v*(s) = max_a [Rₛᵃ + γ Σₛ' Pₛₛ'ᵃ v*(s')]
```

**Bellman Optimality (action value)**
```
q*(s, a) = Rₛᵃ + γ Σₛ' Pₛₛ'ᵃ max_a' q*(s', a')
```

---

## Running the Notebooks

```bash
pip install numpy matplotlib jupyter
jupyter notebook
```

No special RL libraries required — everything is implemented from scratch using NumPy.

---

## The Student MDP Example

All three notebooks use the same running example from the lecture: a student who must decide whether to Study, browse Facebook, or go to the Pub.

| State | Reward |
|---|---|
| Class 1 | −2 |
| Class 2 | −2 |
| Class 3 | −2 |
| Facebook | −1 |
| Pub | +1 |
| Pass | +10 |
| Sleep | 0 |

The goal is to find the policy that maximises expected cumulative reward — i.e., the path through university that earns the most total "reward".

---

## Prerequisites

- Basic probability (expectations, conditional probability)
- Linear algebra (matrix–vector multiplication)
- Python / NumPy basics

---

*Based on Lecture 2 of David Silver's RL Course (UCL / DeepMind)*
