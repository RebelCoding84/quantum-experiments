# 🇬🇧 [English](README.md) | 🇫🇮 [Suomi](README-fi.md)

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Qiskit](https://img.shields.io/badge/Qiskit-1.0-purple)
![License](https://img.shields.io/badge/License-AGPLv3-green)
![Build](https://img.shields.io/badge/Status-Working-success)

# 🧠 Quantum Experiments – Bell State & VQE Simulation (AI-assisted)

This repository contains an educational quantum computing demo built on **Qiskit** and **VS Code Jupyter**, created and refined **with OpenAI Codex in VS Code**.  
Target audience: students, builders, and security-minded engineers who want a hands-on intro to quantum concepts that are actually useful.

> **Finnish summary:** Tämä repo sisältää 6 kvanttiharjoitetta (Bell-tila, VQE, melu), ajettavissa suoraan VS Codessa. Koodi ja teksti on rakennettu AI-avusteisesti (VS Code + Codex).

---

## 🚀 What’s inside (6 exercises)

1. **Bell state creation & Bloch visualization**  
   Create |Φ⁺⟩ = (|00⟩ + |11⟩)/√2 and show Bloch spheres for both qubits.

2. **Bell circuit visualization**  
   Draw the exact H + CNOT circuit using Matplotlib backend.

3. **VQE optimization – energy minimization**  
   Variational Quantum Eigensolver for the toy Hamiltonian **H = ZI + IZ**.  
   Prints minimum energy (~−2.0) and the optimized parameters, plus the final circuit.

4. **Bell-state measurement & correlation verification**  
   Measure 2,000 shots; histogram shows only **00** and **11** (near-perfect correlation).  
   Also reports ⟨Z⊗Z⟩ ≈ 1.0.

5. **VQE energy landscape (heatmap)**  
   2D heatmap of energy across a grid of (θ, φ) → clear minima valleys.

6. **Noise & decoherence demonstration**  
   Add **depolarizing noise (p=0.05)** and compare histograms: clean vs noisy Bell.  
   Shows how noise breaks entanglement and spreads probability mass.

All exercises live in:  
`exercises/vqe_demo/quantum_demo.ipynb`

---

## 🧩 Why these demos matter

- **Bell entanglement:** foundation for QKD, teleportation, non-classical correlations.  
- **VQE:** the practical hybrid algorithm for near-term devices (chemistry, optimization).  
- **Noise model:** reality check—every useful quantum workflow must reason about noise.

---

## 📦 Requirements

```txt
qiskit
qiskit-aer
numpy
matplotlib
pylatexenc
```

> Installed via: `pip install -r requirements.txt`

If Matplotlib circuit rendering complains about LaTeX bits, ensure `pylatexenc` is installed.

---

## ▶️ How to run

1. Open VS Code in the repo root and select the project venv (Python 3.11+).
2. Open the notebook:  
   `exercises/vqe_demo/quantum_demo.ipynb`
3. Click **Run All** (or run cells step-by-step).
4. You should see:
   - Bloch spheres (Bell)
   - Circuit diagrams (Bell & optimized VQE)
   - Bell histograms (clean & noisy)
   - VQE energy printout and heatmap

---

## 🗂️ Repo structure

```
quantum-experiments/
├─ exercises/
│  └─ vqe_demo/
│     └─ quantum_demo.ipynb     # All 6 exercises in one notebook
├─ requirements.txt
├─ .gitignore
└─ README.md
```

---

## 📸 Outputs you can reference in posts

- Bell histogram: only `00` and `11`
- VQE: `Minimum energy ≈ -2.0` and optimized circuit (two RY + CNOT)
- Energy heatmap (θ, φ) for H = ZI + IZ
- Noisy vs clean Bell comparison (depolarizing p=0.05)

> Tip: In VS Code Jupyter, use the image toolbar (save icon) to export figures for LinkedIn/README.

---

## 🔐 Notes for security & reproducibility

- Pin dependencies with `requirements.txt`.  
- Keep notebooks deterministic where possible (set seeds for simulators).  
- Document noise parameters when demonstrating attacks/robustness.

---

## 🤝 Attribution

This demo was generated and refined using **VS Code + OpenAI Codex integration**.  
Author: **Teppo (“RebelCoding84”)** · Repo: `quantum-experiments`
