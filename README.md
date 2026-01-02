# Breast Cancer Classification — Model Comparison

This project applies classical machine learning models to the Wisconsin Breast Cancer dataset
to classify tumors as **malignant** or **benign**. The goal is not only to achieve high accuracy,
but also to understand model behavior using appropriate evaluation metrics and decision
threshold analysis.

---

## 📌 Project Objectives

- Build a reliable baseline classifier for breast cancer detection
- Compare multiple machine learning models under identical conditions
- Evaluate models using metrics beyond accuracy
- Analyze decision thresholds and recall–precision trade-offs in a medical context

---

## 🧠 Models Used

The following models were implemented and compared:

- **Logistic Regression** (baseline, interpretable)
- **Support Vector Machine (RBF kernel)**
- **Random Forest Classifier**

All applicable models were implemented using **scikit-learn Pipelines** to ensure
proper preprocessing and to prevent data leakage.

---

## 📊 Dataset

- **Source:** Wisconsin Breast Cancer Dataset (via `sklearn.datasets`)
- **Samples:** 569
- **Features:** 30 numerical features
- **Classes:**
  - `0` → Malignant
  - `1` → Benign

The dataset was split into training and test sets using stratified sampling.

---

## ⚙️ Preprocessing

- Feature scaling performed using **StandardScaler**
- Scaling applied only to training data via Pipelines
- Tree-based models were trained without scaling

---

## 📈 Evaluation Metrics

Models were evaluated using:

- Accuracy
- Confusion Matrix
- Precision, Recall, F1-score
- ROC Curve and ROC–AUC
- Precision–Recall Curve
- Decision threshold analysis

Special emphasis was placed on **recall**, as false negatives (missed cancer cases)
are particularly costly in medical screening scenarios.

---

## 🔎 Decision Threshold Analysis

Instead of relying solely on the default probability threshold (0.5), the project explores
how changing the decision threshold affects recall and precision. Lower thresholds were
examined to prioritize sensitivity in detecting malignant cases.

ROC and Precision–Recall curves were used to visualize model performance across all thresholds.

---

## 📋 Model Comparison Summary

Multiple classifiers were evaluated under the same train–test split and metrics.
Results show that while more complex models achieve comparable performance, Logistic Regression
offers strong performance with greater interpretability, which is often preferred in
medical decision-support systems.

(Detailed results are available in the notebook.)

---

## 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- scikit-learn
- Matplotlib
- Jupyter Notebook

---

## ▶️ How to Run

1. Clone the repository
2. Create and activate a virtual environment
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
