# 🧠 Deterministic Autoencoders (MNIST & Fashion-MNIST)

Deep learning project implementing **deterministic autoencoders** on **MNIST** and **Fashion-MNIST**.  
We compare **MLP vs CNN** architectures, study the impact of **latent dimension**, and evaluate **regularization** (Dropout, L1) using **PSNR** as the main reconstruction metric.  
A **denoising autoencoder** variant is also included.

---

## 🎯 Goals
- Compare symmetric **3-layer vs 5-layer** encoders/decoders (MLP & CNN).
- Study different **latent sizes** (e.g., 15–600).
- Add **regularization**: Dropout and **L1 penalty** on the embedding.
- Use **PSNR** (Peak Signal-to-Noise Ratio) to assess reconstruction quality.
- Build a **Denoising AE** (Gaussian noise on inputs).
- Visualize the **latent space** (t-SNE / PCA).
- Explore the **decoder as a generator** (random input → decoder).

---

## ⚙️ Methodology (high level)
- Grid search over: `latent_dim`, learning rate, L1 weight, and dropout.
- Train/evaluate MLP and CNN (3L/5L) for 30 epochs per setup.
- Report PSNR and qualitative reconstructions.
- Denoising experiments for different noise variances.
- Latent space visualization and decoder-only sampling.

---

## 📈 Key Findings (example)
- **CNN (3 layers)** achieved the best PSNR and generalization.
- **Larger latent sizes** improved reconstruction; extreme sizes may over-smooth.
- **Dropout** often reduced PSNR; **L1** gave small but consistent gains.
- **Denoising AE** increased robustness at the cost of mild smoothing.
- Latent space (t-SNE) shows clear class separability.
- Decoder can synthesize plausible digits/fashion items (non-probabilistic).

---

## 📦 Repo Structure
```Deterministic_Autoencoders/
├─ notebooks/ # Jupyter notebook
├─ reports/ # Final report + appendices (PDF)
├─ requirements.txt
├─ .gitignore
└─ README.md
```
---

## 🧰 Tech Stack
- TensorFlow / Keras
- NumPy, Pandas
- Matplotlib, Seaborn
- scikit-learn

---
