Machine learning models can be classified into the following two categories on the basis of the learning algorithm:

Supervised learning method: Past data with labels is available to build the model.</br>
    Regression: The output variable is continuous in nature.</br>
    Classification: The output variable is categorical in nature.</br>

Unsupervised learning method: Past data with labels is not available.</br>
    Clustering: There is no predefined notion of labels.
  
Past dataset is divided into two parts in the supervised learning method: 

Training data is used for the model to learn during modelling.</br>
Testing data is used by the trained model for prediction and model evaluation.</br>

Linear regression models can be classified into two types depending upon the number of independent variables: 

Simple linear regression: This is used when the number of independent variables is 1.</br>
Multiple linear regression: This is used when the number of independent variables is more than 1.</br>

The equation of the best fit regression line Y = β₀ + β₁X can be found by minimising the cost function (RSS in this case, using the ordinary least squares method), which is done using the following two methods:

Differentiation
Gradient descent 

The strength of a linear regression model is mainly explained by R², where R² = 1 - (RSS/TSS).

RSS: Residual sum of squares</br>
TSS: Total sum of squares

RSE helps in measuring the lack of fit of a model on a given data. The closeness of the estimated regression coefficients to the true ones can be estimated using RSE. It is related to RSS by the formula: 

RSE = SQRT(RSS/df), where df = n-2 and n is the number of data points.
