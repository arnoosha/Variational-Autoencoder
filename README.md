# Variational Autoencoder on MNIST

This project implements a **Variational Autoencoder (VAE)** for the MNIST handwritten digit dataset.  
The main focus is on exploring and comparing the effects of different latent space dimensions on reconstruction quality and latent representations.

---

## Project Overview

- **Dataset:** MNIST handwritten digits (grayscale, 28×28 pixels).  
- **Model:** Variational Autoencoder (encoder + decoder) built with PyTorch.  
- **Latent Space:** Models are trained and tested with different latent dimensions (e.g., 2, 4, 16).  
- **Training:** Each model is optimized using a combination of binary cross-entropy reconstruction loss and Kullback–Leibler (KL) divergence regularization.  
- **Evaluation Metrics:**
  - **Pixel Accuracy:** Measures how closely reconstructed images match binary thresholded originals.
  - **PSNR (Peak Signal-to-Noise Ratio):** Quantifies reconstruction quality.
- **Visualization:**
  - Latent space visualizations (with t-SNE applied for higher dimensions).  
  - Original vs. reconstructed images for qualitative comparison.

---

## Key Components

- **Encoder:** Compresses the input image into a latent distribution defined by mean and log variance.  
- **Reparameterization:** Samples latent vectors using the reparameterization trick to enable backpropagation.  
- **Decoder:** Reconstructs images from sampled latent vectors.  
- **Training Loop:** Optimizes the VAE using stochastic gradient descent with reconstruction and KL divergence losses.  
- **Testing:** Evaluates reconstruction performance, computes accuracy and PSNR, and collects latent embeddings for visualization.  
- **Visualization Tools:**
  - Latent space scatter plots colored by digit labels.
  - Side-by-side comparison of original and reconstructed images.

