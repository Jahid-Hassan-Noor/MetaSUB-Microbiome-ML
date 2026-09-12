# MetaSUB-Microbiome-ML

# CAMDA 2023 MetaSUB Microbiome ML Classification

An end-to-end Machine Learning pipeline to predict city origins based on microbial relative abundance features using the **CAMDA 2023 MetaSUB** dataset.

## 📌 Key Highlights
* **Task:** Multi-class classification of urban microbiome relative abundance features (`City`).
* **Best Performing Model:** **XGBoost** achieving **~91.07% Accuracy** and **~89.60% Macro F1-Score** on holdout test data.
* **Feature Processing:** Filtered rare/constant microbial features, applied log-transformation (`log1p`), and selected top features via ANOVA F-value (`SelectKBest`).
* **Validation:** Robust 5-fold Stratified Cross-Validation to evaluate model generalization across class-imbalanced datasets.

---

## 📊 Experimental Results (5-Fold Cross-Validation)

| Model | Accuracy (Mean ± Std) | Macro F1 (Mean ± Std) | Macro Precision | Macro Recall |
| :--- | :---: | :---: | :---: | :---: |
| **XGBoost** | **0.8857 ± 0.043** | **0.8741 ± 0.058** | **0.9074** | **0.8705** |
| Logistic Regression | 0.8286 ± 0.058 | 0.8167 ± 0.078 | 0.8488 | 0.8239 |
| Random Forest | 0.8071 ± 0.071 | 0.7940 ± 0.076 | 0.8378 | 0.7983 |
| Linear SVM | 0.7643 ± 0.038 | 0.7410 ± 0.046 | 0.7926 | 0.7463 |

---


