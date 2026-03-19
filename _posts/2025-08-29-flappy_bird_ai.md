---
layout: post
title: "Flappy Bird AI"
date: 2025-08-29
description: "A self learning AI that masters Flappy Bird using Genetic Algorithm and Neural Networks in Unity"
---

# Project Overview
This project combines a self-built Unity simulation of Flappy Bird with an Evolutionary Algorithm approach to train agents as opposed to tradtional RL.

# Purpose
To explore the the ability of Neuroevolution to understand game physics and mechanics. By building the simulation in Unity and the AI logic from scratch, I gained a deep understanding of:
* **Genetic Operators:** Implementing crossover and mutation to explore the weight-space of the networks.
* **Fitness Function Design:** Crafting a scoring system that rewards distance stayed alive and punishes collisions to guide the evolution.
* **Population Dynamics:** Managing hundreds of simultaneous agents to accelerate the learning process.

# Methodology
The training loop follows a strict biological cycle:
1. **Initialization:** A large number, usually 200+ agents are spawned with randomized neural network weights.
2. **Evaluation:** Each agent's "fitness" is calculated based on how far it travels through the pipes.
3. **Selection:** The top-performing birds (the "Elites") are selected to pass their traits to the next generation.
4. **Crossover & Mutation:** New agents are created by mixing the weights of the elites, with small random mutations to prevent local optima.
It's important to note that a wide range of network configurations are kept from worse performers and further random initializations in order to allow a wide range of explorations.

[Link to Repo](https://github.com/Kleo-Git/flappy_bird_ai)