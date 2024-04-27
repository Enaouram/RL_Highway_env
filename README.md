# Reinforcement Learning Project Report: Highway Environment

**Authors:** Ayman MOUMEN, Francisco GARCIA, Marouane MAAMAR, Samer LAHOUD

---

This repository contains the code and project report for a Reinforcement Learning (RL) project focused on navigating and learning in a simulated highway environment. The project explored various RL algorithms and parameter tuning strategies to optimize the performance of agents in both discrete and continuous action spaces.

## Project Overview

### 1. Highway-v0 with Discrete Actions

- **Understanding the Environment:** Initial exploration of the "Highway" environment, including state representation, reward structure, and available actions.
- **Implementing a Basic Agent:** Utilized Deep Q-Network (DQN) algorithm to train an agent, addressing challenges such as environment disparities and suboptimal learning.

### 2.  Highway-v0 with Continuous Actions

**Environment Setup and Initial Interaction:** We began by configuring the environment with a continuous action space and interfaced with it using Gymnasium API methods. Initial visualizations revealed the agent's struggle to stay on track when actions were randomly sampled.

**Agent Training:** We employed the Deep Deterministic Policy Gradient (DDPG) algorithm due to its compatibility with continuous action spaces. Challenges included adapting the agent's output to a scalar format and resolving practical implementation issues. DDPG's actor-critic architecture facilitated policy learning and value estimation.

**Key Classes and Their Roles:**
•	DDPGagent: Central to the training process, encapsulating actor and critic networks, handling environment interaction, and updating networks using experiences.
•	Actor: Policy network mapping states to actions.
•	Critic: Assessing policy by calculating the value function.
•	Memory: Replay buffer storing transitions for efficient learning.
•	OUNoise: Implementing Ornstein-Uhlenbeck process for exploration.

**Training Procedure and Performance:** Training was limited to 100 episodes due to time constraints. While improvements were observed, suboptimal behaviors persisted, indicating the need for extended training and hyperparameter optimization. Visualizations demonstrated the evolution of agent performance.

**Comparison with Discrete Environment:** We contrasted continuous and discrete action spaces in terms of control complexity, learning difficulty, convergence, stability, exploration, realism, and algorithm suitability.


### 3. Implementing an Agent in the Parking Environment Parking-v0

- **Environment Setup and MDP:** Developed and trained an agent within a Markov Decision Process (MDP) using the SAC (Soft Actor-Critic) algorithm.
- **Algorithm and Parameters:** Utilized SAC for continuous action spaces, emphasizing sample efficiency and off-policy learning.

#### Key Findings and Insights

- **Parameter Tuning Experiments:** Explored the impact of hyperparameters (e.g., learning rate, tau, sampled goals) on agent performance.
- **Results Analysis:** Evaluated agent success rates, rewards, and convergence across different parameter settings.
- **Visualizations:** Included graphs and figures illustrating agent performance and learning trends.

#### Experiments and Notebooks

The project includes detailed experimental notebooks covering:
- Default Parameter Training
- Learning Rate Tuning
- Tau Parameter Tuning
- Sampled Goals Tuning

Each notebook explores specific aspects of parameter tuning and performance analysis.




