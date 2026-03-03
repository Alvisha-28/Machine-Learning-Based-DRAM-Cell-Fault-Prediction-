# 🧠 Machine Learning-Based DRAM Cell Fault Prediction

## 📌 Project Overview

As DRAM technology scales, memory cells become increasingly vulnerable to reliability issues such as charge leakage, retention failures, voltage instability, and access-induced stress. Traditional threshold-based fault detection methods fail to capture the nonlinear and multi-parameter nature of DRAM failures.

This project proposes a Machine Learning-based predictive model to estimate DRAM cell fault probability using operational parameters.

---

## 🎯 Objective

To build a supervised Machine Learning model that predicts DRAM cell faults based on:

- Temperature
- Voltage
- Access Frequency
- Refresh Rate
- Retention Time

Output:
- 0 → Healthy Cell
- 1 → Faulty Cell

---

## 🧱 DRAM Cell Background

A DRAM cell consists of:

- 1 Transistor
- 1 Capacitor (1T–1C structure)

The capacitor stores electrical charge representing data. Over time, this charge leaks and must be refreshed periodically.

### Causes of DRAM Failure

- High temperature → Increased leakage
- Low voltage → Weak charge storage
- High access frequency → Transistor stress
- Low retention time → Faster data decay

When charge drops below a safe threshold, a bit flip occurs, leading to memory fault.

---

## 🏗 System Architecture

DRAM Parameters  
↓  
Synthetic Dataset Generation  
↓  
Data Preprocessing  
↓  
Machine Learning Model Training  
↓  
Model Evaluation  
↓  
Fault Probability Prediction  

---

## 📊 Dataset Description

Since real DRAM failure datasets are proprietary, a synthetic dataset was generated using DRAM physical failure conditions.

### Features

- temperature (°C)
- voltage (V)
- access_frequency
- refresh_rate
- retention_time

### Target

- fault = 0 → Healthy
- fault = 1 → Faulty

---

## 🤖 Machine Learning Model

Primary Model Used:

Random Forest Classifier

Reasons:
- Handles nonlinear relationships
- Captures interaction between multiple parameters
- Robust against overfitting
- Suitable for hardware reliability modeling

---

## 📈 Evaluation Metrics

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Special focus was given to Recall, as missing a DRAM fault can lead to data corruption.

---

## 📊 Feature Importance

Feature importance analysis identifies which parameters most influence DRAM faults.

Common dominant features:
- Temperature
- Retention Time
- Voltage

---

## 📁 Project Structure

DRAM-Fault-Prediction/
│
├── dram_fault_dataset.csv
├── dram_fault_prediction.ipynb
├── README.md
└── results/

---

## 🎓 Results

## 📊 Feature Importance

![Feature Importance](images/feature_importance(1).png)

- High classification accuracy achieved
- Random Forest effectively modeled nonlinear DRAM behavior
- ML approach outperformed static threshold-based logic
- Fault probability prediction enables proactive memory reliability management

---

## 🔮 Future Work

- Compare with SVM and XGBoost
- Add ROC curve analysis
- Hyperparameter tuning
- Cross-validation
- Time-series degradation modeling
- Integration with DRAM simulators

---

## 🛠 Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

## 📌 Applications

- Memory reliability prediction
- Data center fault prevention
- Embedded system memory management
- Semiconductor reliability modeling

---

