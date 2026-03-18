# Fetal Health Diagnosis using Machine Learning and Deep Learning

## 📌 Project Overview

This project focuses on **Fetal Health Diagnosis using Cardiotocography (CTG) data** by applying Machine Learning, Feature Selection, and Deep Learning techniques.
The goal is to build a predictive system that can classify pregnancy conditions based on fetal heart rate signals and related features, and to demonstrate the results through performance metrics, graphs, and a simple front-end interface.

The project was developed as part of an **M.Sc. Computer Science final year project**, with emphasis on program implementation, model comparison, and performance improvement using feature selection and signal segmentation.

---

## 📌 What is Cardiotocography (CTG)?

Cardiotocography (CTG) is a **non-invasive monitoring technique** used during pregnancy to record:

* Fetal Heart Rate (FHR)
* Uterine Contractions
* Accelerations and Decelerations
* Variability patterns

These signals help doctors determine whether the fetus is:

* Normal
* Suspicious
* Pathological

This project uses CTG data to train machine learning and deep learning models to automatically predict fetal health condition.

---

## 📌 Dataset Used

Dataset used in this project:

* CTU-CHB Cardiotocography Dataset and High Risk Pregnancy Datset : https://physionet.org/content/ctu-uhb-ctgdb/1.0.0/
* Contains multiple patient recordings and their physiological data
* Each patient has signal data stored in `.hea` / signal files
* Signals are long time-series recordings (~17500 samples)

### Preprocessing Steps

* Extract signal information from `.hea` files
* Convert to structured format (CSV)
* Segment long signals into smaller windows
* Label each segment using class labels
* Handle class imbalance using oversampling

---

## 📌 Signal Segmentation Strategy

Each signal is very long, so segmentation was required.

* Original signal length ≈ 17500 samples
* Each signal split into **14 segments**
* Each segment length = 1200 samples (≈20 minutes)
* Total segments generated = 7728

Class distribution before oversampling:

| Class   | Count |
| ------- | ----- |
| Class 0 | 1463  |
| Class 1 | 6143  |

Oversampling applied to balance classes before training.

Segmentation helped because:

* CNN requires large dataset
* More samples → better learning
* Improves generalization

---

## 📌 Feature Selection

Feature selection was used to improve model performance.

Technique used:

* Mutual Information
* Recursive Random Forest

Steps:

1. Extract all features
2. Compute feature importance
3. Select top features
4. Train model on selected features
5. Compare accuracy before and after feature selection


## 📌 Models Used

### Machine Learning Models

* ANN

### Deep Learning Model

* 1D-CNN + BiGRU


## 📌 Notes

This project is for academic and research purposes.

