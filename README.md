# NYC Restaurant Food Safety Risk Analysis
# Overview

Analysis of 55,278 NYC restaurant inspections to predict poor food safety outcomes. This project merges two NYC OpenData government datasets: restaurant inspection results (2007 to 2026) and rodent inspection records (approximately 3 million rows), joined by ZIP code and month.

## The central question: does area-level rodent activity predict restaurant food safety risk, or does prior inspection history matter more?

# Key Finding

- Inspection history beats geography. Local rodent activity added only 0.0002 to the model ROC-AUC once a restaurant's own inspection history was accounted for. Risk is establishment-level, not neighbourhood-level.

#Three Questions Answered

- Which factors significantly influence the probability of a poor inspection outcome? (Statistical inference)
- Can machine learning predict whether a restaurant will fail its next inspection? (Predictive modelling)
- How do outcomes and rodent activity vary across boroughs, cuisines and seasons? (Tableau dashboard)

#Results Summary

- Logistic regression achieved a ROC-AUC of 0.610 on a 2025 to 2026 held-out test set
- Indian, Thai and Asian/Asian Fusion cuisines showed the highest odds of poor outcomes
- Prior inspection score and days since last inspection were the strongest predictors
- Rodent activity was not statistically significant (p = 0.09)
- An interactive Tableau dashboard was built to communicate findings to public health stakeholders

# Tools and Methods

- Python: pandas, NumPy, scikit-learn, statsmodels, matplotlib, seaborn
- Logistic regression, decision tree, random forest
- Time-based train/test split (train up to 2024, test 2025 onwards)
- Balanced class weights, ROC-AUC, precision, recall, F1 evaluation
- Tableau for interactive dashboard

# Data

Both datasets sourced from NYC OpenData and Data.gov (public government data).

- DOHMH NYC Restaurant Inspection Results
- NYC Rodent Inspection dataset

# How to Run
Open the notebook in Jupyter or Google Colab. Update the file paths to point to your local copies of the CSV files. Run all cells in order.
