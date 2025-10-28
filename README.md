# 🚀 QuantAIML

- This project implements a complete end-to-end AutoML framework without using AutoML libraries. Designed for production-style automation, it handles data processing, model selection, hyperparameter tuning, explainability, drift monitoring, and final reporting — all with zero manual tweaking.


# ✅ Key Capabilities :

| Stage                         | What It Does                                                        |
| ----------------------------- | ------------------------------------------------------------------- |
| **1️⃣ Dataset Handling**      | Type detection, missing value treatment, encoding, optional scaling |
| **2️⃣ Model Zoo**             | Random Forest, XGBoost, LightGBM, CatBoost                          |
| **3️⃣ Bayesian Optimization** | Optuna / Custom TPE with Stratified K-Fold CV                       |
| **4️⃣ Explainability**        | SHAP global + local insights, automatic plot export                 |
| **5️⃣ Drift Monitoring**      | PSI + KL Divergence detection for dataset health                    |
| **6️⃣ Reporting**             | Auto-generated PDF/HTML with results overview                       |

# 🧠 System Architecture

┌────────────────┐
│   Input Data    │
└───────┬────────┘
        ▼
┌───────────────────────┐
│ Auto Data Preprocessor │◄── Missing Value Handling
└───────┬───────────────┘
        ▼
┌──────────────────────┐
│   Model Zoo & Tuner   │─ RandomForest
│  (Bayesian Search)    │─ XGBoost
└───────┬──────────────┘─ LightGBM
        ▼                 └ CatBoost
┌──────────────────────┐
│ Best Model Selector  │
└───────┬──────────────┘
        ▼
┌──────────────────┐
│ SHAP Explainability│
└───────┬───────────┘
        ▼
┌──────────────────┐
│ Drift Monitoring │
└───────┬──────────┘
        ▼
┌────────────────────────────┐
│ Automated Final Report     │
└────────────────────────────┘

# 📊 Evaluation Metrics

- ROC-AUC / F1 Score (based on problem type)

- Stratified K-Fold CV mean performance

- Drift indicators: PSI & KL Divergence

# 🧩 Explainability

✅ SHAP summary plot

✅ 5 local prediction explanations

✅ Feature contribution ranking
