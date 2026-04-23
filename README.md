# 🚀 ML Optimization of H₂ Production from Catalytic Methane Decomposition

This project focuses on predicting and optimizing hydrogen (H₂) production from the **Catalytic Decomposition of Methane (CDM)** using **Fe-based catalysts** through Machine Learning techniques.

---

## 📌 Overview

Hydrogen is a clean and high-energy fuel with growing industrial demand. Traditional production methods like **Steam Methane Reforming (SMR)** produce significant CO₂ emissions.

This project explores:

> ⚡ **Catalytic Decomposition of Methane (CDM)** → Produces H₂ + solid carbon (no direct CO₂)

Machine Learning is used to predict hydrogen yield and optimize process parameters efficiently.

---

## 🧪 Problem Statement

CDM performance depends on multiple interacting variables:
- Temperature
- Gas flow rate (GHSV)
- Catalyst composition
- Reaction time

Traditional optimization is:
- Time-consuming  
- Expensive  
- Inefficient for nonlinear systems  

👉 Solution: Use ML models for prediction and optimization.

---

## ⚙️ Methodology

### 1. Data Collection
- Extracted from multiple research papers
- Includes:
  - Textual data
  - Tabular data
  - Graphical data (via WebPlotDigitizer)

### 2. Data Preprocessing
Three-layer pipeline:
- **Basic Cleaning** → Missing values, formatting
- **Structural Cleaning** → Duplicates, outliers, unit conversion
- **Validation** → Scientific consistency

### 3. Features

#### Input Parameters:
- Reaction Temperature
- Calcination Temperature
- GHSV (Gas Hourly Space Velocity)
- Reaction Time
- CH₄ Concentration
- Catalyst composition (Fe wt%, Al₂O₃, promoters, etc.)

#### Output:
- 🎯 **H₂ Yield**

---

## 🤖 Machine Learning Models Used

- K-Nearest Neighbors (KNN)
- Random Forest Regressor
- XGBoost Regressor

### Training Pipeline:
1. Load dataset  
2. Define X and y  
3. Train-test split (80/20)  
4. Train models  
5. Predict on test data  
6. Evaluate performance  

---

## 📊 Key Results

### 🏆 Best Model:
- **Random Forest**
- **R² ≈ 0.9688**

### 🔍 Insights:
- **GHSV** → Most influential parameter (strong negative effect)
- **CH₄ Conversion ↔ H₂ Yield** → Strong positive correlation (~0.73)
- **Catalyst composition (Fe, Al₂O₃)** significantly impacts output
- Temperature shows limited impact beyond a threshold

---

## 📈 Model Interpretation

### Feature Importance:
Top features:
1. GHSV  
2. Al₂O₃ wt%  
3. Fe wt%  

### Partial Dependence:
- High GHSV → Low yield  
- Longer time → Catalyst deactivation  
- Excess Al₂O₃ (>60%) → Reduced activity  

---

## 📉 Visualizations

- Correlation Heatmap  
- True vs Predicted plots  
- Feature Importance graph  
- Partial Dependence plots  

---

## 💡 Key Takeaways

- ML effectively models nonlinear catalytic systems  
- Random Forest performs best  
- Optimization should focus on:
  - GHSV  
  - Catalyst composition  
  - Reaction time  

---

## 🔮 Future Work

- Predict CH₄ conversion  
- Model catalyst deactivation rate  
- Estimate coke deposition  
- Multi-output ML model:
  - H₂ yield  
  - Conversion  
  - Carbon formation  
- Predict carbon nanofiber (CNF) yield  

---

## 🛠️ Tech Stack

- Python  
- NumPy, Pandas  
- Matplotlib, Seaborn  
- Scikit-learn  
- XGBoost  

---

## 👨‍🔬 Authors

- Aditya Mani Tripathi  
- Anupam Singh  
- Tejas Ashri  
- Om Utkarsh  

Department of Chemical Engineering  
IIT (BHU), Varanasi  

---

## 📌 How to Run

```bash
# Clone repo
git clone https://github.com/propulse-7969/UGP-ML-x-Catalysis

# Install dependencies
pip install -r requirements.txt

# Run
python main.py
