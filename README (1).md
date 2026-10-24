# 🏥 Healthcare Fraud Detection

Detecting potentially fraudulent healthcare providers from Medicare billing data by identifying abnormal billing patterns.

---

## 📌 Objective

Flag high-risk providers for further investigation by finding those whose submitted charges are unusually high compared to standardized Medicare amounts.

## ❓ Problem Statement

Fraudulent billing is a major concern in the healthcare industry. This project identifies providers who submit **unusually high charges** relative to **standardized Medicare amounts**, so that investigators can prioritize the most suspicious cases.

## 🛠 Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Data handling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine learning | Scikit-learn |

## 📊 Dataset

- **Size:** 100,000 healthcare provider records
- **Contents:** Provider details, service counts, and Medicare billing information

**Key columns used**

| Column | Description |
|---|---|
| `Average Submitted Charge Amount` | Average amount the provider charged |
| `Average Medicare Standardized Amount` | Standardized Medicare payment amount |
| `Number of Services` | Count of services billed |
| `Gender` | Provider gender |
| `Provider Type` | Provider specialty / category |

## 🧹 Data Cleaning

- Filled missing `Gender` values with `"Unknown"`
- Converted numeric columns stored as objects to `float`
- Removed infinite values from `Std_Charge_Ratio`
- Created the target variable `Fraud_Flag_Std`

## 📈 Exploratory Data Analysis

- Visualized fraud vs. non-fraud distribution
- Analyzed fraud ratio by **provider type** and **gender**
- Generated a correlation heatmap of numeric features

## 🚀 Getting Started

```bash
# Clone the repository
git clone <your-repo-url>
cd healthcare-fraud-detection

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# Launch the notebook
jupyter notebook
```

## 📁 Project Structure

```
healthcare-fraud-detection/
├── data/            # Medicare billing dataset
├── notebooks/       # Analysis and modeling notebooks
└── README.md
```

## 🔮 Next Steps

- Train and evaluate classification models using Scikit-learn
- Explore anomaly detection methods (e.g., Isolation Forest)
- Review flagged providers for validation
