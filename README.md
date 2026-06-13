# Skin Lesion Classification — CNN vs ViT vs Hybrid

> Comparing CNN, Vision Transformer, and Hybrid architectures for skin lesion 
> classification on HAM10000 under limited data conditions.

---

## What This Is

This is an ongoing research project I'm working on as part of my journey into 
AI/ML research. The core question I'm trying to answer:

**Can a Hybrid CNN-Transformer model outperform standalone CNN and ViT models 
for skin lesion classification — especially when training data is limited?**

Medical imaging felt like the right place to start. The dataset is small enough 
to work with on free compute, the problem is real, and the class imbalance makes 
it genuinely challenging.

---

## Dataset

**HAM10000** — Human Against Machine with 10,000 training images  
10,015 dermoscopy images across 7 skin lesion classes

| Class | Full Name | Samples |
|-------|-----------|---------|
| nv | Melanocytic Nevi | 6,705 |
| mel | Melanoma | 1,113 |
| bkl | Benign Keratosis | 1,099 |
| bcc | Basal Cell Carcinoma | 514 |
| akiec | Actinic Keratoses | 327 |
| vasc | Vascular Lesions | 142 |
| df | Dermatofibroma | 115 |

Heavy class imbalance (67:1 ratio) — addressed using WeightedRandomSampler 
and weighted CrossEntropy loss.

---

---

## Models

| Model | Type | Role |
|-------|------|------|
| EfficientNet-B3 | CNN | Baseline |
| ViT-Small (patch16) | Transformer | Baseline |
| Hybrid (CNN + Transformer) | Hybrid | Our Contribution |

All models pretrained on ImageNet and fine-tuned on HAM10000.

---


## About

> Built by **Maavia Rizwan** — CS student, AI/ML researcher.  
> DIP Lab - Islamia College Peshawar.

Part of [Synaptix](https://github.com/maaviarizwan) — a student AI collective.

This is a work in progress. Notebooks, figures, and results update as each 
stage completes. Feedback and suggestions welcome.
