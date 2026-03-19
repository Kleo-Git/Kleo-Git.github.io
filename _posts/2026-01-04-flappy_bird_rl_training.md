---
layout: default
title: "Deep Reinforcement Learning for Flappy Bird"
date: 2026-01-04
description: "Using deep RL techniques to teach an agent to play flappy bird"
---

# Project Overview
This project explores the training of agents to play Flappy Bird using Deep Reinforcement Learning algorithms. Using the flappy-bird-gymnasium environment, I implemented and benchmarked several architectures to observe how different mathematical approaches would handle real time decision making.

# Purpose
The goal was to move from neuroevolution and implement and understand full reinforcement learning.

# Methodology
I implemented and compared four distinct RL agents:

* **DQN**: A value-based approach using a neural network to estimate the "quality" of an action in a given state.
* **Double DQN (DDQN)**: Improved the standard DQN by decoupling action selection from action evaluation, significantly reducing the overestimation of Q-values.
* **Dueling DQN**: Used a split network architecture to separately calculate the state value and the action values.
* **REINFORCE**: A policy-gradient method that directly optimizes the bird's strategy, resulting in smoother,

[Link to Repo](https://github.com/Kleo-Git/flappy_bird_rl_training)