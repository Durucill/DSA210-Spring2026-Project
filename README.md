# Netflix Viewing Behavior and Snack Consumption Analysis

## Project Overview
This project analyzes the relationship between Netflix viewing behavior and snack consumption using real 60-day data.

The goal is to understand whether watching more Netflix is associated with a higher likelihood of having snacks available.

---

## Dataset
The dataset combines:
- Netflix viewing history (titles and dates)
- Food order / snack availability data

After cleaning and merging, the final dataset includes daily observations.

---

## Variables
- Netflix_Count: Number of Netflix items watched per day
- Snack_Available: Whether snacks were available (0 = No, 1 = Yes)
- Order_Day: Whether a food order was made (0 = No, 1 = Yes)

---

## Exploratory Data Analysis (EDA)

The following analyses were performed:
- Summary statistics (mean, std, distribution)
- Histograms for all variables
- Correlation heatmap
- Scatter plot (Netflix_Count vs Snack_Available)

These helped to understand the distribution and potential relationships between variables.

---

## Hypothesis Testing

H0 (Null Hypothesis): There is no relationship between Netflix viewing and snack availability  
H1 (Alternative Hypothesis): There is a relationship between Netflix viewing and snack availability  

We used Pearson correlation to test the relationship.

---

## Results

- Correlation: 0.145  
- P-value: 0.266  

---

## Conclusion

Since the p-value is greater than 0.05, we fail to reject the null hypothesis.

This means there is no statistically significant relationship between Netflix viewing behavior and snack availability in this dataset.

Although a slight positive correlation exists, it is weak and not statistically meaningful.

---

## Files

- analysis.ipynb → Main analysis notebook  
- final_merged_analysis_data.csv → Cleaned dataset  
- graph.png → Visualization example
- 
