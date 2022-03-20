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
 
**Linear Regression Cost Function**

To find the optimum betas, we need to reduce the cost function for all data points, which is given as 

        J(θ0,θ1) = ∑(i=1 to N) (yi - yi(p))2
        

**Optimisation Methods**

There are two types of Optimisation methods - 

1. Closed form solution (Differentiation)
2. Iterative form solution (Gradient Descent)


To compute optimal thetas, we need to apply Gradient Descent to the Cost function  given as follows -

∂ J(θ)
∂θ

Gradient descent is an iterative method of optimising an objective function, in our case the cost function, by moving toward the negative of the gradient. To compute θ1, equation will be - 

θ1 = θ0 - η∂ J(θ)
           ∂θ

Where η is known as the learning rate, which defines the speed at which we want to move towards negative of the gradient.


**Multiple Linear Regression**

 It represents the relationship between two or more independent input variables and a response variable. Formulation/Equation of MLR - 
 
        Y = β0 + β1X1 + β2X2 + .... + βpXp + ϵ
  
Below aspects are same as that of SLR

- The model now fits a hyperplane instead of a line.
- Coefficients are still obtained by minimising the sum of squared errors, the least squares criteria.
- The assumptions from simple linear regression still hold: zero mean, independent and normally distributed error terms with constant variance.

The new aspects to consider when moving from simple to multiple linear regression are as follows:

- Overfitting
  - As you keep adding variables, the model may become far too complex.
  - It may end up memorising the training data and, consequently, fail to generalise.
  - A model is generally said to overfit when the training accuracy is high while the test accuracy is very low.
- Multicollinearity
  - This refers to associations between predictor variables.
- Feature selection
  - Selecting an optimal set from a pool of given features, many of which might be redundant, becomes an important task.

**Multicollinearity**

Multicollinearity refers to the phenomenon of having related predictor (independent)  variables in the input data set. In simple terms, in a model that has been built using several independent variables, some of these variables might be interrelated, due to which the presence of that variable in the model is redundant. You drop some of these related independent variables as a way of dealing with multicollinearity.

Multicollinearity affects the following:

- Interpretation : change in Y when all others are held constant might not apply
- Inference : Coefficients swing wildly, signs can invert. Therefore, p-values are not reliable.

There are two ways to deal with Multicollinearity - 

- Looking at pairwise correlations
- Checking the variance inflation factor (VIF)

        VIFi = 1/(1 - Ri2)

The common heuristic we follow for the VIF values is:

- > 10:  VIF value is definitely high, and the variable should be eliminated.
- > 5:  Can be okay, but it is worth inspecting.
- < 5: Good VIF value. No need to eliminate this variable.

Some methods to deal with Multicollinearity - 

- Dropping Variables
  - Drop the variable that is highly correlated with others.
  - Pick the business interpretable variable.
- Creating a new variable using the interactions of the older variables
  - Add interaction features, i.e., features derived using some of the original features.
- Variable transformations
  - Principal component analysis

Standardisation :- x = (x - mean(x))/sd(x)
MinMax Scaling  :- x = (x - min(x))/(max(x) - min(x))

**Model Assessment and Comparison**

    Adjusted R2 = 1 - (1-R2)(N-1)/(N-p-1)

    AIC = n * log(RSS/n) + 2p

n = Sample Size
p = number of predictor variables

The adjusted R2 adjusts the value of R2 such that a model with a larger number of variables is penalised.

**Feature Selection**

Manual Feature Selection

- Build the model with all the features
- Drop the features that are the least helpful in prediction (high p-value)
- Drop the features that are redundant (using correlations and VIF)
- Rebuild the model and repeat.

Manual Feature Elimination is not a practical approach when we have large number of features.

Automated Feature Selection

- Automatically selects the number of given feature variables.

We will combine the manual approach and the automated one in order to get an optimal model relevant to the business. Hence, we first do an automated elimination (coarse tuning), and when we have a small set of potential variables left to work with, we can use our expertise and subjectivity to eliminate a few other features (fine tuning).

Multiple Linear Regression in Python steps -

- Reading and Understanding the Data
- Data Preparation
- Initial Steps
- Building the Model (1,2.. )
- Residual Analysis and Predictions
- Variable Selection using RFE

