# 🌟 Welcome to the U-Net Denoising Project! 🌟

👋 **Hello there! Thank you for visiting my repository.** 

This project was developed as an **individual school project** focused on deep learning and image processing. It implements a **U-Net architecture** from scratch to denoise images, removing unwanted noise to restore clarity. 

---

## 🏫 Project Overview
This repository serves an **educational purpose** to demonstrate the inner workings of convolutional neural networks (CNNs) for image restoration. 

The entire project is built and optimized to run seamlessly on 📊 **Google Colab**, utilizing its free GPU acceleration.

### ⚠️ Disclaimer & Usage
> 🔴 **Important Notice:** This project is intended **strictly for educational purposes**. It is a student submission and should be used as a learning reference only.

---

## 🚀 Google Colab Setup Guide

To run this project, open the notebook in Google Colab and follow these initialization steps:

### 📁 1. Linking Google Drive
We use Google Drive to store and source our image dataset. Run the following code cell in Colab to mount your drive:
```python
from google.colab import drive
drive.mount('/content/drive')
srcpath = 'your_srcpath'  #@param {type:'string'}
srcpath = os.path.join('/content/drive/My Drive', srcpath)
```

### 📦 2. Importing Libraries
Ensure you have the required deep learning framework and image processing tools imported at the top of your notebook:
```python
import torch
import torch.nn as nn
import torch.optim as optim
from torch.utils.data import DataLoader, Dataset
import torchvision.transforms as transforms
import numpy as np
import matplotlib.pyplot as plt
from PIL import Image
```

---

## 📑 Notebook Structure

The notebook is cleanly divided into three core sections:

### 🧩 [Part 1] Neural Network Implementation
*   Coding the encoder (downsampling), decoder (upsampling), and critical **skip connections**.

### 🧪 [Part 2] Hyperparameter Testing & Experiments
An in-depth exploration of how different settings affect model training efficiency and final loss. Tests include:
*   📈 **Learning Rate:** Tuning the optimization step size.
*   ⏳ **Epochs:** Evaluating underfitting vs. overfitting over time.
*   📦 **Batch Size:** Finding the balance between memory limit and gradient stability.
*   🔄 **Activation Functions:** A direct comparison of performance using **Sigmoid vs. ReLU**.

### 🖼️ [Part 3] Dataset Preparation & Model Training
*   **Data Pipeline:** Steps for pairing clean images with artificial noise to create a synthetic dataset.
*   **Training Loop:** Implementing the complete training process, monitoring loss curves, and saving the best-performing weights.
*   Detailed walkthrough of building the **U-Net architecture**.

---
## 📊 Results & 🎨 Visualizations

We utilized `matplotlib.pyplot` to track training performance and visually compare the impact of different hyperparameters. Below are the metrics captured during testing:

### 📈 1. Hyperparameter Performance Charts
Using line graphs, we plotted the **Training Loss vs. Epochs** to evaluate how smoothly the model converged under different configurations:

*   **🟢 Learning Rate Impact:** Comparing fast but unstable convergence (high LR) against slow, steady progress (low LR).
*   **🔵 Batch Size Efficiency:** Visualizing how smaller batch sizes created noisy gradients compared to smoother curves from larger batches.
*   **🟡 Activation Function Battle (ReLU vs. Sigmoid):** Graphs showing the clear difference in gradient flow and final loss when swapping the activation layers.

### 🖼️ 2. Visual Denoising Output
Using `plt.imshow()`, the final notebook generates a side-by-side visual comparison to evaluate the network's real-world performance:




💡 *If you find this project helpful for your learning journey, feel free to give it a ⭐!*
