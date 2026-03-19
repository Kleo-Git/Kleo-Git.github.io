---
layout: default
title: "CNN for facial recognition"
date: 2025-11-27
description: "Train CNN's on facial images to learn to predict gender and age."
---

# Project Overview
This project involves the design and evaluation of two distinct Convolutional Neural Network (CNN) architectures tasked with predicting both Age and Gender from facial images. Using a dataset of 5,000 images with varying poses and lighting, I compared a fully custom-built CNN against a fine-tuned MobileNet architecture to determine the most effective approach for real-world facial analysis.

# Purpose
The primary goal was to master Transfer Learning and Multi-Output architectures. By using one "backbone" to feed two separate "heads,

# Methodology
I benchmarked two different strategies across two different data augmentation pipelines:
1. **Model A (Custom CNN):** 4-block architecture featuring dual Conv2D layers per block for deep feature extraction. It achieved a 6.52 MAE for age.
2. **Model B (MobileNet):** A transfer learning approach where I froze the pre-trained base and fine-tuned the final 10 layers.
3. **Data Augmentation:** I compared "Custom Augmentation" (static) against "TensorFlow Real-time Augmentation" to observe how noise affects model convergence and stability.

[Link to Repo](https://github.com/Kleo-Git/cnn_facial_recognition)