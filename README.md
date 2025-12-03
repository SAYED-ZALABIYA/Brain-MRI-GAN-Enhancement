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


---

## 🧬 Dataset  
The project uses **BraTS (Brain Tumor Segmentation Challenge)** MRI slices in `.h5` format.

- 4 MRI modalities per slice:  
  **FLAIR, T1, T1CE, T2**  
- This project focuses on **FLAIR** as the most tumor-sensitive modality.
- Additional versions (100, 101, …) correspond to **different subjects**, not different classes.

---

## 🛠️ Features  
✔ GAN training for MRI denoising  
✔ LPIPS perceptual loss integration  
✔ Clean / Noisy / Enhanced MRI comparison  
✔ Classification before & after enhancement  
✔ Automatic saving of enhanced slices  
✔ Reproducible training / evaluation pipeline  

---

## 🏗️ Model Components  

### 🔹 Generator — Improved UNet  
- Multi-scale encoder–decoder  
- Residual bottleneck block  
- Skip connections  
- Sigmoid output for image reconstruction  

### 🔹 Discriminator — PatchGAN  
- Classifies local patches instead of the full image  
- Stabilizes GAN training  

### 🔹 Loss Functions  
- **Adversarial (MSE)**
- **L1 Loss (pixel reconstruction)**
- **LPIPS Loss (perceptual similarity)**

---

## 📊 Results  
The pipeline generates **three visual outputs** for each MRI slice:

- **Clean MRI**
- **Noisy MRI**
- **Generated MRI (GAN Output)**

Example:

![Comparison](comparison_clean_noisy_gan.png)

The GAN clearly reduces noise and preserves anatomical structure.

---

## 🧪 Classification Results  
The project trains **ResNet18** twice:

1. **Before Enhancement**  
2. **After Enhancement**

Metrics included:

- Accuracy  
- Precision, Recall, F1-score  
- Confusion Matrix  
- ROC Curve & AUC  

This demonstrates the impact of GAN-based enhancement on downstream medical AI tasks.

---

## 📁 Project Structure  
└── Brain-MRI-GAN-Enhancement/
├── data/
├── generator/
├── classifier/
├── enhanced_outputs/
├── comparison_clean_noisy_gan.png
├── BEST_GENERATOR.pth
├── README.md
└── main.ipynb

---

## 🧑‍💻 Technologies Used  
- Python  
- PyTorch  
- NumPy  
- LPIPS  
- Matplotlib  
- scikit-learn  
- BraTS MRI Dataset  

---

## 📌 Future Work  
- Add full multi-class (LGG vs HGG) dataset  
- Train on 3D volumetric MRI instead of 2D slices  
- Try diffusion models for higher-quality reconstruction  
- Compare UNet-GAN vs CycleGAN vs Diffusion  

---

## 🤝 Contributions  
Pull Requests are welcome — especially for dataset expansion, model improvements, or medical evaluation ideas.

---

## 📜 License  
MIT License – Free for academic and research use.

---

