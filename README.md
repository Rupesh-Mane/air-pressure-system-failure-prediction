# 🚛 Detecting Air Pressure System Failure in Trucks

<div align="center">

<img src="assets/APS_Truck_banner.png" width="900">


</div>

---
## 📌 Project Overview

This project uses **Machine Learning to predict Air Pressure System (APS) component failures in heavy trucks**.

The dataset contains real-world truck sensor data with **missing values and a highly imbalanced target class**. The project covers the complete ML workflow — from data analysis and preprocessing to **SMOTE, model training, evaluation, and hyperparameter tuning**.

After comparing multiple classification models, **XGBoost** was selected as the final model and achieved:

**99.35% Accuracy | 84.73% Recall | 82.48% F1 Score | 99.28% ROC-AUC**

---

## 🎯 Motivation

I wanted to work on a real-world machine learning problem where the data is not perfectly clean and the model needs to handle practical challenges. The Air Pressure System is an important part of heavy trucks, especially for functions such as braking and gear changes.

While working on this project, I wanted to understand how machine learning can be applied to sensor data to identify possible component failures. The dataset also contains many missing values and a highly imbalanced target, which motivated me to learn how to handle these challenges properly instead of working only with simple, clean datasets.

This project helped me connect the concepts I learned in machine learning with a practical engineering problem and increased my interest in applying **AI and machine learning to real-world systems**.

---

## 🎯 Objective

My main objective in this project was to build a machine learning model that could predict whether an Air Pressure System (APS) component in a heavy truck could fail.

I wanted to understand the complete machine learning process, starting from **data preprocessing and handling missing values**, to dealing with the **imbalanced dataset**, training different classification models, and evaluating their performance.

I also wanted to compare different models and use **hyperparameter tuning** to improve the final model's performance. Through this project, my goal was not only to achieve good accuracy, but also to understand how machine learning can be applied to a real-world failure prediction problem.

---

## 📊 Dataset

The dataset used in this project is:

**APS Failure at Scania Trucks**

The dataset was obtained from the **UCI Machine Learning Repository**.

🔗 **Dataset:**  
https://archive.ics.uci.edu/ml/datasets/aps+failure+at+scania+trucks

### 📋 Dataset Information

<table>
<tr>
<th>📌 Information</th>
<th>📊 Details</th>
</tr>

<tr>
<td><b>Dataset</b></td>
<td>APS Failure at Scania Trucks</td>
</tr>

<tr>
<td><b>Source</b></td>
<td>UCI Machine Learning Repository</td>
</tr>

<tr>
<td><b>Problem Type</b></td>
<td>Binary Classification</td>
</tr>

<tr>
<td><b>Training Instances</b></td>
<td>60,000</td>
</tr>

<tr>
<td><b>Test Instances</b></td>
<td>16,000</td>
</tr>

<tr>
<td><b>Attributes</b></td>
<td>171</td>
</tr>

<tr>
<td><b>Feature Type</b></td>
<td>Integer and Real</td>
</tr>

<tr>
<td><b>Missing Values</b></td>
<td>Yes</td>
</tr>

<tr>
<td><b>Target</b></td>
<td><code>class</code></td>
</tr>

</table>

The positive class represents component failures for a specific component of the APS, while the negative class represents trucks with failures not related to the APS.

### 📚 Dataset Citation

> APS Failure at Scania Trucks [Dataset]. (2016). UCI Machine Learning Repository.

**DOI:** 10.24432/C51S51

---
## 🔄 Project Workflow

🚛 Raw Dataset
       ↓
🔍 Data Understanding
       ↓
📊 EDA
       ↓
🧹 Data Preprocessing
       ↓
⚖️ SMOTE
       ↓
🤖 Model Training
       ↓
📈 Model Evaluation
       ↓
⚙️ Hyperparameter Tuning
       ↓
🏆 Final XGBoost Model
       

---

## 🧹 Data Preprocessing

Before training the models, I prepared the dataset step by step to make it suitable for machine learning.

<div align="center">

| 🔧 Step | 📝 What I Did |
|---|---|
| 🧹 **Missing Values** | Handled missing values using **mean imputation** |
| ✂️ **Train / Test Split** | Prepared separate training and testing datasets |
| 📏 **Feature Scaling** | Scaled the numerical features to bring them to a similar range |
| ⚖️ **Class Imbalance** | Used **SMOTE** to balance the minority and majority classes in the training data |
| 📦 **Processed Dataset** | Created the final processed training and testing datasets for model training |

</div>

### ⚖️ Handling Class Imbalance

The dataset contains considerably fewer failure cases than non-failure cases.  
To address this problem, I used **SMOTE (Synthetic Minority Oversampling Technique)** on the training data.

```text
Original Training Data
        ↓
   Class Imbalance
        ↓
      SMOTE
        ↓
Balanced Training Data
        ↓
   Model Training

---