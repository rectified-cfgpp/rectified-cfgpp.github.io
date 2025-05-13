# Rectified-CFG++: Rectified Classifier-Free Guidance for Diffusion Models

Official PyTorch implementation of [**Rectified-CFG++: Rectified Classifier-Free Guidance for Diffusion Models**](https://arxiv.org/abs/XXXX.XXXXX).

**[Code will be released soon…]**

Given a plain text prompt (and optional reference style or content), our method **Rectified-CFG++** augments standard classifier-free guidance with a rectification term that:  
1. Improves prompt adherence (higher CLIP / ImageReward)  
2. Preserves sample diversity  
3. Enhances generation quality (lower FID)  
across multiple backbone T2I models (SD3, SD3.5, Flux-dev, Lumina).

![teaser](./data/teaser.png)

---

## 🔥 Updates

- **2025.02.10** First release of README and code skeleton.  
- *(coming soon)* Pretrained weights & example notebooks!

---

## Installation

```bash
git clone https://github.com/your-org/rectified-cfgpp.git
cd rectified-cfgpp
pip install -r requirements.txt
