# MSEM-PE6012-IKEA-SCM-Analyse
# 📦 AI-Driven Supply Chain Optimization for IKEA

## 📍 Project Overview

This project focuses on improving supply chain decision-making for IKEA using a data-driven analytics pipeline.  

We integrate:

- 📊 Descriptive Analytics (EDA + Geo Visualization)  
- 🤖 Predictive Analytics (Demand Forecasting)  
- ⚙️ Prescriptive Analytics (Constrained Optimization)  

to transform raw data into actionable inventory allocation decisions.

---

## 🎯 Problem Statement

Supply chain management faces several key challenges:

- Demand varies significantly across product categories and regions  
- Inventory resources are limited  
- Uniform allocation leads to inefficiencies and service loss  

👉 This project aims to:

**Forecast demand at the category level and optimize inventory allocation under real-world constraints.**

---

## 🗂 Dataset

The dataset is a simulated IKEA supply chain dataset (Europe–MENA sample).

### 📌 Key Features

- Sales data (`units_sold`)  
- Product information (`category`, `SKU`)  
- Pricing and promotion  
- Inventory levels  
- Store-level geographic information  

### 📊 Summary

- ~1000 rows  
- 14 columns  
- Multi-dimensional supply chain data  

👉 This dataset enables both demand modeling and operational optimization.

---

## 🔍 Methodology

We follow a complete Data Analytics Pipeline:

EDA & Geo Analysis  
↓  
Weekly Category Demand Forecasting  
↓  
Model Comparison & Stacking  
↓  
Constrained Inventory Optimization  

---

## 📊 Exploratory Data Analysis

We perform:

- Category-level demand analysis  
- Temporal trend analysis (weekly aggregation)  
- Geographic visualization of store performance  

### 🔑 Key Observations

- Demand is uneven across categories  
- Geographic demand is concentrated (Mediterranean region)  
- Promotion has limited impact on demand variation  

---

## 🤖 Demand Forecasting

### 🎯 Target

- Weekly category-level demand (`units_sold`)

---

### 🧠 Feature Engineering

We construct time-aware features:

- Lag features (historical demand)  
- Rolling statistics (trend smoothing)  
- Calendar features (seasonality)  
- Cyclical features (weekly/monthly patterns)  
- Interaction and momentum features  

---

### ⚙️ Models Used

- Ridge Regression  
- Random Forest  
- Extra Trees  
- XGBoost  
- LightGBM  

---

### 🔗 Stacking Model (Ridge Meta-Learner)

We combine multiple base models using stacking:

Base Models → Predictions → Ridge Meta-Learner → Final Output  

This improves model robustness and stability.

---

## 📈 Model Performance

- Tree-based models outperform linear models  
- Stacking improves prediction consistency  
- Predictions capture overall trends but smooth extreme values  

### 📊 Observations

- Typical prediction error:
  - ~5–10 units (stable categories)  
  - ~15–25 units (volatile categories)  

👉 Predictive power is moderate but sufficient for decision support.

---

## ⚙️ Constrained Optimization

We formulate an inventory allocation problem:

### 🎯 Objective

Minimize total cost:

Total Cost = Holding Cost + Shortage Cost  

---

### 🔒 Constraints

- Total inventory capacity (~92% of predicted demand)  
- Minimum service level (~70%)  
- Maximum allocation bounds  

---

### 📊 Results

- High-demand categories are prioritized  
- Low-demand categories are reduced (~10–30%)  
- Most categories maintain service levels above 70%  

👉 Optimization balances efficiency and service level.

---

## 💡 Key Takeaways

- Demand is uneven across categories and regions  
- Weekly aggregation improves predictability  
- Model performs well on trends but not extreme spikes  
- Optimization significantly improves resource allocation  
- The main value lies in linking forecasting with decision-making  

---

## 🚀 Conclusion

Combining demand forecasting with constrained optimization enables more efficient and practical supply chain decisions.

---

## 🛠 Tech Stack

- Python (Pandas, NumPy)  
- Scikit-learn  
- XGBoost / LightGBM  
- Matplotlib / Seaborn  
- Optimization (SciPy / Linear Programming)

---

## 📁 Project Structure

---

## 📌 Future Improvements

- Incorporate external data (weather, holidays)  
- Improve time-series modeling (hierarchical forecasting)  
- Extend optimization to multi-echelon supply chain  
