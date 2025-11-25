# 🌟 Loan Review A/B Test: Evaluating a New AI Model for High-Risk Loan Identification

![R](https://img.shields.io/badge/R-4.3-blue?logo=r&logoColor=white)
![Data Analytics](https://img.shields.io/badge/Data_Analytics-AB_Testing-orange)
![Statistics](https://img.shields.io/badge/Statistics-T%2DTest-yellow)
![Visualization](https://img.shields.io/badge/Visualization-ggplot2-green)
![Experimental Design](https://img.shields.io/badge/Experimental_Design-tidyverse-lightblue)

---

## 📝 Project Overview

This project evaluates a **new AI-assisted loan review model** through a **10-day A/B experiment** involving 47 loan officers. The AI model was designed to improve **risk identification**, reducing misclassification of loans and improving overall loan approval quality.  

The analysis focuses on **Type I and Type II errors**, weighted error metrics, and recall improvements to quantify **business impact**.

---

## 📌 Business Problem

Loan officers often face misclassification challenges:

- **Type I Errors:** Rejecting safe loans  
- **Type II Errors:** Approving risky loans  

**Impact:**  
> Misclassifying high-risk loans leads to financial losses; misclassifying low-risk loans leads to lost revenue and dissatisfied customers.  

**Goal:**  
> Minimise financial losses and maximise profits by guiding officers with AI-driven predictions for more accurate loan reviews.

---

## 💡 Business Impact

Deploying the AI model allows the company to:

1. **Reduce Financial Losses** – Fewer risky loans approved incorrectly  
2. **Increase Revenue Opportunities** – Less rejection of safe loans  
3. **Improve Operational Efficiency** – Faster, more accurate decision-making  
4. **Maximise ROI** – Weighted error reduction ensures cost-effective approvals  

---

## 🗂 Dataset Overview

- **Original dataset:** 470 entries from 47 loan officers  
  - Control group: 19 officers  
  - Treatment group: 28 officers  
- **Cleaned dataset:**  
  - 380 entries for error analysis  
  - 330 entries for recall analysis  
- **Key Columns:**  

| Column | Description |
|--------|-------------|
| `Officer_ID` | Unique loan officer identifier |
| `Loan_ID` | Unique loan application |
| `Group` | Control / Treatment |
| `Type_I_Error` | Rejecting a safe loan |
| `Type_II_Error` | Approving a risky loan |
| `Weighted_Error` | Combined metric emphasizing financial risk |
| `Recall` | Fraction of risky loans correctly identified |
| `Final_Recall` | Post-AI prediction recall |
| `Loan_Risk_Category` | High-risk / Low-risk |

**Data Preparation Steps:**

- Removed incomplete reviews  
- Verified data integrity and consistency  
- Visualizations (raincloud plots, histograms) confirmed approximate normality for t-tests  

---

## 🧠 Methodology

- **T-tests:** Compare mean metrics between control and treatment groups  
- **Effect Size (Cohen’s d):** Measures practical significance of changes  
- **Power Analysis:** Ensures sample size sufficiency to detect meaningful effects  

All analysis performed in **R**, using **tidyverse** and **ggplot2** for data cleaning and visualization.

---

## 📊 Results Summary

### 6.1 T-Test Findings

| Metric | p-value | Mean Difference | Interpretation |
|--------|---------|----------------|----------------|
| Type I Error | 0.00405 | -6.09% | Fewer safe loans incorrectly rejected |
| Type II Error | 0.1691 | -1.13% | Not significant — no reduction in risky loans approved |
| Weighted Error | 0.00014 | -2.78% | Significant overall improvement |
| Final Recall | 0.02264 | +11.4% | More high-risk loans identified after AI predictions |
| Recall Change | 0.01097 | +7.69% | Treatment group improved detection relative to initial reviews |

### 6.2 Effect Size (Cohen’s d)

| Metric | Cohen’s d | Interpretation |
|--------|-----------|----------------|
| Type I Error | -0.72 | Moderate practical improvement |
| Type II Error | -0.36 | Small effect, minimal relevance |
| Weighted Error | -1.08 | Large, meaningful reduction |
| Final Recall | 1.37 | Large, substantial improvement |
| Recall Change | 0.67 | Moderate, meaningful improvement |

### 6.3 Power Analysis

- Type II Error: Insufficient sample to detect small effect  
- Type I Error & Recall: Strong evidence and meaningful improvements  

**Key Insight:**  
> AI-assisted model reduces Type I errors and weighted error, while significantly improving recall of high-risk loans.  

---

## 📌 Interpretation

- New AI model **reduces misclassification of low-risk loans**  
- Increases detection of high-risk loans  
- Weighted error reduction indicates **better decision quality**  
- Type II errors not significantly reduced but overall impact is minor  

**Business Takeaway:**  
> Improved decision-making leads to **financial savings, better risk management, and enhanced operational outcomes**.

---

## 📝 Recommendations

**For Analytics Manager:**

1. Stop the experiment — improvements are statistically & practically significant  
2. Refine future experiments:  
   - Adjust thresholds to balance Type I/II errors  
   - Segment analysis by officer experience, loan type, and risk category  
   - Improve data collection for complete reviews  

**For Executive Team:**

1. Gradual deployment → start small, monitor performance, scale gradually  
2. Maximise ROI → fewer rejected safe loans, better detection of risky loans, lower default rates  

---

## ⚙️ Tools & Skills Demonstrated

![R](https://img.shields.io/badge/R-4.3-blue)
![tidyverse](https://img.shields.io/badge/tidyverse-orange)
![ggplot2](https://img.shields.io/badge/ggplot2-green)
![Statistics](https://img.shields.io/badge/Statistics-T%2DTest-yellow)
![Effect Size](https://img.shields.io/badge/Effect_Size-Cohens_d-lightblue)
![Power Analysis](https://img.shields.io/badge/Power_Analysis-lightgrey)
![Data Cleaning](https://img.shields.io/badge/Data_Cleaning-lightgrey)
![Visualization](https://img.shields.io/badge/Visualization-Raincloud%2FHistograms-lightgreen)
![Business Reporting](https://img.shields.io/badge/Business_Reporting-lightpink)

---

## 📂 Quick Access

| File | Description |
|------|-------------|
| `Code/ADA_Code.html`(Code/ADA_Code.Rmd) | R code for cleaning, analysis, and visualizations |
| `Data/ADAproject_2025_data.csv` | Raw experimental data |
| `Reports/IB98D0_Group32.pdf` | Full technical report |

---

## 💡 Non-Technical Explanation

- **Type I Error:** Rejecting a safe loan → lost opportunity  
- **Type II Error:** Approving a risky loan → financial loss  
- **Recall:** Fraction of risky loans correctly identified  
- **Weighted Error:** Combines Type I & II errors based on financial cost  
- **Cohen’s d:** Practical significance of changes  
- **Power Analysis:** Ensures sample size is sufficient for reliable conclusions
