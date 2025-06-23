# Advanced DDoS Attack Detection in SDN Using Machine Learning

This repository presents the full dataset, trained models, result plots, and evaluation metrics for the Master’s thesis titled:

**"Advanced Detection and Prediction of DDoS Attacks in SDN Environments Using Cutting-Edge Machine Learning Techniques on Statistical Datasets"**  
by *Aram Saleem* – MSc in Computer Science, 2025.

---

## 📌 Overview

This project aims to enhance the detection and prediction of Distributed Denial of Service (DDoS) attacks within Software-Defined Networking (SDN) environments using advanced machine learning techniques. The work focuses on using statistical features extracted from network flows to classify traffic as normal or attack with high precision and reliability.

The dataset was collected from a real SDN environment using Mininet and Ryu, and several ensemble and baseline machine learning models were trained and tested on this dataset.

---

## 📊 Dataset Description

The dataset consists of real-time traffic flows labeled as either "Normal" or "DDoS Attack". It includes key statistical features such as:

| Feature | Description |
|--------|-------------|
| `flow_duration` | Duration of the network flow |
| `packet_rate`, `byte_rate` | Traffic volume metrics |
| `protocol`, `src_ip`, `dst_ip`, `src_port`, `dst_port` | Flow identifiers |
| `label` | Class label: 0 (Normal), 1 (Attack) |

The data was balanced and preprocessed before training the models.

---

## 🧠 Machine Learning Models Used

The following models were applied for classification:

- LightGBM
- XGBoost
- CatBoost
- Gradient Boosting Decision Trees (GBDT)
- AdaBoost
- Bagging
- One-Class SVM
- Bayesian Network

### Evaluation Metrics
All models were evaluated using:
- **Accuracy, Precision, Recall, F1-Score**
- **Area Under the Curve (AUC)**
- **Cohen's Kappa**, **Matthews Correlation Coefficient (MCC)**
- **False Positive Rate (FPR)**, **False Negative Rate (FNR)**
- **Cross-Validated Accuracy**

---

## 📈 Visual Results

The repository contains plots for visual evaluation of all models.

### 🔳 Confusion Matrices
Each classifier's confusion matrix shows the number of correct and incorrect classifications:

- `confusion_matrix_lightgbm.png`
- `confusion_matrix_xgboost.png`
- `confusion_matrix_catboost.png`
- `confusion_matrix_gbdt.png`
- `confusion_matrix_adaboost.png`
- `confusion_matrix_bagging.png`
- `confusion_matrix_ocsvm.png`
- `confusion_matrix_bayes.png`

### 📉 ROC Curves
Receiver Operating Characteristic (ROC) curves illustrate the trade-off between TPR and FPR:

- `roc_curve_lightgbm.png`
- `roc_curve_xgboost.png`
- `roc_curve_catboost.png`
- ... and more
- `roc_curve_all_models_comparison.png` — A combined ROC graph for all classifiers

---

## 🧪 Summary of Results

| Model | Accuracy | Precision | Recall | F1-Score | AUC | Kappa | MCC | FPR | FNR | Cross-Validated Accuracy |
|-------|----------|-----------|--------|----------|-----|--------|-----|-----|-----|---------------------------|
| LightGBM | 0.9998 | 0.9999 | 0.9996 | 0.9998 | 0.9999 | 0.9996 | 0.9996 | 0.0001 | 0.0004 | 0.9992 |
| XGBoost | 0.9989 | 0.9996 | 0.9983 | 0.9989 | 0.9999 | 0.9978 | 0.9978 | 0.0004 | 0.0017 | 0.9985 |
| CatBoost | 0.9993 | 0.9999 | 0.9987 | 0.9993 | 0.9999 | 0.9987 | 0.9987 | 0.0001 | 0.0013 | 0.9986 |
| GBDT | 0.9989 | 0.9991 | 0.9987 | 0.9989 | 0.9999 | 0.9978 | 0.9978 | 0.0009 | 0.0013 | 0.9993 |
| AdaBoost | 0.9987 | 0.9991 | 0.9983 | 0.9987 | 0.9999 | 0.9974 | 0.9974 | 0.0009 | 0.0017 | 0.9989 |
| Bagging | 0.9991 | 0.9996 | 0.9987 | 0.9991 | 0.9999 | 0.9982 | 0.9982 | 0.0004 | 0.0013 | 0.9992 |
| One-Class SVM | 0.9823 | 0.9794 | 0.9998 | 0.9895 | 0.9999 | 0.9322 | 0.9343 | 0.1077 | 0.0002 | 0.9505 |
| Bayesian Network | 0.9982 | 1.0000 | 0.9965 | 0.9983 | 0.9983 | 0.9965 | 0.9965 | 0.0000 | 0.0035 | 0.9984 |

---

## 📚 Citation

If you use this work or dataset, please cite:

