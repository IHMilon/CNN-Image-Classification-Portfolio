# VGG on CIFAR10

## Overview
Custom VGG-style CNN implemented from scratch for CIFAR-10 image classification, optimized for high accuracy with minimal parameters.

## Dataset
- 60,000 color images (32×32) in 10 classes
- Train/Test split: 50k / 10k

## Model & Training
- 8 `conv-bn-relu` blocks + 4 `maxpool` layers, 2 fully connected layers (10 outputs)
- Parameters: *4.76 million* | MACs: *209.70 million*
- 25 epochs, AdamW optimizer, CrossEntropyLoss, OneCycleLR, Batch size: 128, Mixed Precision
- Framework: PyTorch

## Results
- Train/Test Accuracy: 95.84% / 92.38%
- Training time: 12.29 min (1.2× faster with mixed precision)
- Confusion mainly between *cat* and *dog*
- Plots and confusion matrix: see `results/`

## Key Takeaways
- Lightweight VGG achieves strong performance on CIFAR10
- Mixed precision significantly speeds up training
