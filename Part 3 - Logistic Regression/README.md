
# Part 3 - Logistic Regression

This folder contains the predictive modeling workbook used to estimate the likelihood of adverse food safety inspections across Montgomery County establishments[cite: 15].

## Folder Contents
* **`Logistic Regression.xlsx`:** Complete Microsoft Excel workbook containing the engineered predictor variables, XLMiner multivariable logistic regression output, predicted failure probabilities across all 11,835 records, and $2 \times 2$ confusion matrix performance metrics[cite: 15].

## Model Specification & Methodology
* **Modeling Tool:** Microsoft Excel (XLMiner Data Analysis ToolPak)
* **Sample Size:** $N = 11,835$ health inspection visits (October 2022 – October 2024)
* **Dependent Variable (`Is_Adverse`):** Binary indicator (`1` = Critical Violations Corrected or Facility Closed; `0` = No Critical Violations Noted)
* **Independent Variables:**
  * `Prior_Adverse`: Lagged compliance indicator tracking whether the facility failed its immediately preceding inspection (created by sorting records chronologically by `Establishment ID` and `Inspection Date`).
  * `Restaurant`: Binary indicator for full-service restaurants.
  * `Reinspection`: Binary indicator for follow-up reinspection visits.
  * `Complaint`: Binary indicator for consumer complaint-driven investigations.

## Summary of Regression Results

| Predictor Variable | Coefficient ($\beta$) | Standard Error | $P$-value | Odds Ratio ($\text{OR}$) | Key Interpretation |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **Intercept** | $-1.2429$ | $0.0337$ | $< 0.001$ | $0.289$ | Baseline log-odds for non-restaurant initial visits |
| **Prior_Adverse** | $+0.8804$ | $0.0495$ | $< 0.001$ | **2.412** | **2.41x higher odds** of failing again after a prior failure |
| **Restaurant** | $+0.5694$ | $0.0420$ | $< 0.001$ | **1.767** | **76.7% higher odds** of failure vs. non-restaurant venues |
| **Reinspection** | $-1.1959$ | $0.1011$ | $< 0.001$ | **0.302** | **69.8% reduction** in failure odds on follow-up visits |
| **Complaint** | $-1.8817$ | $0.2087$ | $< 0.001$ | **0.152** | Standalone complaints rarely yield critical citations |

## Classification Performance & Threshold Optimization
* **Standard 0.50 Cutoff:** Achieves **69.66% overall accuracy** with a low **7.27% False Positive Rate**, but produces an **82.42% False Negative Rate** (missing over 8 out of 10 actual violators because overall baseline failure rates sit at 30.7%).
* **Recommended 0.30 Cutoff:** Lowering the dispatch threshold from `0.50` to `0.30` cuts the False Negative Rate down to **30.24%**, flagging repeat offenders and full-service restaurants so inspectors capture nearly **70%** of critical violators proactively.
