# Customer Churn Analysis (Telecom)

## Problem Statement

Why do customers leave a telecom company, and which customer groups are most at risk? This project cleans the data, explores churn patterns, and turns the findings into practical retention recommendations.

## Dataset

[Telco Customer Churn (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn): 7,043 customers and 21 columns covering demographics, services, contracts, billing, and churn.

## Tools

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook in VS Code

## Project Steps

1. **Clean the data:** Convert `TotalCharges` from text to numeric and fill its 11 blank values with `0` for customers with zero tenure. Check for duplicates and create `ChurnFlag` and `TenureGroup` columns.
2. **Explore churn patterns:** Calculate churn rates overall and by contract, tenure, payment method, and monthly charges.
3. **Visualize results:** Create bar charts, histograms, box plots, and a correlation heatmap.
4. **Summarize findings:** Identify factors associated with churn and develop practical retention recommendations.

## Key Findings

The overall churn rate is **26.5%**.

| Factor | Finding |
|---|---|
| Contract type | Month-to-month churn is **42.7%**, compared with **11.3%** for one-year and **2.8%** for two-year contracts. |
| Tenure | Churn is **47.4%** among customers in their first 12 months, falling to **9.5%** for customers with 49 or more months of tenure. |
| Payment method | Electronic check users have **45.3%** churn, compared with **15–19%** for users of other payment methods. |
| Monthly charges | Churned customers pay **$74.44** per month on average, compared with **$61.27** for customers who stayed. |

Correlation with churn: tenure **-0.35**, monthly charges **+0.19**, and total charges **-0.20**. These are associations and do not establish that a factor causes churn.

## Recommendations

- Offer discounts or perks to encourage month-to-month customers to choose one- or two-year contracts.
- Create an onboarding and check-in program for the first 12 months, when churn is highest.
- Encourage electronic check users to switch to automatic card or bank payments, potentially with a small bill credit.
- Review pricing and perceived value for customers with higher monthly bills.

## Charts

The notebook includes:

- Churn by contract type
- Churn by payment method
- Churn by tenure group
- Histograms
- Box plots
- Correlation heatmap

## Project Structure

```text
├── data/                 # Dataset files
├── images/               # Saved charts
├── churn_analysis.ipynb  # Analysis notebook
├── requirements.txt      # Python dependencies
└── README.md
```

## How to Run

From the project folder, install the dependencies and launch the notebook:
```bash
python -m pip install -r requirements.txt
jupyter notebook churn_analysis.ipynb
```