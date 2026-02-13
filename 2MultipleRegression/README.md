# Multiple Linear Regression

## Introduction

Multiple Linear Regression is a supervised machine learning algorithm used to predict a continuous dependent variable using two or more independent variables.

Unlike Simple Linear Regression (which uses one feature), Multiple Linear Regression models the relationship between multiple input variables and the output variable.

The mathematical equation is:

    Y = b0 + b1X1 + b2X2 + ... + bnXn

Where:
- Y  = Dependent variable (target)
- X1, X2, ..., Xn = Independent variables (features)
- b0 = Intercept
- b1, b2, ..., bn = Regression coefficients

The goal is to find optimal coefficients that minimize the prediction error using the **Least Squares Method**.

---

# Algorithm: MultipleLinearRegression

## Input:
    D = Training dataset with n samples and m features
    X_new = New input feature vector (X1, X2, ..., Xm)

## Output:
    Predicted value Y_pred

---

## Steps:

1. Let:
       n ← number of training samples
       m ← number of features

2. Construct the design matrix X:
       Add a column of 1s for intercept term (b0)

3. Represent output values as vector Y.

4. Compute regression coefficients using Normal Equation:

       B = (XᵀX)^(-1) XᵀY

   Where:
       B = Vector of coefficients (b0, b1, ..., bm)
       Xᵀ = Transpose of matrix X

5. Form regression model:

       Y = b0 + b1X1 + b2X2 + ... + bmXm

6. For new input X_new, compute prediction:

       Y_pred = b0 + b1X1 + b2X2 + ... + bmXm

7. Return Y_pred

---

## Cost Function

The algorithm minimizes the Mean Squared Error (MSE):

       J(B) = (1/n) Σ (Yi − Ŷi)²

Where:
- Yi  = Actual value
- Ŷi  = Predicted value

---

## Assumptions

- Linear relationship between dependent and independent variables
- No multicollinearity among features
- Homoscedasticity (constant variance of errors)
- Errors are normally distributed

---

## Time Complexity

Using Normal Equation:

    O(m³)

Where:
- m = number of features

---

## Space Complexity

    O(m²)

---

## Conclusion

Multiple Linear Regression extends simple linear regression to handle multiple input features.  
It is widely used in predictive modeling, forecasting, and data analysis due to its interpretability and effectiveness.
