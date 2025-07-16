# 📡 Phase Unwrapping and Estimation Using Deep Learning (Internship @ IIST Trivandrum)

This repository contains the implementation of my internship project at **IIST Trivandrum**, where I developed a deep learning-based system to perform **phase unwrapping** — the process of recovering continuous phase information from modulo-\(2\pi\) wrapped interferometric data.

Wrapped phase maps arise in optical interferometry due to the periodic nature of phase, and unwrapping them is essential for extracting accurate surface profiles, displacement fields, or curvature data.

---

## 🔍 Project Summary

- ✅ **Simulated Dataset**  
  Generated 1000 synthetic interferograms with:
  - Random fringe patterns (left & right halves)
  - Reference beam interference
  - Wrapped phase extracted via Fourier-domain filtering
  - Ground truth unwrapped using `skimage.unwrap_phase`

- 🧠 **Model Architecture**  
  Designed a hybrid **U-Net-style CNN** with:
  - Residual blocks in both encoder and decoder
  - Channel + Spatial Attention modules
  - Transformer block as bottleneck to capture global spatial continuity
  - Final output: real-valued continuous phase map

- ⚙️ **Training Details**  
  - Loss Function: Smooth L1 Loss (Huber)
  - Optimizer: Adam (LR = 1e-4)
  - Train/Validation Split: 90% / 10%
  - Input/Output: 100×100 grayscale images

- 📈 **Performance**  
  - **MAE** ≈ 0.0131  
  - **RMSE** ≈ 0.0196  
  - Model robustly predicts unwrapped phase with low error across diverse samples

---

## 🛠️ Tools & Frameworks

- Python, PyTorch
- NumPy, SciPy
- scikit-image (`unwrap_phase`)
- Matplotlib for visualization

---


