# Liver Cirrhosis Stage Prediction using Machine Learning

This repository contains a comprehensive Machine Learning project to predict the progression stages of Liver Cirrhosis based on clinical and laboratory data. 

## 📌 Project Overview
Liver Cirrhosis is a life-threatening condition where healthy liver tissue is replaced by scar tissue. This project analyzes a dataset containing several medical indicators (like Bilirubin, Albumin, Copper, etc.) to:
1. **Multi-class Classification:** Categorize patients into one of four stages (Stage 1, 2, 3, or 4).
2. **Binary Classification:** Predict if a patient is in a **Low Risk** (Stages 1-2) or **High Risk** (Stages 3-4) condition.

## 📊 Dataset Highlights
The dataset is sourced from the **Mayo Clinic Liver Cirrhosis Study**.
- **Samples:** 418 patients.
- **Key Features:** Age, Sex, Ascites, Hepatomegaly, Spiders, Edema, Bilirubin, Cholesterol, Albumin, Copper, Alk_Phos, SGOT, Tryglicerides, Platelets, Prothrombin.
- **Challenge:** The dataset was highly imbalanced with significant missing values.

## 🛠️ Technical Workflow

### 1. Data Preprocessing
- **Handling Missing Values:** Used `KNNImputer` to estimate missing clinical values based on the nearest neighbors.
- **Encoding:** Categorical variables (Sex, Drug, Spiders, etc.) were transformed using `LabelEncoder`.
- **Scaling:** Applied `StandardScaler` to normalize the range of independent variables.
- **Handling Imbalance:** Used **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the classes in the training set.

