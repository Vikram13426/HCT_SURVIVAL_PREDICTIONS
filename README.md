 FTTransformer for Event-Free Survival Prediction in HSCT Patients

This project applies the **FTTransformer** model to predict **event-free survival** in patients undergoing **allogeneic Hematopoietic Stem Cell Transplantation (HSCT)**, using data from the **CIBMTR** dataset. It aims to produce accurate, fair, and interpretable predictions across different racial and demographic groups.

---

🧠 Objective

- Predict **event-free survival time** for post-HSCT patients using tabular clinical and demographic data.
- Train a **fair model** that performs well across different racial/ethnic groups.
- Use **FTTransformer**, a transformer-based architecture designed for tabular data.

---
🛠️ Features

- Uses **FTTransformer** (TabTransformer + Feature Tokenization)
- Handles **categorical** and **numerical** inputs with proper preprocessing
- Uses **Cox proportional hazards loss** for survival modeling
- Includes fairness visualizations (e.g., Kaplan-Meier by race)
- Implements **early stopping** and **learning rate scheduling**

---

 
---

## 🧬 Dataset

- **Source**: CIBMTR dataset (modified for event-free survival analysis)
- **Size**: ~13,000 patients
- **Target Variables**:
  - `event_time`: Time to event or censoring
  - `event_indicator`: 1 = Event occurred; 0 = Censored
- **Features**:
  - Categorical: race, donor_type, disease_type, etc.
  - Numerical: age, graft_type, BMI, WBC counts, etc.

---

## 🔄 Preprocessing

- Missing value imputation
- One-hot or label encoding for categorical variables
- Standard scaling for numerical variables
- Train-test split with stratification by race

---

## 🤖 Model

**FTTransformer** is used with:
- Depth: 6
- Heads: 8
- Dimension: 64
- Dropout: 0.4
- Final linear layer to output risk scores

Loss function: **Cox partial likelihood** (negative log-likelihood)

---


