# Netflix Viewing Behavior and Snack Consumption Analysis

## Project Overview
This project analyzes the relationship between Netflix viewing behavior and snack consumption using a **4-year real-world dataset**.

The goal is to understand whether watching more Netflix is associated with a higher likelihood of ordering snacks.

---

## Dataset
The dataset combines:

- Netflix viewing history (titles and dates)
- Snack order data (binary: 0 = No, 1 = Yes)

After cleaning and merging, the final dataset contains **daily observations over 4 years (~400+ days).**

---

## Variables

- **Netflix_Count**: Number of Netflix items watched per day  
- **Snack_Order**: Whether a snack/food order was made (0 = No, 1 = Yes)  
- **Snack_Next_Day**: Snack order on the following day (for lag analysis)

---

## Exploratory Data Analysis (EDA)

The following analyses were performed:

- Summary statistics (mean, std, distribution)
- Missing value analysis
- Histograms for variables
- Time series visualization
- Correlation heatmap
- Boxplot (Netflix usage vs snack order)
- Scatter plot
- Logistic Regression model for prediction

These helped to understand the distribution and potential relationships between variables.


---

## Hypothesis Testing

- **H0 (Null Hypothesis):** There is no relationship between Netflix viewing and snack ordering  
- **H1 (Alternative Hypothesis):** There is a relationship between Netflix viewing and snack ordering  

We used **Pearson correlation** to test the relationship.

---

## Results

- **Correlation:** ~0.18  
- **P-value:** ~0.00019  

- **Lag Correlation (Next Day):** ~0.018  

---

## Conclusion

- There is a **weak positive correlation** between Netflix watching and snack ordering.
- The relationship is **statistically significant** (p < 0.05).
- However, the effect size is small → meaning Netflix usage alone is not a strong predictor of snack behavior.
- - Machine learning results support this finding, as the model struggled to predict snack orders accurately and defaulted to the majority class.

- **Lag analysis shows almost no relationship**, meaning watching Netflix today does not significantly affect snack orders the next day.

---

## Files

- `analysis-4year.ipynb` → Main analysis notebook  
- `netflix_last_4_years.xlsx` → Netflix viewing data  
- `snack_netflix_4years.xlsx` → Snack order dataset  
- `README.md` → Project documentation  
- `DSA210-PROJECT PROPOSAL` → Initial proposal  

---

## How to Run

1. Open the notebook in Google Colab or Jupyter
2. Make sure the Excel files are in the same directory
3. Run all cells

---

## Notes

- Dataset is cleaned and preprocessed within the notebook
- All visualizations and statistical tests are reproducible
## Machine Learning

We applied Logistic Regression to predict whether a snack order occurs based on Netflix usage.

### Model Setup
- Feature: Netflix_Count
- Target: Snack_Order
- Train/Test split: 80/20

### Results
- Accuracy: ~71%
- The model shows high accuracy due to class imbalance, predicting mostly the majority class (snack order = 1).
- It fails to correctly identify the minority class (no snack orders).

However, the model predicts almost all observations as "snack order = 1", failing to capture the minority class.

### Interpretation
This indicates a class imbalance problem and suggests that Netflix usage alone is not a strong predictor of snack ordering behavior.

These results are consistent with the statistical analysis, which showed only a weak relationship between the variables.
These findings are consistent with the hypothesis testing results, which showed a weak but statistically significant relationship.
