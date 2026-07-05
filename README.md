# 📞 AlphaCom Customer Churn Prediction: Proactive Revenue Safeguarding Framework

![Python](https://img.shields.io/badge/Language-Python_3.10-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Framework-Scikit--Learn-orange.svg)
![Machine Learning](https://img.shields.io/badge/Field-Supervised__Classification-green.svg)
![Domain](https://img.shields.io/badge/Industry-Telecommunications-red.svg)

## 📌 Project Overview and Strategic Objective
AlphaCom, a leading telecommunications provider, has recently experienced a concerning rise in customer churn despite offering a highly competitive and wide product portfolio. Unchecked account cancellation directly penalizes recurring revenue streams and dramatically expands customer acquisition costs (CAC) in an intensely saturated marketplace.

**Objective:** As a Data Scientist at AlphaCom, I developed an end to end predictive framework designed to flag subscribers at high risk of turning over. By shifting from a reactive strategy to a data driven proactive retention architecture, this model empowers leadership to deploy highly targeted loyalty incentives, protect existing revenue and maximize customer lifetime value (LTV).

---

## 🔍 Core Data Insights (Part 1: Exploratory Data Analysis)
An exploratory evaluation was performed across a dataset of subscriber transaction records to locate historical friction vectors prior to modeling:
* **Contractual Vulnerabilities:** Month to month contracts represent an overwhelming risk factor. Subscribers on short-term rolling structures display significantly higher churn rates compared to those on fixed 1 year or 2 year commitments.
* **Infrastructure Anomalies:** Customers subscribing to high-speed **Fiber Optic** connections showed an elevated velocity of drop offs, indicating a critical need to evaluate installation friction, pricing satisfaction or network stability.
* **Financial Risk Triggers:** Account profiles exhibiting high `MonthlyCharges` paired with short continuous account `tenure` indicate severe early-stage budget friction, serving as a primary churn warning light.

---

## 🤖 Predictive Machine Learning Architecture (Part 2: Modeling)
The production pipeline implements thorough data hygiene workflows to prepare attributes safely before ingestion:
* **Preprocessing Pipeline:** Category expressions undergo full dummy variable transformation (One Hot Encoding), missing monetary rows within `TotalCharges` are resolved via median imputation, and partitions are stratified using a clean training, validation and testing split methodology.

### Supervised Classification Model Performance
Multiple classification models were trained and performance metrics cross verified over isolated testing partitions:

| Classification Model | Testing Precision | Target Sensitivity (Recall) | Core F1-Score | Area Under ROC Curve |
| :--- | :---: | :---: | :---: | :---: |
| Baseline K-Nearest Neighbors (KNN) | 0.57 | 0.54 | 0.55 | 0.7843 |
| Baseline Decision Tree | 0.50 | 0.50 | 0.50 | 0.6493 |
| **Optimized Champion Logistic Regression** | **0.67** | **0.57** | **0.61** | **0.8464** |

* **Champion Model Selection:** The optimized **Logistic Regression** model outpaced competing baseline classifiers. It established the cleanest generalization equilibrium, achieving a top Area Under the ROC Curve of **0.8464** for tracking active risk markers.

---

## 💡 Executive Business Recommendations
1. **Contract Migration Campaigns:** Design proactive marketing incentives (e.g. promotional credits or service upgrades) explicitly engineered to transition month to month customers over to long term 1 year or 2 year fixed agreements.
2. **Fiber Optic Experience Audits:** Partner with the technical operations department to audit accounts utilizing Fiber Optic connections. Deploy automated post installation quality touchpoints to neutralize service complaints before they lead to cancellations.
3. **Automated Billing Incentives:** Accounts linked to manual electronic checks exhibit distinct drop off habits. Introduce small monthly account credits to steer subscribers into adopting low friction automated credit card or direct bank transfer payment structures.

---

## 🛠️ Repository Directory and Execution
The project files are mapped into clear operational steps:
* `Part_1_Exploratory_Data_Analysis/`: Contains the exploratory notebooks, demographic deep dives and raw source file distributions (`customer_churn.csv`).
* `Part_2_Machine_Learning_Modeling/`: Holds the predictive modeling scripts, model validation configurations and baseline comparison tables.
