# Auto MPG Regression Model Comparison

This project analyzes the fuel efficiency of vehicles using the Auto dataset (392 observations). The goal is to model **miles per gallon (mpg)** using multiple linear regression while addressing violations of regression assumptions.

Several model correction strategies were applied to improve model performance and satisfy linear regression assumptions.

## Objective

Build and compare regression models to explain and predict vehicle fuel efficiency while addressing violations of:

- Linearity
- Zero mean assumption
- Constant variance (homoskedasticity)
- Normality of residuals

## Models Constructed

Five regression models were developed using different transformation strategies:

### Model 1 – Polynomial Regression
Square terms were added for predictors exhibiting nonlinear relationships with mpg.

### Model 2 – Log Transformation of Predictors
Log transformations were applied to displacement, horsepower, and weight to improve linearity.

### Model 3 – Log Transformation of Response
The response variable (mpg) was log-transformed to address heteroskedasticity and non-normal residuals.

### Model 4 – Log-Log Model
Both the response and selected predictors were log-transformed.

### Model 5 – Box-Cox Transformation
The response variable was transformed using the Box-Cox method with the optimal λ value.

## Model Comparison

| Model | R² |
|-----|-----|
| Model 1 | 0.760 |
| Model 2 | 0.748 |
| Model 3 | 0.791 |
| Model 4 | **0.805** |
| Model 5 | 0.798 |

Model 4 achieved the highest explanatory power.

## Final Selected Model

**Model 4 (Log-Log Model)** was selected as the best model because:

- Highest R² (0.805)
- Regression assumptions are largely satisfied
- Predictors are statistically significant
- Residual diagnostics indicate approximately normal distribution
- Box-Cox transformation suggested λ ≈ 0.19, supporting the use of log transformation

## Interpretation Example

In the log-log model:

- A **1% increase in horsepower decreases mpg by approximately 0.484%**.

## Tools Used

- Python
- pandas
- numpy
- statsmodels
- scipy
- matplotlib
- seaborn

## Project Files

- `Code.ipynb` – analysis code
- `Auto-1.csv` – dataset
- `Analytical Report.pdf` – full analytical report
