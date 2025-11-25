# 🏦 Loan Review A/B Test — Evaluating a New AI Model for High-Risk Loan Identification

[![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)](https://www.r-project.org/)
[![A/B Testing](https://img.shields.io/badge/A%2FB%20Testing-ff69b4?style=for-the-badge)]()
[![Statistics](https://img.shields.io/badge/Statistics-4caf50?style=for-the-badge)]()
[![Data Analytics](https://img.shields.io/badge/Data%20Analytics-f39c12?style=for-the-badge)]()

---

## ⭐ Executive Summary

This analysis evaluates a **new AI-assisted loan review model** using a 10-day A/B experiment.  

**Key findings:**
- Significant reduction in **Type I errors** (false positives) — fewer low-risk loans incorrectly rejected.  
- Improvement in **recall** — more high-risk loans correctly identified.  
- No significant change in **Type II errors** (false negatives).  
- **Weighted error** reduced — overall better decision-making.  

**Business impact:** Deploying this model can **reduce financial losses** and **improve loan approval quality**. 

---

## 📘 1. Project Overview

Loan officers face **misclassification challenges**:
- Type I errors: Rejecting good loans
- Type II errors: Approving risky loans  

A new AI model was tested against the old model to determine whether it improves **loan officer accuracy** and **risk identification**.  

---

## 🎯 2. Business Problem

The company’s goal: **Minimise losses from bad loans and maximise profits from good loans**.  

**Why it matters:**
- Misclassifying high-risk loans = financial losses  
- Misclassifying low-risk loans = lost revenue & customer dissatisfaction  
- AI can guide officers to make more accurate decisions

---

## 🧪 3. Experimental Design

**Hypothesis:**  
Loan officers using the **new AI model** will correctly identify more high-risk loans than those using the old model.

**Evaluation Metrics:**
- **Primary:** Recall change (proportion of risky loans correctly identified)
- **Secondary:** Weighted error, final recall  

**Weighted error explanation:**  
- Type II errors (approving risky loans) are 2× as costly as Type I errors (rejecting safe loans).  
- Weighted error metric emphasizes preventing costly mistakes.

---

## 🧹 4. Data Preparation

- **Original dataset:** 470 entries from 47 loan officers (19 control, 28 treatment)  
- Removed incomplete reviews → 380 entries for **error analysis** and 330 for **recall analysis**  
- Verified data integrity and consistency  
- **Visualizations:** Raincloud plots and histograms confirmed approximate normality → suitable for t-tests

**Technical terms explained for clarity:**
- **Recall:** Fraction of risky loans correctly identified  
- **Type I Error:** Rejecting a good loan  
- **Type II Error:** Approving a bad loan  
- **Weighted Error:** Combines Type I & II errors according to financial importance

---

## 🧠 5. Methodology

- **T-tests:** Compare average metrics between control and treatment  
- **Effect Size (Cohen’s d):** Measures practical significance  
- **Power Analysis:** Ensures sample size is enough to detect meaningful effects  

All analysis conducted in **R**.

---

## 📊 6. Results

### 6.1 T-Test Findings

| Metric | p-value | Mean Difference | Interpretation |
|--------|---------|----------------|----------------|
| Type I Error Change | 0.00405 | -6.09% | Fewer low-risk loans incorrectly rejected |
| Type II Error Change | 0.1691 | -1.13% | Not significant — no reduction in risky loans approved |
| Weighted Error Change | 0.00014 | -2.78% | Significant overall improvement |
| Final Recall | 0.02264 | +11.4% | More high-risk loans identified after AI predictions |
| Recall Change | 0.01097 | +7.69% | Treatment group improved detection relative to initial reviews |

### 6.2 Effect Size (Cohen’s d)

| Metric | Cohen’s d | Interpretation |
|--------|-----------|----------------|
| Type I Error | -0.72 | Moderate practical improvement |
| Type II Error | -0.36 | Small effect, minimal practical relevance |
| Weighted Error | -1.08 | Large, meaningful reduction |
| Final Recall | 1.37 | Large, substantial improvement |
| Recall Change | 0.67 | Moderate, meaningful improvement |

**Explanation:** Effect size shows **how impactful changes are in real business terms**, not just whether they are statistically significant.

### 6.3 Power Analysis

- Type II error: insufficient sample size to detect small effect  
- Type I error and recall: strong evidence and meaningful improvements

---

## 📌 7. Interpretation

- New model **reduces Type I errors**, improves recall, and reduces weighted errors.  
- Type II errors not significantly improved, but impact is minor.  
- Overall: **better financial and operational outcomes**.

---

## 🏁 8. Conclusions

- Reduces misclassification of low-risk loans  
- Increases identification of high-risk loans  
- Weighted errors reduced → better decision quality  
- Practical improvements justify **gradual deployment**  

---

## 📝 9. Recommendations

### For Analytics Manager
1. **Stop the experiment** — improvements are statistically & practically significant  
2. **Refine future experiments**:
   - Adjust thresholds to balance Type I/II errors  
   - Segment analysis by officer experience, loan type, risk category  
   - Improve data collection for complete reviews  

### For Executive Team
1. **Gradual deployment** → start small, monitor performance, scale gradually  
2. **Maximise ROI** → fewer rejected good loans, better detection of high-risk loans, lower default rates  

---

## ⚙️ 10. Tools & Skills Demonstrated

- **R Programming:** tidyverse, ggplot2, stats  
- **A/B Testing & Experimental Design**  
- **Effect Size & Power Analysis**  
- **Data Cleaning & Transformation**  
- **Risk & Decision Analytics**  
- **Business Reporting for Executives**

---

## 📂 11. Quick Access

| File | Description |
|------|-------------|
| `Code/Loan_Review_ABTest_Analysis.R` | R code for cleaning, analysis, and visualizations |
| `Data/ADAproject_2025_data.csv` | Raw experimental data |
| `Reports/Loan_Review_ABTest_Report.pdf` | Full report |
| `Reports/Presentation.pdf` | Executive summary slides |
| `Visuals/` | Figures and visualizations used in report |

---

## 💡 12. Non-Technical Explanation

- **Type I Error:** Rejecting a safe loan → customer loses opportunity  
- **Type II Error:** Approving a risky loan → company loses money  
- **Recall:** How many risky loans are correctly identified  
- **Weighted Error:** Combines Type I & II errors based on financial risk  
- **Cohen’s d:** Practical significance of changes  
- **Power Analysis:** Sample size sufficiency to detect meaningful improvements



