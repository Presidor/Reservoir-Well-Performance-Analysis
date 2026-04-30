# 📊 Reservoir & Well Performance Analysis (DSEATS Africa 2025)

## 📌 Overview
This project presents a **comprehensive analysis of oil and gas well performance** using a combination of **data science techniques and petroleum engineering principles**.

The workflow integrates:
- Data cleaning and preprocessing
- Engineering-based feature extraction
- Exploratory data analysis (EDA)
- Machine learning (supervised & unsupervised)

---

## 🎯 Objectives
- Identify the **reservoir for each well**
- Classify reservoirs as **Saturated or Undersaturated**
- Determine **flow mechanism** (Natural Flow vs Gas Lift)
- Analyze **production stability**
- Extract meaningful insights from well production data

---

## 📁 Dataset
- **Total Records:** 7,955  
- **Wells:** 20  
- **Key Features:**
  - Bottom-hole pressure (BHP)
  - Wellhead pressure & temperature
  - Choke size
  - Cumulative oil, gas, and water production
  - On-stream hours

---

## ⚙️ Workflow

### 1. Data Cleaning & Preprocessing
- Renamed columns for consistency
- Converted date column to datetime format
- Removed commas from numeric columns
- Converted object types to float
- Verified:
  - ✅ No missing values  
  - ✅ No duplicates  
  - ✅ Consistent well identifiers  

---

### 2. Feature Engineering (Domain-Based)

#### Reservoir Identification
- Based on:
  - Maximum bottom-hole pressure
  - Reservoir pressure constraints (≤ 200 psi differential)

#### Reservoir Type Classification
- **Saturated:** Initial Pressure ≤ Bubble Point  
- **Undersaturated:** Initial Pressure > Bubble Point  

#### Flow Mechanism
- **Natural Flow:** Formation Gas = Total Gas  
- **Gas Lift:** Otherwise  

#### Production Rates
- Derived from cumulative values using differencing

---

### 3. Well Performance Analysis

#### Production Stability
- Wells classified as:
  - **Unsteady** → >50% oil drop within 3–6 months  
  - **Steady** → otherwise  

#### Gas-Oil Ratio (GOR)
- Computed and compared with solution GOR

#### Water Cut Trends
- Evaluated water production behavior over time

---

### 4. Exploratory Data Analysis (EDA)
- Time-series analysis across wells
- Pressure and production comparisons
- Distribution plots and correlation analysis

---

### 5. Machine Learning

#### Supervised Learning
Models used:
- Random Forest
- Gradient Boosting
- XGBoost

Applications:
- Reservoir classification
- Well behavior prediction

#### Unsupervised Learning
- K-Means Clustering
- PCA (Dimensionality Reduction)

Goal:
- Identify hidden patterns across wells

---

## 🧠 Key Insights
- Average reservoir pressure improves classification accuracy
- Both **natural flowing** and **gas-lifted wells** exist
- Production instability is common across several wells
- GOR is relatively consistent within reservoirs

---

## 🛠️ Tech Stack
- **Python**
- **Pandas, NumPy**
- **Matplotlib, Seaborn**
- **Scikit-learn**
- **XGBoost**

---
