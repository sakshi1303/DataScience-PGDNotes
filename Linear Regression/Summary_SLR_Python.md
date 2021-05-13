A quick recap of simple linear regression

Assumptions of simple linear regression
- Linear relationship between X and y.
- Normal distribution of error terms.
- Independence of error terms.
- Constant variance of error terms.

Hypothesis testing in linear regression
  To determine the significance of beta coefficients.

    H0 : β1 = 0; HA : β1 ≠ 0

  T-test on the beta coefficient.

    t-score = ^βi/SE(^βi)

Building a linear model
- OLS (Ordinary Least Squares) method in statsmodels to fit a line.
- Summary statistics
   - F-statistic, R-squared, coefficients and their p-values.

Residual Analysis
- Histogram of the error terms to check normality.
- Plot of the error terms with X or y to check independence.

Predictions
- Making predictions on the test set using the 'predict()' function.

Linear Regression using SKLearn
- A second package apart from statsmodels for linear regression.
- A more hassle-free package to just fit a line without any inferences.
