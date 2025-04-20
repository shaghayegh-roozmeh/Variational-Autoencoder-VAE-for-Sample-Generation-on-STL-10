# Variational-Autoencoder-VAE-for-Sample-Generation-on-STL-10
This project implements a Variational Autoencoder (VAE) in PyTorch, trained on the STL-10 dataset. Rather than reconstructing input images, the VAE is used to **generate new, realistic samples** by learning a latent representation of the dataset.
# Variational Autoencoder (VAE) for Sample Generation on STL-10

## 📌 Project Overview

This project implements a **Variational Autoencoder (VAE)** in PyTorch, trained on the **STL-10 dataset**. Rather than reconstructing input images, the VAE is used to **generate new, realistic samples** by learning a latent representation of the dataset.

The primary objectives of this notebook are:
- Build a basic VAE model.
- Train it on STL-10 natural images.
- Generate new images by sampling from the learned latent space.

---

## 📁 Project Structure

- `VAE.ipynb`: Jupyter Notebook containing model definition, training loop, and image generation code.

---

## 🚀 Code Summary

### 1. **Setup & Imports**
The notebook imports all necessary libraries, sets up the computing device (CPU/GPU), and defines hyperparameters.

### 2. **Data Loading**
The STL-10 dataset is loaded and preprocessed using `torchvision.transforms` to convert images into normalized tensors suitable for training.

### 3. **Model Definition**
The VAE class contains:
- **Encoder**: Maps high-dimensional images to a lower-dimensional latent space (mean and log variance).
- **Reparameterization**: Samples latent vectors using the reparameterization trick.
- **Decoder**: Generates images from latent vectors.

### 4. **Loss Function**
- **Reconstruction Loss** (Binary Cross-Entropy or MSE): Measures how well the generated sample matches expected output (used during training).
- **KL Divergence**: Encourages the latent distribution to be close to a standard normal distribution.

### 5. **Training Process**
- The model is trained on STL-10 images for several epochs.
- Each batch is passed through the encoder and decoder.
- The combined loss is used to update model weights using the Adam optimizer.

### 6. **Image Generation**
- After training, new image samples are **generated from randomly sampled latent vectors**.
- These samples are visualized to show the VAE’s generative capability.

---

## 🎨 Results
The trained VAE generates **new STL-10-style images**, demonstrating its ability to capture the underlying data distribution through unsupervised learning.
