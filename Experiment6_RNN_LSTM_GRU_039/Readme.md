# Experiment 7 — Autoencoders

## CS3807 — Deep Learning Laboratory

### Objective
Study Fully Connected Autoencoders Convolutional Autoencoders Denoising Autoencoders and Variational Autoencoders for image reconstruction denoising and generative modeling.

### Dataset
MNIST Handwritten Digit Dataset  
Image size: `28 × 28 × 1`  
Training: `10,000` images  
Testing: `2,000` images  
Pixel values normalized from `[0,255]` to `[0,1]`.

### Models
- Fully Connected Autoencoder
- Convolutional Autoencoder
- Denoising Convolutional Autoencoder
- Variational Autoencoder

### Evaluation
- MSE
- MAE
- SSIM
- Reconstruction error
- Latent space visualization
- Image generation
- Latent interpolation

### Main Results

| Model | MSE | MAE | SSIM | Parameters |
|---|---:|---:|---:|---:|
| FC-AE | 0.019823 | 0.053790 | 0.765471 | 211040 |
| Conv-AE | 0.002706 | 0.015344 | 0.972631 | 74497 |
| Denoising CAE | 0.004687 | 0.021415 | 0.943362 | 74497 |

### Denoising Results

| Gaussian Noise | MSE | MAE | SSIM |
|---:|---:|---:|---:|
| σ = 0.1 | 0.003753 | 0.018029 | 0.958518 |
| σ = 0.2 | 0.004687 | 0.021415 | 0.943362 |
| σ = 0.3 | 0.007183 | 0.030019 | 0.862765 |

### VAE Results

```text
Reconstruction Loss = 168.6003
KL Loss = 4.8065
Total Loss = 173.4068

Test MSE = 0.043513
Test MAE = 0.102146
Test SSIM = 0.493061
