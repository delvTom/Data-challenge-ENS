# 🧪 Data Challenge 2025 — Gas Detection  
**Sorbonne University – M2 MS2A (Mathematics, Statistics and Learning)**  
**Organizers:** ENS Paris-Saclay × Bertin Technologies  

---

## 🎯 Project Overview

This project was carried out as part of the **Data Challenge 2025**.  
The goal was to **predict the concentration of 23 gases simultaneously** using multivariate sensor measurements.  

A major difficulty was the **data distribution shift** between the training and test sets — mainly due to the *Humidity* variable — as the test data represented physical conditions rarely observed in training.  
The evaluation metric was a **Weighted RMSE**, which penalized larger errors more strongly for higher concentration values.

---

## 🧠 Summary of the Approach

The final solution is based on an **ensemble of Extra Trees Regressors**, combined through a **weighted blending** strategy, followed by **linear calibration** and **shrinkage toward the training mean**.  
Row-wise statistical features (mean, std, IQR, MAD, etc.) played a key role in improving robustness under distribution shift.  

- **Public score:** 0.1400  
- **Private score:** 0.1520  

---

## 📂 Repository Structure

Data-Challenge-MS2A-2025/
│
├── DataChallenge_2025_Notebook_Final.ipynb # Main notebook (EDA → preprocessing → modeling → submission)
├── figures/ # EDA plots (shift, target distribution, etc.)
├── report/ # Final report (2-page academic summary)
├── submission_ET_BLEND_v1.csv # Final submission file
└── README.md # Project description

---

## 🧾 Report & Reproducibility

The complete report is available in [`report/Rapport_DataChallenge_2025.pdf`](report/Rapport_DataChallenge_2025.pdf),  
and the final notebook allows full reproduction of the pipeline and submission.

---

## 👤 Author

**Tom DE OLIVEIRA**  
M2 MS2A – Sorbonne University  
📧 [Add your professional email or LinkedIn profile here]

---

