### Summary

#### Single Linear Regression
- Machine learning models can be classified into the following two categories on the basis of the learning algorithm:
- Supervised learning method: Past data with labels is available to build the model.
  - Regression: The output variable is continuous in nature.
  - Classification: The output variable is categorical in nature.
- Unsupervised learning method: Past data with labels is not available.
- Clustering: There is no predefined notion of labels.
- Past dataset is divided into two parts in the supervised learning method:
- Training data is used for the model to learn during modelling.
- Testing data is used by the trained model for prediction and model evaluation.
- Linear regression models can be classified into two types depending upon the number of independent variables:
  - Simple linear regression: This is used when the number of independent variables is 1.
  - Multiple linear regression: This is used when the number of independent variables is more than 1.
- The equation of the best fit regression line Y = β₀ + β₁X can be found by minimising the cost function (RSS in this case, using the ordinary least squares method), which is done using the following two methods:
- Differentiation Gradient descent
- The strength of a linear regression model is mainly explained by R², where R² = 1 - (RSS/TSS).
  - RSS: Residual sum of squares
  - TSS: Total sum of squares
- RSE helps in measuring the lack of fit of a model on a given data. The closeness of the estimated regression coefficients to the true ones can be estimated using RSE. It is related to RSS by the formula:

    RSE = SQRT(RSS/df), where df = n-2 and n is the number of data points.

#### Single Linear Regression - Python
- Assumptions of simple linear regression
  - Linear relationship between X and y.
  - Normal distribution of error terms.
  - Independence of error terms.
  - Constant variance of error terms.
- Hypothesis testing in linear regression To determine the significance of beta coefficients.
    
    H0 : β1 = 0; HA : β1 ≠ 0
- T-test on the beta coefficient.

    t-score = ^βi/SE(^βi)
- Building a linear model
  - OLS (Ordinary Least Squares) method in statsmodels to fit a line.
  - Summary statistics: F-statistic, R-squared, coefficients and their p-values.
- Residual Analysis
  - Histogram of the error terms to check normality.
  - Plot of the error terms with X or y to check independence.
- Predictions: Making predictions on the test set using the 'predict()' function.
- Linear Regression using SKLearn
  - A second package apart from statsmodels for linear regression.
  - A more hassle-free package to just fit a line without any inferences.

#### Multiple Linear Regression
- When one variable might not be enough
  - A lot of variance values are not explained by just one feature.
  - Predictions are inaccurate.
- Formulation of MLR
- New considerations to be made when moving from SLR to MLR
  - Overfitting
  - Multicollinearity
  - Feature selection
- Dealing with categorical variables
  - Dummy variables for fewer levels
- Feature scaling
  - Standardisation
  - MinMax scaling
  - Scaling for categorical variables
- Model assessment and comparison
  - Adjusted R-squared
  - AIC, BIC 
- Feature selection
  - Manual feature selection
  - Automated feature selection
  - Finding a balance between the two 
 
 #### Industry Relevance Linear Regression 
- It is important to understand if a linear regression modelling will be applicable to the problem you are trying to solve. For example, linear regression cannot help you decide if a customer will opt out of a subscription, as this is a classification problem.
- Linear regression guarantees interpolation but not extrapolation.
- While linear regression can be used for both projection and prediction, there is a difference between the two. In prediction, the goal is to identify the most important variables that explain the outcome in a simpler way. In projection, the goal is to accurately forecast the outcome, no matter how complex the model gets.
- The business goal is crucial and will decide what path the modelling process should take.
- In the industry, variables that are actionable are valued over others. For example, given two quite similar variables, “Views to the platform” and “Visitors to the platform”, the latter is more actionable, as it is easier to get viewers to the platform than forcing anybody to watch the shows.
- You don’t end the modelling process until you are sure that no more significant variables could be added to explain the outcome. Thus, you check for randomness of errors, which could indicate whether any KPI that could have helped explain the outcome was left out.
