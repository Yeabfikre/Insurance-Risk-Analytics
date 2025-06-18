# 📊 Insurance Risk Analytics

Welcome to the **Insurance Risk Analytics** project — a complete analytics and modeling pipeline for AlphaCare Insurance Solutions, South Africa. This project explores customer policy and claims data to extract actionable insights and build predictive models to better understand **risk**, **loss ratios**, and **claim severity** across different regions and demographics.

---

## 🔍 Project Objectives

- **Exploratory Data Analysis (EDA):** Understand key metrics such as Loss Ratio, Claim Frequency, and Margin.
- **Versioning:** Use Git and DVC for reproducible workflows and data versioning.
- **Hypothesis Testing:** Evaluate statistical significance of claim patterns across provinces, genders, and other segments.
- **Predictive Modeling:** Build models to predict claim severity using ML algorithms and interpret results using SHAP.

---

## 🗂️ Repository Structure
```
insurance-risk-analytics/
├── data/
│ ├── raw/ # Original data (CSV files)
│ └── processed/ # Cleaned data for analysis/modeling
├── notebooks/ # Jupyter notebooks (optional)
├── plots/ # Generated visualizations
├── src/
│ ├── task1_eda.py # EDA and visualizations
│ ├── task2_dvc.py # DVC data management
│ ├── task3_hypothesis.py # Hypothesis testing and inference
│ ├── task4_modeling.py # ML training & SHAP interpretation
├── dvc.yaml # DVC pipeline definitions
├── .dvc/ # DVC cache and metadata
├── .gitignore
├── README.md # Project overview
└── requirements.txt # Python dependencies
```
---


---

## 🧪 Key Metrics

- **Loss Ratio:** `TotalClaims / TotalPremium`
- **Claim Frequency:** % of policies with at least one claim
- **Claim Severity:** Average claim amount (for claim-positive cases)
- **Margin:** `TotalPremium - TotalClaims` per policy

---

## 📈 Sample Insights (from EDA & Hypothesis Testing)

- Claim frequency varies significantly by **province** (p < 0.05).
- **Males** and **females** have different claim rates in some regions.
- Policies with higher `CustomValueEstimate` tend to have larger claims.
- Certain **vehicle types** are associated with higher loss ratios.

---

## 🤖 Models & Performance
```
| Model          | RMSE    | R² Score |
|----------------|---------|----------|
| LinearRegression | 287.13 | 0.56     |
| RandomForest    | 195.77 | 0.81     |
| XGBoost         | 189.34 | 0.83     |
```
📌 *SHAP analysis* reveals `VehicleType`, `CustomValueEstimate`, and `Province` are top contributors to claim severity.

---

## ⚙️ How to Run This Project

### ✅ Prerequisites

- Python 3.9+
- pip
- Git & DVC installed

### 🔧 Installation

```bash
# Clone repo
git clone https://github.com/Yeabfikre/Insurance-Risk-Analytics.git
cd Insurance-Risk-Analytics

# Create environment
python -m venv env
source env/bin/activate  # or .\env\Scripts\activate (Windows)
pip install -r requirements.txt
```
---
## 📂 Setup DVC
```
dvc pull  # Pull data from remote
```
## 🚀 Run Tasks
```
python src/task1_eda.py
python src/task3_hypothesis.py
python src/task4_modeling.py
```


