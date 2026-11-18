# Part 1 - Data 

This folder contains the raw source dataset and the cleaned, analysis-ready dataset used for the **Montgomery County Food Safety Inspection Risk Analysis** project.

## Data Source
* **Dataset:** [Food Inspection Dataset (Data.gov)](https://catalog.data.gov/dataset/food-inspection?from_hint=eyJxIjoiRm9vZCBpbnNwZWN0aW9uIiwic29ydCI6InJlbGV2YW5jZSJ9)
* **Publisher:** Montgomery County Department of Health and Human Services (Licensure and Regulatory Services)
* **Timeframe:** October 2022 – October 2024
* **Records:** 11,835 health inspection visits across 4,160 unique establishments

## Folder Contents

### 1. `Raw Data/`
Contains the original, unmodified inspection dataset downloaded directly from Data.gov prior to any formatting, cleaning, or filtering.

### 2. `Cleaned Data/`
Contains the cleaned Excel workbook (`DATA INSPECT.xlsx`) prepared for exploratory analysis and Tableau visualizations.

## Data Cleaning & Preparation Steps
1. **Standardization & Formatting:** Standardized date formats (`Inspection Date`), verified establishment categories across 18 facility types, and audited all 16 individual health code compliance check columns (`In Compliance`, `Out of Compliance`, `Not Applicable`).
2. **Binary Target Encoding (`Is_Adverse`):** Converted multi-class `Inspection Results` into a binary outcome variable:
   * `1` = Adverse Outcome (`Critical Violations Corrected` or `Facility Closed`)
   * `0` = Compliant Visit (`No Critical Violations Noted`)
3. **Longitudinal History Sorting:** Sorted all 11,835 records chronologically by `Establishment ID` and `Inspection Date` to ensure accurate tracking of repeat inspections across establishments.
4. **Operational Indicator Variables:** Created binary indicator flags for full-service restaurants (`Restaurant`) and non-routine visit triggers (`Reinspection`, `Complaint`).

---

*Note: Predictive modeling and logistic regression files are located in their own dedicated repository folder.*
