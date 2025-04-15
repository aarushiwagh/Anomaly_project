# Anomaly_project — Attack Detection in Multi-Tenant Cloud Systems

A machine learning pipeline for detecting malicious tenants in multi-tenant distributed systems using ensemble-based meta-classification and custom data balancing techniques.

> This project is based on our research paper published in the *International Journal on Recent and Innovation Trends in Computing and Communication (IJRITCC), Vol. 11, Issue 9, 2023.*

## Abstract

Cloud-based multi-tenant systems, while efficient and scalable, are prone to vulnerabilities due to shared infrastructure. This project proposes a **weighted ensemble learning approach** to predict attacks from tenants by analyzing system parameter patterns. It addresses challenges like **dataset scarcity**, **feature redundancy**, and **class imbalance** by:
- Generating a custom dataset with over **50,000 timeframes**
- Applying **oversampling and undersampling** for class balancing
- Training multiple classifiers and combining them via **weighted averaging**

---

## Key Features

- Custom cloud-attack dataset generation via virtualized environment
- Handling class imbalance using RandomOverSampler and RandomUnderSampler
- Feature selection to reduce dimensionality and prevent overfitting
- Models used: Decision Tree, Random Forest, SVM, Naive Bayes, Multi-layer Perceptron (ANN)
- Final prediction via **weighted average ensemble**
- Evaluation via Accuracy, Precision, Recall, and F1 Score

---

## Dataset

The dataset includes over **55,000 labeled entries** with key features:
- `app_cpu_netdata_x`
- `app_cpu_apps.plugin_x`
- `app_cpu_tc-qos-helper_x`
- `app_cpu_ssh_x`
- `running`, `freeused`, `cached`, `buffers`

Class labels:
- `0`: Normal tenant
- `1`: Malicious tenant (attack instance)

Balancing Strategy:
- Oversampled minority class using `RandomOverSampler`
- Undersampled majority class using `RandomUnderSampler`
- Achieved final ratio: ~1.25:1 (non-attack:attack)

---

## Results

Model | Accuracy | Precision | Recall | F1 Score
Decision Tree | 99.64% | 0.909 | 0.667 | 0.769
Naive Bayes | 91.05% | 0.846 | 0.733 | 0.785
SVM | 99.60% | 0.900 | 0.750 | 0.810
ANN | 99.60% | 0.900 | 0.750 | 0.810
Random Forest | 99.92% | 0.916 | 0.733 | 0.814
Ensemble | 99.14% | 0.911 | 0.753 | 0.819

## Citation

If you use this code or dataset in your research, please cite:

> Patil, P., Kale, G., Chandwani, M., & Wagh, A. (2023). _Boosting Attack Detection Capabilities in Multi-Tenant Distributed Systems via Meta-Ensemble Classifiers and Weighted Averaging_. IJRITCC, Vol. 11, Issue 9. [Read Paper]([http://www.ijritcc.org/download/Boosting-Attack-Detection-Capabilities-in-Multi-Tenant-Distributed-Systems-via-Meta-Ensemble-Classifiers-and-Weighted-Averaging.pdf](https://ijritcc.org/index.php/ijritcc/article/view/8994))

