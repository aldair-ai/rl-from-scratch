# Lecture 01 — Introduction to Reinforcement Learning

**Source:** David Silver, UCL RL Course, Lecture 1  
**Reference:** Sutton & Barto (2018), Chapter 1

---

## 📖 Theory Summary

### What is Reinforcement Learning?

RL is the study of how an **agent** learns to make decisions by interacting with an **environment**
to maximize **cumulative reward**. It differs from supervised and unsupervised learning in three key ways:

- No supervisor — only a reward signal
- Feedback is delayed, not instantaneous
- Time matters — sequential, non-i.i.d. data
- Agent's actions affect the data it sees next

### The Agent-Environment Loop

At each time step $t$:

```
Agent  →  action Aₜ   →  Environment
Agent  ←  observation Oₜ  ←  Environment
Agent  ←  reward Rₜ   ←  Environment
```

The agent's **goal** is to maximize total future reward:

$$G_t = R_{t+1} + R_{t+2} + R_{t+3} + \ldots = \sum_{k=0}^{\infty} \gamma^k R_{t+k+1}$$

The discount factor $\gamma \in [0, 1]$ controls how much the agent values immediate vs. future rewards.

### State and the Markov Property

The **history** is the full sequence of observations, actions, and rewards:

$$H_t = O_1, R_1, A_1, \ldots, A_{t-1}, O_t, R_t$$

The **state** is the information used to decide what happens next. A state $S_t$ is **Markov** if:

$$P[S_{t+1} \mid S_t] = P[S_{t+1} \mid S_1, \ldots, S_t]$$

"The future is independent of the past given the present." Once you know the current state, the history can be thrown away.

### Components of an RL Agent

An RL agent has up to three components:

| Component | What it does |
|-----------|-------------|
| **Policy** $\pi(a \mid s)$ | Maps states to actions — the agent's behaviour |
| **Value function** $v_\pi(s)$ | Predicts expected future reward from state $s$ |
| **Model** | Agent's internal representation of the environment |

### Exploration vs. Exploitation

The fundamental tension in RL:

- **Exploitation** — use known information to maximize immediate reward
- **Exploration** — gather new information about the environment

A good agent must do both. Too much exploitation → stuck in local optima.
Too much exploration → never uses what it learned.

---

## 💻 Notebook

The notebook implements:

1. The `GridWorld` environment from Silver's slides (maze example)
2. A random policy — visualize where the agent goes
3. The value function $v_\pi(s)$ for the random policy — matching Silver's slide exactly
4. The optimal policy $\pi^*$ — matching Silver's slide
5. The discount factor effect — how $\gamma$ changes what the agent values

---

## 🔑 Key Insight

The value function $v_\pi(s)$ tells you how good it is to be in a state — *given a specific policy*.
The optimal value function $v^*(s)$ tells you the best you can possibly do from that state.
The gap between them is what RL algorithms are trying to close.
