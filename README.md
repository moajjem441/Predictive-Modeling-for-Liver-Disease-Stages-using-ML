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

### 2. Exploratory Data Analysis (EDA)
- Analyzed feature correlations using Heatmaps.
- Visualized the distribution of liver stages to identify class imbalance.

### 3. Model Implementation
I experimented with multiple algorithms to find the best fit:
- **Decision Tree Classifier**
- **Random Forest Classifier**
- **XGBoost Classifier**



## 📈 Performance Comparison

| Model | Classification Type | Accuracy |
| :--- | :--- | :--- |
| Decision Tree | Multi-class (1-4) | 47.62% |
| Random Forest (SMOTE) | Multi-class (1-4) | 48.81% |
| XGBoost | Multi-class (1-4) | 45.24% |
| **Random Forest (Binary)** | **Binary (Low/High Risk)** | **68.60%** |


### Key Insight:
While multi-class prediction is challenging due to the small dataset, the **Binary Classification** model is quite effective at identifying high-risk patients (Stages 3 & 4) with nearly **69% accuracy**.

## 🧬 Feature Importance
Based on the Random Forest model, the following features were most critical in determining the disease stage:
1. **Bilirubin**
2. **Copper**
3. **Albumin**
4. **Prothrombin Time**


## 🚀 How to Use

You can run this project either directly on Kaggle (recommended for ease of use) or locally on your machine.

### 1. Run on Kaggle (Easiest Way)
Since this project was developed on Kaggle, you can run it without any local setup:
* **Step 1:** Go to the [Kaggle Notebook](https://www.kaggle.com/code/your-username/your-notebook-slug). *(Replace with your actual link)*
* **Step 2:** Click on the **"Copy and Edit"** button.
* **Step 3:** Ensure the `cirrhosis.csv` dataset is attached in the input directory.
* **Step 4:** Run all cells to see the data processing, visualizations, and model results.

### 2. Run Locally
If you prefer to run it on your own computer, follow these steps:

**A. Clone the Repository:**
```bash
git clone [https://github.com/moajjem441/Predictive-Modeling-for-Liver-Disease-Stages-using-ML.git](https://github.com/moajjem441/Predictive-Modeling-for-Liver-Disease-Stages-using-ML.git)
cd Predictive-Modeling-for-Liver-Disease-Stages-using-ML

B. Install Required Libraries:

Bash
pip install -r requirements.txt
C. Launch the Notebook:
Open your terminal and run:

Bash
jupyter notebook
Then, open the .ipynb file from the dashboard.
