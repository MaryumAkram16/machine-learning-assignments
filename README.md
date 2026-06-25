# machine-learning-assignments

# E-commerce Sales Prediction — Linear Regression

A simple linear regression model that predicts total e-commerce sales based on marketing spend.

## Overview

This project explores the relationship between marketing spend and total sales using a single-feature linear regression model. The workflow includes data visualization, model training, cross-validation, and prediction.

## Dataset

`ecommerce_sales_data.csv` — contains marketing spend and corresponding total sales figures.

**Features used:**
- `Marketing_Spend_USD` — independent variable (input)
- `Total_Sales_USD` — dependent variable (target)

## Workflow

1. **Data exploration** — loaded the dataset and visualized the relationship between marketing spend and sales using a scatter plot
2. **Correlation check** — examined correlation between marketing spend and sales to confirm a linear relationship was reasonable
3. **Model training** — fit a `LinearRegression` model from scikit-learn
4. **Cross-validation** — used 5-fold cross-validation to verify the model generalizes well, rather than relying on a single train/test split
5. **Prediction** — used the final model (fit on the full dataset) to predict sales for a given marketing spend

## Results

| Metric | Value |
|---|---|
| Coefficient | 12.62 |
| Intercept | 1834.14 |
| Mean R² (5-fold CV) | 0.964 |
| Std Dev (5-fold CV) | 0.016 |

**Interpretation:** Each additional $1 in marketing spend is associated with approximately $12.62 more in total sales. The low standard deviation across folds indicates the model's performance is consistent and not dependent on a particular train/test split.

**Example prediction:** For $1,000 in marketing spend, predicted sales ≈ **$14,450.74**

## Tech Stack

- Python
- pandas
- NumPy
- scikit-learn
- Matplotlib

## How to Run

1. Clone the repo
2. Open the notebook in Google Colab or Jupyter
3. Update the dataset path if needed
4. Run all cells

## Notes

This model shows a strong *correlation* between marketing spend and sales, not necessarily causation. Other factors (seasonality, promotions, organic demand) may influence both variables simultaneously. Further analysis (e.g., time-series decomposition or controlled experiments) would be needed to establish a causal relationship.

---
*First assignment for Linear Regression — Machine Learning coursework.*
