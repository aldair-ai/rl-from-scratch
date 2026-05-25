# Reinforcement Learning from Scratch ✏️ 

**Implementing David Silver's UCL RL Course — Theory + Code in Parallel**

[![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> *"More data beats clever algorithms, but better representations beat more data."*  
> — David Silver

This repository implements every major algorithm from David Silver's UCL Reinforcement Learning course
([lecture series](http://www.cs.ucl.ac.uk/staff/D.Silver/web/Teaching.html)) from scratch in Python —
no RL libraries, no gym wrappers, just NumPy and the math.

Each lecture has a paired notebook that follows a consistent pattern:
the concept in plain English → the key equation → the implementation → a visualization → the key insight.

---

## 🗂️ Course Modules

| Lecture | Topic | Core Algorithms | Notebook |
|---------|-------|-----------------|----------|
| 01 | [Introduction to RL](./lecture-01-introduction/) | Gridworld · Agent-Environment loop · MDP preview | [![Open](https://img.shields.io/badge/Open-Notebook-orange)](./lecture-01-introduction/notebook.ipynb) |
| 02 | [Markov Decision Processes](./lecture-02-mdp/) | Bellman expectation · Bellman optimality | [![Open](https://img.shields.io/badge/Open-Notebook-orange)](./lecture-02-mdp/notebook.ipynb) |
| 03 | [Dynamic Programming](./lecture-03-dynamic-programming/) | Policy evaluation · Policy iteration · Value iteration | [![Open](https://img.shields.io/badge/Open-Notebook-orange)](./lecture-03-dynamic-programming/notebook.ipynb) |
| 04 | [Model-Free Prediction](./lecture-04-model-free-prediction/) | Monte Carlo · TD(0) · TD(λ) | [![Open](https://img.shields.io/badge/Open-Notebook-orange)](./lecture-04-model-free-prediction/notebook.ipynb) |
| 05 | [Model-Free Control](./lecture-05-model-free-control/) | SARSA · Q-learning · On-policy vs Off-policy | [![Open](https://img.shields.io/badge/Open-Notebook-orange)](./lecture-05-model-free-control/notebook.ipynb) |
| 06 | [Value Function Approximation](./lecture-06-value-function-approximation/) | Linear · Neural net · SGD | [![Open](https://img.shields.io/badge/Open-Notebook-orange)](./lecture-06-value-function-approximation/notebook.ipynb) |
| 07 | [Policy Gradient](./lecture-07-policy-gradient/) | REINFORCE · Actor-Critic · Baseline | [![Open](https://img.shields.io/badge/Open-Notebook-orange)](./lecture-07-policy-gradient/notebook.ipynb) |
| 08 | [Integrating Learning & Planning](./lecture-08-integrating-learning-planning/) | Dyna-Q · Model-based RL | [![Open](https://img.shields.io/badge/Open-Notebook-orange)](./lecture-08-integrating-learning-planning/notebook.ipynb) |
| 09 | [Exploration & Exploitation](./lecture-09-exploration-exploitation/) | UCB · Thompson Sampling · Bandits | [![Open](https://img.shields.io/badge/Open-Notebook-orange)](./lecture-09-exploration-exploitation/notebook.ipynb) |
| 10 | [RL in Games](./lecture-10-rl-in-games/) | Self-play · MCTS · AlphaGo concepts | [![Open](https://img.shields.io/badge/Open-Notebook-orange)](./lecture-10-rl-in-games/notebook.ipynb) |

*Notebooks added weekly as the course progresses.*

---

## 🧠 What This Repo Demonstrates

- **RL fundamentals from scratch** — every algorithm implemented in pure NumPy, no RL libraries
- **Theory meets code** — each mathematical concept paired with a working implementation
- **Progressive complexity** — from tabular methods to function approximation to policy gradients
- **Visual understanding** — every algorithm visualized on gridworlds, plots, and animations
- **Connection to practice** — lecture 09 (exploration) directly informs the
  [`abaudit`](https://github.com/aldair-ai/abaudit) bandit-testing extension

---

## 🛠️ Setup

```bash
git clone https://github.com/aldair-ai/rl-from-scratch.git
cd rl-from-scratch
pip install -r requirements.txt
jupyter lab
```

Open any lecture folder and run the notebook top to bottom.

---

## 📁 Repo Structure

```
rl-from-scratch/
├── README.md
├── requirements.txt
├── lecture-01-introduction/
│   ├── README.md          ← theory: agent, environment, reward, state, Markov property
│   └── notebook.ipynb     ← gridworld implementation + policy/value visualization
├── lecture-02-mdp/
│   ├── README.md          ← theory: MDPs, Bellman equations
│   └── notebook.ipynb     ← Bellman expectation + optimality from scratch
├── lecture-03-dynamic-programming/
│   ├── README.md          ← theory: policy evaluation, improvement, iteration
│   └── notebook.ipynb     ← policy iteration + value iteration on gridworld
├── lecture-04-model-free-prediction/
│   ├── README.md          ← theory: Monte Carlo, TD learning
│   └── notebook.ipynb     ← MC vs TD convergence comparison
├── lecture-05-model-free-control/
│   ├── README.md          ← theory: SARSA, Q-learning
│   └── notebook.ipynb     ← SARSA vs Q-learning on cliff walking
├── lecture-06-value-function-approximation/
│   ├── README.md
│   └── notebook.ipynb
├── lecture-07-policy-gradient/
│   ├── README.md
│   └── notebook.ipynb
├── lecture-08-integrating-learning-planning/
│   ├── README.md
│   └── notebook.ipynb
├── lecture-09-exploration-exploitation/
│   ├── README.md
│   └── notebook.ipynb
└── lecture-10-rl-in-games/
    ├── README.md
    └── notebook.ipynb
```

---

## 📚 References

- Silver, D. (2015). *UCL Course on Reinforcement Learning.*
  [Lecture slides](http://www.cs.ucl.ac.uk/staff/D.Silver/web/Teaching.html)
- Sutton, R.S. & Barto, A.G. (2018). *Reinforcement Learning: An Introduction (2nd ed.).*
  MIT Press. [Free online](http://www.incompleteideas.net/book/the-book.html)
- Szepesvári, C. (2010). *Algorithms for Reinforcement Learning.*
  [Free online](https://sites.ualberta.ca/~szepesva/papers/RLAlgsInMDPs.pdf)

---

## 👤 About

**Edwin Aldair Espinoza Zegarra** · MS Data Science · UC San Diego · 2025–2026

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/aldair-ai/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/aldair-ai)

---
*Related project: [`abaudit`](https://github.com/aldair-ai/abaudit) — A/B test validity auditor
built on the statistical foundations covered in lecture 09.*
