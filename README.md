# Final-Project-Food-Inspection-Montgomery-County
BUS 446 Final Project
# Food-Safety-Inspection-Risk-Analysis-Montgomery-County

README for Food Safety Inspection Risk Analysis: Montgomery County (Data Analytics Final Project)

## Data Section
The data used for this project is sourced from the Data.gov repository [Food Inspection Dataset](https://catalog.data.gov/dataset/food-inspection?from_hint=eyJxIjoiRm9vZCBpbnNwZWN0aW9uIiwic29ydCI6InJlbGV2YW5jZSJ9). The study analyzes 11,835 health inspection records across 4,160 unique food establishments collected between October 2022 and October 2024. Data cleaning, binary target encoding (`Is_Adverse`), and longitudinal sorting (`Prior_Adverse`) steps are detailed in the report, and the cleaned dataset is available in the `DATA INSPECT.xlsx` file.

## Visualization with Final Findings Section
This section contains the Tableau workbooks (`Project for class.twb` and `Projecct for class Q2.twb`) and exported high-resolution charts used in the project presentation and report. The visualizations cover inspection outcome rates by facility category, the corrective impact of follow-up reinspections, the Pareto ranking of top health code violations, violation hotspots by establishment type, and seasonal refrigeration failure trends.

## Analytics & Modeling Section
The `Logistic Regression.xlsx` file in this repository contains the multivariable logistic regression model built using the Excel XLMiner Data Analysis ToolPak. The worksheet includes chronological sorting logic to create the `Prior_Adverse` predictor, regression parameter estimates, odds ratios, predicted failure probabilities for all 11,835 inspections, and the $2 \times 2$ confusion matrix evaluating classification accuracy and threshold cutoffs.

## Key Findings
* **Facility Risk Profiles:** Public Middle Schools (40.5%), Restaurants (36.2%), and Carry Out locations (33.2%) experience the highest adverse inspection rates, while Snack Bars (11.2%) and Caterers (12.7%) experience the lowest.
* **Reinspection Impact:** Follow-up reinspections drop violation rates down to approximately 11% across facility categories, demonstrating rapid compliance recovery after official citations.
* **Top Health Code Violations:** Cold Holding Temperature (19.9% of visits) and Rodents and Insects (15.5% of visits) account for the majority of critical citations county-wide.
* **Seasonal Weather Strain:** Cold holding temperature violations increase from 18.3% in winter to 21.8% in summer due to outdoor heat waves straining commercial refrigeration units.
* **Predictive Risk Drivers:** Multivariable logistic regression shows that failing a prior inspection more than doubles the odds of failing again (Odds Ratio = 2.41), while full-service restaurants face 77% higher odds of failure than baseline retail markets.
* **Threshold Optimization:** At the standard 0.50 cutoff, the model reaches 69.7% overall accuracy but misses 82.4% of actual violators; lowering the dispatch cutoff to 0.30 captures nearly 70% of critical violators proactively.

## Business Case Report Section
This section presents the project report *"Food Safety Inspection Risk Analysis: Montgomery County"* by the team Soum’s Prodigies (Mikey Vang, Jace Miller, Maxwell Blanc, & Ryan Winkler). The paper evaluates operational, environmental, and historical drivers of food safety violations from 2022 to 2024. It includes an executive summary, data and methodology overview, visual findings from Tableau, logistic regression modeling and confusion matrix evaluation, strategic recommendations for health inspectors, and embedded figures.

## How to Use This Repository
* **Accessing the Paper:** The full Business Case Report is available in the accompanying Word/PDF report file in this repository.
* **Datasets & Models:** Raw and cleaned inspection records are stored in `DATA INSPECT.xlsx`, and the XLMiner logistic regression model is stored in `Logistic Regression.xlsx`.
* **Visualizations:** Interactive Tableau workbooks (`Project for class.twb` and `Projecct for class Q2.twb`) and exported chart images are included in the repository files.

## Additional Information
* The project is based on Montgomery County food inspection data collected from October 2022 through October 2024.
* For inquiries, contact the author, Mikey Vang, Jace Miller, Maxwell Blanc, Ryan Winkler.

---

*Note: This README file provides an overview. Refer to the respective files and report sections for detailed information.*
