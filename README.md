# CNN From Scratch — CIFAR-10

A simple convolutional neural network built from scratch in PyTorch, trained on the CIFAR-10 dataset. This is a learning exercise to understand CNN fundamentals before applying them to the PRISM project.

## What it does

Classifies 32x32 colour images into 10 categories (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck) using a CNN with four convolutional layers, two max-pooling layers, and two fully connected layers.

## Architecture

```
Input (3x32x32 RGB image)
  → Conv2d (3→32, 3x3) → Conv2d (32→32, 3x3) → MaxPool2d (2x2)
  → Conv2d (32→64, 3x3) → Conv2d (64→64, 3x3) → MaxPool2d (2x2)
  → Flatten → Linear (1600→128) → ReLU → Linear (128→10)
  → Output (10 class scores)
```

## Tech

- Python 3
- PyTorch
- Torchvision (CIFAR-10 dataset + transforms)
- Google Colab (T4 GPU)

## How to run

Open `entry-0-setup.ipynb` in Google Colab and run all cells. The dataset downloads automatically on first run. Training runs for 20 epochs.

## Purpose

Part of a learning curve toward building [PRISM](https://github.com/ShemeshiRobert) — an explainable cross-modal ranking system for forensic evidence triage. This project covers Entry 0 (setup) and Entry 1 (CNN basics) of the learning plan.
