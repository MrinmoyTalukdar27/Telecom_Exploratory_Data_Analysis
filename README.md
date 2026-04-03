# 📡 Telecom Customer Churn — Exploratory Data Analysis (EDA)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Plots-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

> An end-to-end exploratory analysis of a telecom company's customer base — identifying the key drivers behind customer churn across **7,043 records and 21 features**.

---

## 📌  Project Overview

Customer churn is one of the most expensive problems in the telecom industry. Acquiring a new customer costs significantly more than retaining an existing one, which makes it critical to understand *why* customers leave. This project digs into a real-world telecom dataset to uncover patterns in demographics, service usage, contract behaviour, and payment habits — all with the goal of understanding what separates customers who stay from those who don't.

---

## 🎯 Objectives

- Understand the overall scale of churn in the dataset
- Identify which customer segments are most at risk
- Explore how contract type, tenure, and services subscribed relate to churn
- Draw actionable conclusions that could support a real retention strategy

---

## 📊 Key Findings

| Factor | Finding |
|--------|---------|
| **Overall Churn Rate** | 26.54% of customers churned (1,869 out of 7,043) |
| **Gender** | No meaningful difference — churn is equal across male and female customers |
| **Senior Citizens** | Seniors churn at a disproportionately higher rate than non-seniors |
| **Tenure** | Churn peaks in the first 1–2 months; long-term customers rarely leave |
| **Contract Type** | Month-to-month customers churn far more than those on 1 or 2-year contracts |
| **Services** | Customers without add-ons (security, backup, tech support) churn more |
| **Payment Method** | Electronic check users have the highest churn rate |

---

## 📂 Dataset

- **File:** `telecome.csv`
- **Records:** 7,043 customers
- **Target Variable:** `Churn` (Yes / No)
- **Features:** 21 columns including demographics, service subscriptions, contract info, and billing

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas** — data loading, cleaning, and transformation
- **NumPy** — numerical operations
- **Matplotlib** — base-level plotting
- **Seaborn** — statistical visualisations

---

## 🧹 Data Cleaning Steps

1. **Churn Label Fix** — A corrupt value `'No11'` was found in the Churn column and replaced with `'No'` to ensure only two valid categories existed.
2. **TotalCharges Conversion** — The column was stored as a string with blank spaces for customers with zero tenure. Blanks were replaced with `'0'` and the column was cast to `float64`.
3. **SeniorCitizen Encoding** — Binary values (0/1) were mapped to readable strings (`'yes'`/`'no'`) using a custom function for cleaner visualisations.
4. **Null & Duplicate Check** — Confirmed zero null values and zero duplicate records across both full rows and unique customer IDs.

---

## 📈 Visualisations Included

1. **Churn Count Bar Chart** — Raw counts of churned vs retained customers with bar labels
2. **Churn Pie Chart** — Percentage breakdown of churned vs retained
3. **Churn by Gender** — Side-by-side count plot comparing churn across gender
4. **Senior Citizen Count** — Distribution of senior vs non-senior customers
5. **Senior Citizen Churn (Stacked Bar)** — Churn percentage within each age group
6. **Tenure Histogram** — Distribution of customer tenure coloured by churn status
7. **Churn by Contract Type** — Count plot across month-to-month, 1-year, and 2-year contracts
8. **Services vs Churn (3×3 Grid)** — Nine subplots covering PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies
9. **Churn by Payment Method** — Labelled count plot across all four payment methods

---

## 🚀 How to Run

1. **Clone the repository**
```bash
   git clone https://github.com/your-username/telecom-churn-eda.git
   cd telecom-churn-eda
```

2. **Install dependencies**
```bash
   pip install pandas numpy matplotlib seaborn jupyter
```

3. **Launch the notebook**
```bash
   jupyter notebook Telecom_churned__analysis.ipynb
```

4. Make sure `telecome.csv` is placed in the same directory as the notebook before running.

---

## 📁 Project Structure
```
telecom-churn-eda/
│
├── Telecom_churned__analysis.ipynb   # Main Jupyter Notebook
├── telecome.csv                       # Dataset (add your own copy)
├── README.md                          # Project documentation
└── Telecom_Churn_EDA_Report.pdf       # Full PDF analysis report
```

---

## 💡 Recommendations

Based on the analysis, here are the most impactful actions a telecom company could take:

- **Focus retention efforts on the first 3 months** — this is when churn risk is highest and early engagement makes the biggest difference.
- **Incentivise longer contracts** — even a small discount for switching from month-to-month to an annual plan can dramatically reduce churn.
- **Promote add-on services** — customers with security, backup, and tech support are far less likely to leave. Bundling these into plans increases both revenue and loyalty.
- **Target senior customers with dedicated support** — simplified plans or a dedicated helpline could meaningfully reduce churn in this group.
- **Encourage auto-pay enrolment** — customers on automatic payment methods churn significantly less, making this a low-effort, high-impact nudge.

---

## 🔭 Next Steps

This EDA lays the groundwork for building a **predictive churn model**. Potential next steps include:

- Feature engineering (e.g., encoding categorical variables, creating risk scores)
- Training classification models — Logistic Regression, Random Forest, XGBoost
- Evaluating models using precision, recall, and AUC-ROC
- Deploying a churn prediction pipeline for real-time flagging

---

## 👤 Author

**Mrinmoy Talukdar**  
📧 mrinmoytalukdargcu@gmail.com 

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
