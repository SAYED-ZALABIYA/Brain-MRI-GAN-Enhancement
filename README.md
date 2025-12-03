# 🧠 Brain MRI Enhancement Using GANs  
### Denoising • Enhancement • Classification Pipeline  
A full deep-learning pipeline for improving Brain MRI quality using a GAN-based enhancement model, followed by a tumor-grade classifier.

---

## 🚀 Project Overview  
Brain MRI images often suffer from noise, low contrast, and poor visibility, which can negatively affect clinical diagnosis and machine-learning models.  
This project proposes a **GAN-based enhancement system** designed to:

- Remove noise from MRI images  
- Improve structural details  
- Enhance visibility of tumors  
- Boost the accuracy of classification models (LGG vs HGG)

The system integrates:

1. **UNet-based Generator (Improved UNet)**
2. **PatchGAN Discriminator**
3. **LPIPS + L1 + Adversarial loss**
4. **MRI classifier (ResNet18)**
5. **Before/After comparison pipeline**

---

## 📂 Pipeline Architecture

