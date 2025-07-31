This repo contains all work and learnings during SOC 2025 project whose details are:
Mentor: Manit Jhajharia
 Project Name: Image Style Transfer using GANs
 Project UID: 46
# CycleGAN: Horse to Zebra Image Translation

This project implements an **unpaired image-to-image translation** using **CycleGAN**, trained on the `horse2zebra` dataset.

## 🧠 About the Project

The goal is to translate images of **horses into zebras** using a **CycleGAN** architecture. Unlike Pix2Pix, CycleGAN does not require paired images. This makes it suitable for many real-world use cases where paired data is scarce.

## 📂 Dataset

- Dataset: [Kaggle Horse2Zebra Dataset](https://www.kaggle.com/datasets/suraj332/horse2zebra)
- Format: Provided as `archive.zip`, containing `trainA`, `trainB`, `testA`, `testB`

## 🏗️ Model Architecture

CycleGAN consists of:
- 2 Generators (G_AB and G_BA)
- 2 Discriminators (D_A and D_B)
- Cycle Consistency Loss
- Identity Loss (optional)
- Adversarial Loss (with PatchGAN)

## 📦 Requirements

- Python 3.7+
- PyTorch
- torchvision
- matplotlib
- numpy
- tqdm
- PIL

## 🚀 How to Run

```bash
# Upload archive.zip to your Colab or local environment

# Unzip data
!unzip archive.zip

# Train CycleGAN
# Set up data loaders, define models (G_AB, G_BA, D_A, D_B), losses, optimizers

# Train for 10 epochs (modifiable)
for epoch in range(10):
    # training loop
