# Data Challenge 2025 — Gas Detection  
**Sorbonne University – M2 MS2A (Mathematics, Statistics and Learning)**  
**Organizers:** Bertin Technologies  

---

## Project Overview

This project was carried out as part of the **Data Challenge 2025**.  
The goal was to **predict the concentration of 23 gases simultaneously** using multivariate sensor measurements.  

A major challenge was the **data distribution shift** between the training and test sets as the test data represented physical conditions rarely observed in training.  
The evaluation metric was a **Weighted RMSE**, which penalized larger errors more strongly for higher concentration values.

---

## Summary of the Approach

The final solution is based on an **ensemble of Extra Trees Regressors**, combined through a **weighted blending** strategy, followed by **linear calibration** and **shrinkage toward the training mean**.  
Row-wise statistical features (mean, std, IQR, MAD, etc.) played a key role in improving robustness under distribution shift.  

- **Public score:** 0.1400  
- **Private score:** 0.1395  

---

## Repository Structure

**Main files and directories:**
- `01_EDA.ipynb / 02_Final_model.ipynb` — Complete notebook (EDA → preprocessing → modeling → submission)  
- `report/` — Final 2-page academic report in PDF format  
- `README.md` — Project documentation  

---

## Report & Reproducibility

The complete report is available in [`report/Rapport_DataChallenge_2025.pdf`](report/report_ms2a_2025.pdf),  
and the final notebook allows full reproduction of the pipeline and submission.


![Python](https://img.shields.io/badge/Python-3.10-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Finished-brightgreen)
