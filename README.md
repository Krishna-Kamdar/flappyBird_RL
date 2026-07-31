# Flappy Bird Deep Q-Learning (DQN) Agent

An implementation of a Deep Q-Network (DQN) using PyTorch to autonomously play Flappy Bird. This project trains a reinforcement learning agent to navigate through pipes by learning optimal flapping strategies directly from the game's state space.

## 🧠 Project Overview
This repository features a custom Reinforcement Learning agent that utilizes **Experience Replay** and a **Target Network** to master the Flappy Bird environment. 

A key technical highlight of this implementation is the use of **Layer Normalization** within the neural network. This stabilizes the training process by scaling the raw coordinate data provided by the game, preventing exploding gradients and allowing the agent to converge on a winning strategy efficiently.

## 📂 Repository Structure

* **`agent.py`**: The core Reinforcement Learning agent. Contains the training loop, epsilon-greedy action selection, loss calculation, and optimization steps.
* **`dqn.py`**: The PyTorch neural network architecture. Defines the layers of the Deep Q-Network, including the `nn.LayerNorm` for data stabilization.
* **`experience_replay.py`**: The memory buffer class. Stores past transitions (state, action, reward, next_state) and samples them randomly in mini-batches to break correlation during training.
* **`game_flappy_bird.py`**: The environment wrapper that interfaces with the Flappy Bird game engine.
* **`parameters.yaml`**: The central configuration file containing all tunable hyperparameters (learning rate, epsilon decay, batch size, etc.).

## ⚙️ Installation

1. Clone the repository:
   ```bash
   git clone [https://github.com/YourUsername/YourRepoName.git](https://github.com/YourUsername/YourRepoName.git)
   cd YourRepoName
