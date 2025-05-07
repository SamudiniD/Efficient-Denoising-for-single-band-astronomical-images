# Efficient-Denoising-for-single-band-astronomical-images
Final Year Project

---

## 🚀 Project Overview

Ground-based astronomical imaging—such as single-exposure galaxy cutouts from SDSS—suffers from mixed Poisson, Gaussian, and impulsive noise that obscures faint structures (e.g., spiral arms, star-forming regions). Traditional filters often blur these critical features, while many deep models trained on natural images don’t generalize well to astronomy. This project proposes efficient, attention-augmented U-Net models (alongside comparisons to DnCNN, Noise2Noise, and Noise2Void) to denoise single-band galaxy images, balancing high PSNR/SSIM performance with CPU-friendly inference speed. Out-of-distribution tests on PS1 data highlight domain-generalization challenges and guide future survey-independent, real-time denoising solutions 

This repository explores deep-learning-based denoising methods for single-band astronomical images (e.g., SDSS and PS1 galaxy cutouts). It benchmarks several architectures and training paradigms on metrics like PSNR, SSIM, and inference speed—focusing on models that deliver high fidelity while remaining efficient enough for CPU-only deployment.

## 📚 Abstract

Ground-based astronomical images, such as those from the Sloan Digital Sky Survey (SDSS), are often degraded by atmospheric distortion, sensor read-out noise, and cosmic-ray interference. We explore deep-learning denoising—specifically U-Net architectures augmented with self-attention—to recover galaxy structures while maintaining fast inference. Multiple U-Net variants, trained on SDSS cutouts corrupted with synthetic Gaussian, Poisson, and salt-and-pepper noise, are benchmarked against classical and self-supervised baselines (DnCNN, Noise2Noise, Noise2Void) using PSNR and SSIM. The attention-augmented U-Net consistently outperforms others in both quantitative and qualitative evaluations, especially in preserving astrophysical features. However, performance drops on out-of-distribution PS1 data, underscoring domain-adaptation needs. These findings demonstrate the promise of attention-based denoisers for enhancing astronomical images and lay groundwork for survey-agnostic, real-time implementations

Key features:
- **U-Net** (baseline vs. attention/multi-head variants)  
- **DnCNN-Complex** for residual learning  
- **Noise2Noise** self-supervised denoising  
- **Noise2Void** blind-spot masking  

---

## 📂 Repository Structure

├── notebooks/
│ ├── Baseline_U_Net_VS_Best_U_Net.ipynb
│ ├── DnCNN_Complex.ipynb
│ ├── Noise2Noise_100ep.ipynb
│ └── noise2void_ep100.ipynb
├── src/
│ ├── unet.py
│ ├── dncnn_complex.py
│ ├── noise2noise.py
│ └── noise2void.py
├── data/ # (optional) sample FITS or .npy files
├── environment.yml # conda environment specification
├── requirements.txt # pip installable packages
└── README.md



---

## ⚙️ Installation

1. **Clone the repository**  
   ```bash
   git clone https://github.com/SamudiniD/Efficient-Denoising-for-single-band-astronomical-images.git
   cd Efficient-Denoising-for-single-band-astronomical-images

