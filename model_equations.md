# Dummy Variable Creation

Categorical variables cannot be directly used in regression models. Therefore, dummy variables were created to represent categorical values numerically.

## Region

The variable `region` contained four categories:

* North
* South
* East
* West

Three dummy variables were created:

* North_dummy
* South_dummy
* East_dummy

The category **West** was excluded and used as the reference category.

Example:

North → (1,0,0)

South → (0,1,0)

East → (0,0,1)

West → (0,0,0)

Using all four categories would create perfect multicollinearity (dummy variable trap), so one category was omitted.

---

## Store Type

The variable `store_type` contained three categories:

* Urban
* Mall
* Rural

Two dummy variables were created:

* Urban_dummy
* Mall_dummy

The category **Rural** was used as the reference category.

Urban → (1,0)

Mall → (0,1)

Rural → (0,0)

This approach avoids redundancy and allows the regression coefficients to be interpreted relative to the reference category.

---

## Dummy Variable Approach

Reference categories:

* Region: West
* Store Type: Rural

One category from each categorical variable was intentionally excluded to avoid multicollinearity and the dummy variable trap.





# Simple Regression Models

## Model 1: Monthly Sales vs Marketing Spend

Dependent Variable:

monthly_sales

Independent Variable:

marketing_spend

Regression Equation:

monthly_sales = 560777.3454 + 2.1296 × marketing_spend

R-Squared:

0.1672

Coefficient:

2.1296

P-value:

2.48 × 10^-14

Business Interpretation:

Marketing spend has a positive relationship with monthly sales. On average, every additional unit of marketing spend is associated with an increase of approximately 2.13 units in monthly sales.

Variable Usefulness:

The variable is statistically significant because the p-value is extremely small. However, the relatively low R² value indicates that marketing spend alone explains only about 16.7% of the variation in monthly sales. Therefore, marketing spend is useful but not a strong standalone predictor.

---

## Model 2: Monthly Sales vs Footfall

Dependent Variable:

monthly_sales

Independent Variable:

footfall

Regression Equation:

monthly_sales = 446410.5829 + 35.6780 × footfall

R-Squared:

0.7363

Coefficient:

35.6780

P-value:

4.75 × 10^-94

Business Interpretation:

Footfall has a strong positive relationship with monthly sales. On average, an increase of one customer visit is associated with an increase of approximately 35.68 units in monthly sales.

Variable Usefulness:

Footfall is highly statistically significant and explains approximately 73.6% of the variation in monthly sales. Therefore, footfall appears to be one of the strongest predictors of sales performance and is highly useful for regression modeling.





# Multiple Regression Model

## Dependent Variable

monthly_sales

## Independent Variables

* marketing_spend
* footfall
* inventory_availability_pct
* East_dummy

---

## Regression Equation

monthly_sales =

149038.03

* 1.1830 × marketing_spend

* 33.9480 × footfall

* 2804.17 × inventory_availability_pct

− 16716.89 × East_dummy

---

## R-Squared

R² = 0.8102

Adjusted R² = 0.8078

The model explains approximately 81% of the variation in monthly sales, indicating strong explanatory power.

---

## Intercept Interpretation

The intercept value of 149038.03 represents the baseline level of monthly sales when all independent variables are zero and the store belongs to the reference category (West region).

---

## Marketing Spend

Coefficient = 1.1830

P-value = 2.4 × 10^-17

Relationship: Positive

Business Interpretation:

An increase in marketing spending is associated with higher monthly sales. On average, one additional unit of marketing spend increases monthly sales by approximately 1.18 units, holding other variables constant.

This variable is highly statistically significant.

---

## Footfall

Coefficient = 33.9480

P-value = 1 × 10^-101

Relationship: Positive

Business Interpretation:

Footfall is one of the strongest drivers of sales. Each additional customer visit increases monthly sales by approximately 33.95 units.

This variable is extremely significant and highly important.

---

## Inventory Availability

Coefficient = 2804.17

P-value = 1.1 × 10^-8

Relationship: Positive

Business Interpretation:

Higher inventory availability improves sales performance. Stores with better stock availability tend to generate substantially higher monthly sales.

This variable is statistically significant.

---

## East Region Dummy Variable

Coefficient = -16716.89

P-value = 0.00245

Relationship: Negative

Business Interpretation:

Compared with the reference category (West region), stores located in the East region generate approximately 16,717 lower monthly sales, holding other variables constant.

The variable is statistically significant.

---

## Variable Strength

All variables have p-values below 0.05 and are statistically significant.

Footfall appears to be the strongest predictor of monthly sales.

Inventory availability and marketing spend also contribute positively to sales.

East region stores show lower sales relative to the reference category.





# Model Equations

## Simple Regression Model 1: Marketing Spend

### Equation

monthly_sales = 560777.35 + 2.1296 × marketing_spend

### Business Interpretation

Marketing spend has a positive relationship with monthly sales. On average, increasing marketing expenditure by one unit is associated with an increase of approximately 2.13 units in monthly sales.

Although marketing spend is statistically significant, it explains only a limited portion of the variation in sales.

---

## Simple Regression Model 2: Footfall

### Equation

monthly_sales = 446410.58 + 35.6780 × footfall

### Business Interpretation

Customer footfall has a strong positive effect on sales. Each additional customer visit is associated with an increase of approximately 35.68 units in monthly sales.

Footfall alone explains a large proportion of sales variation and is one of the strongest sales drivers.

---

## Multiple Regression Model

### Equation

monthly_sales =

149038.03

* 1.1830 × marketing_spend

* 33.9480 × footfall

* 2804.17 × inventory_availability_pct

− 16716.89 × East_dummy

---

## Explanation of Coefficients

### Marketing Spend

Coefficient = 1.1830

Increasing marketing expenditure is associated with higher sales. Additional marketing investment contributes positively to store performance.

### Footfall

Coefficient = 33.9480

Footfall is the strongest driver of monthly sales. Stores with higher customer traffic tend to generate significantly higher sales.

### Inventory Availability

Coefficient = 2804.17

Stores with better inventory availability achieve higher sales because customers are more likely to find products in stock.

### East Dummy Variable

Coefficient = -16716.89

The East region stores generate approximately 16,717 lower monthly sales compared with the reference region, holding other variables constant.

---

## Dummy Variable Explanation

Dummy variables were created to represent categorical variables numerically.

For the region variable:

* East_dummy = 1 for East stores.
* East_dummy = 0 otherwise.

---

## Reference Category Used

The West region was selected as the reference category.

Therefore:

* East stores are compared against West stores.
* A negative coefficient indicates lower sales compared with West stores.

One category was intentionally excluded to avoid the dummy variable trap and multicollinearity.

---

## Final Model Selected

Final Model:

Multiple Regression Model

Variables Used:

* marketing_spend
* footfall
* inventory_availability_pct
* East_dummy

R² = 0.8102

Adjusted R² = 0.8078

---

## Reason for Selecting the Final Model

The multiple regression model was selected because it provides the highest explanatory power among all models.

The model explains approximately 81% of the variation in monthly sales and incorporates multiple business drivers simultaneously.

From a business perspective, the model provides actionable insights:

* Increasing customer footfall can significantly improve sales.
* Maintaining inventory availability supports higher revenue.
* Marketing investments positively influence performance.
* Regional differences should be considered while allocating resources.

Compared with simple regression models, the multiple regression model provides a more comprehensive understanding of store performance and therefore serves as the preferred model for decision-making.



