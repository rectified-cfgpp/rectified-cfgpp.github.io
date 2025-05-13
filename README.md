# Rectified-CFG++ for Flow Based Models

[![NeurIPS Submission](https://img.shields.io/badge/NeurIPS-2024-orange)](https://neurips.cc) [![ArXiv](https://img.shields.io/badge/arXiv-2406.08070-blue)](https://arxiv.org/abs/2406.08070) [![License](https://img.shields.io/badge/License-MIT-green)](./LICENSE)

A **training-free**, **geometry-aware** guidance scheme for flow-based text-to-image (T2I) models. Rectified-CFG++ replaces the naïve extrapolation of classifier-free guidance (CFG) with a predictor–corrector integrator that stays on the learned data manifold, eliminating oversaturation and structural artifacts while improving prompt alignment and sampling efficiency.

---

## 📖 Table of Contents

1. [Features](#-features)  
2. [Installation](#-installation)  
3. [Quick Start](#-quick-start)  
4. [API Usage](#-api-usage)  
5. [Configuration](#-configuration)  
6. [Examples](#-examples)  
7. [Benchmarks & Results](#-benchmarks--results)  
8. [Citation](#-citation)  
9. [License](#-license)

---

## ✨ Features

- **On-Manifold Sampling**  
  Predictor–corrector updates keep trajectories within a bounded tubular neighborhood of the data manifold.
- **Training-Free**  
  Drop-in replacement for standard CFG—no additional training or fine-tuning required.
- **Model-Agnostic**  
  Works with any transformer-based rectified-flow T2I backbone (e.g., Flux, SD3/3.5, Lumina-Next).
- **Stable Across Scales**  
  Maintains visual fidelity and prompt alignment even at high guidance strengths.
- **Efficient**  
  Achieves state-of-the-art FID and CLIP-Score with 20–30% fewer function evaluations.

---

## 🛠️ Installation

1. **Clone the repository**  
   ```bash
   git clone https://github.com/PLACEHOLDER/rectified-cfgpp.git
   cd rectified-cfgpp

2. **Create a Python environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt

## 🚀 Quick Start

Generate images with Rectified-CFG++ using a pre-trained Flux model:
   ```bash
        python scripts/sample.py \
            --model_name flux-dev \
            --prompt "A neon sign that says 'CyberCore Café', glowing in magenta and blue" \
            --guidance_method rectified-cfgpp \
            --guidance_scale 3.0 \
            --num_inference_steps 20 \
            --output_dir outputs/

## 📚 Citation
--SOON--


