# Part 4 - Business Case Report

This folder contains the final written Business Case Report for **BUS 446**, synthesizing the exploratory data analysis, Tableau visualizations, and multivariable logistic regression findings into actionable policy recommendations for Montgomery County health officials.

## Folder Contents
* **`Business Case Report - BUS 446.pdf`:** Final formatted PDF version of the report with all embedded Tableau figures, Excel regression tables, and section formatting preserved for easy viewing[cite: 14].
* **`Business Case Report - BUS 446.docx`:** Editable Microsoft Word version of the full report[cite: 14].

## Report Structure & Sections
1. **Executive Summary:** High-level overview of the 11,835 inspection records, core risk drivers, and recommended resource-allocation reforms.
2. **Data and Methodology:** Explanation of data sourcing from Data.gov, binary outcome encoding (`Is_Adverse`), longitudinal compliance sorting (`Prior_Adverse`), and analytical workflows across Tableau and Excel XLMiner.
3. **Facility Risk and Inspection Dynamics (Question 1):** Breakdown of adverse outcome rates across 18 facility categories—highlighting high-risk kitchens such as Public Middle Schools (40.5%), Restaurants (36.2%), and Carry Out locations (33.2%)—and the sharp compliance drop during follow-up reinspections (~11%).
4. **Top Violations and Seasonal Weather Patterns (Question 2):** Pareto ranking of the 16 health code check items, facility-specific hazard hotspots, and the summer spike in Cold Holding Temperature failures (rising from 18.5% in winter to 21.8% in summer).
5. **Predictive Modeling and Evaluation (Question 3):** Parameter estimates and odds ratios from the multivariable logistic regression model, demonstrating that prior failures more than double failure odds ($\text{OR} = 2.41$), along with a $2 \times 2$ confusion matrix comparing the 0.50 and 0.30 probability cutoffs.
6. **Strategic Policy Recommendations:** Three actionable reforms for the Montgomery County Department of Health and Human Services: lowering the dispatch threshold to `0.30`, automating priority queues for repeat offenders, and conducting pre-summer commercial refrigeration audits.
