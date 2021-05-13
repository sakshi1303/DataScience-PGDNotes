Machine learning models can be classified into the following three types based on the task performed and the nature of the output:

**Regression**: The output variable to be predicted is a continuous variable, e.g., the score of a student on a subject.</br>
**Classification**: The output variable to be predicted is a categorical variable, e.g., classifying incoming emails as spam or ham.</br>
**Clustering**: No predefined notion of a label is allocated to the groups/clusters formed, e.g., customer segmentation. 

Machine Learning model can be classified into - 

**Supervised learning methods**

Past data with labels is used for building the model.</br>
Regression and classification algorithms fall under this category.</br>

**Unsupervised learning methods**

No predefined labels are assigned to past data.</br>
Clustering algorithms fall under this category.</br>

**Regression Line** - 

y = β0 + β1 = 0 

A simple linear regression model attempts to explain the relationship between a dependent variable and an independent one using a straight line.

The independent variable is also known as the **predictor**/**feature** variable, and the dependent variables are also known as the **output** variables.

**Best Line** - The best fit line is obtained by minimising a quantity called the residual sum of squares (RSS) which is a cost function.

Ways to minimize Cost Funtion -

- Differentiation
- Gradient Descent

**Gradient Descent**

Gradient descent is an optimisation algorithm that optimises the objective function (cost function for linear regression) to reach the optimal solution.

The strength of a linear regression model is mainly explained by R², where R² = 1 - (RSS/TSS).

RSS: Residual sum of squares</br>
TSS: Total sum of squares</br>
RSE: Residual Squared error</br>

RSE = SQRT(RSS/df), where df = n-2 and n is the number of data points.

**Simple Linear Regression**

When output variable is dependent only one feature/independent variable , it is known as Simple Linear Regression.

**Assumptions of Simple Linear Regression**

- There is a linear relationship between X and Y
- Error terms are normally distributed with mean zero(not X, Y)
- Error terms are independent of each other
- Error terms have constant variance (homoscedasticity)


**Hypothesis Testing in Linear Regression**

    Null Hypothesis(H0): β1 = 0
    Alternate Hypothesis(H0): β1 ≠ 0

If the p-value turns out to be less than 0.05, you can reject the null hypothesis and state that β1 is indeed significant.

**Building a Linear Model**

```python

from sklearn.model_selection import train_test_split
X_train_lm, X_test_lm, y_train_lm, y_test_lm = train_test_split(X, y, train_size = 0.7, test_size = 0.3, random_state = 100)

import statsmodels.api as sm
X_train_sm = sm.add_constant(X_train)
lr = sm.OLS(y_train, X_train_sm)
lr_model=lr.fit()

```

OLS stands for Ordinary Least Squares which is the method that 'statsmodels' use to fit the line. We used the command 'add_constant' so that statsmodels also fits an intercept. If we  don't use this command, it will fit a line passing through the origin by default.

F-statistic tells whether the overall model fit is significant or not.
Prob (F-statistic) - If its value < 0.05 then we can conclude that the overall model fit is significant. If it is > 0.05, we might need to review our model as the fit might be by chance, i.e. the line may have just luckily fit the data. 

R-squared of 0.816 means that the model is able to explain 81.6% of the variance which is pretty good.

**Residual Analysis and Predictions** 

- Error terms should be normally distributed with mean equal to 0 - Plot a histogram of the error terms to check whether they are normally distributed. 
- The error terms should be independent of each other - Plot the error terms, this time with either of X or y to check for any patterns.

predict() function - present in statsmodels.api which is used to make predictions on test dataset.

**Linear Regression using SKLearn** - SKLearn is a ‘lighter’ version of the linear regression packages. 

```python

from sklearn.linear_model import LinearRegression

lm = LinearRegression()   # Create a linear regression object
lm.fit(X_train, y_train)

```
 
