# Phone Pricing Regression Analysis
This project explores the relationship between various mobile phone specifications and their market prices using linea regression techniques. 

## 📌 Objective
The goal is to identify significant predictors of phone price and build the best predictive model using multiple selection strategies.

## 📅 Dataset
Data: Mobile phone price

Predictor Variables: RAM, Internal Memory, Screen Size, PPI (Pixels Per Inch), CPU Core & Frequency, Rear and Front Camera, Battery Capacity, Thickness, Weight

Source: Kaggle

## 🔍 Project Workflow
**1. Exploratory Data Analysis (EDA)**
- Structural summary of variables using str() and summary()
- Scatter plots of Price vs. each predictor
- Correlation matrix & visualization via corrplot

**2. Model Fitting**
- Full model: Price ~ . using all predictors
- Model 1: Price ~ RAM
- Model 2: Price ~ Thickness
- Model 3: Price ~ RAM + Thickness

**3. Model Selection Techniques**
- Multicollinearity Check: Variance Inflation Factor (VIF)
- VIF-based model (Model 4): Removed variables with high multicollinearity
- Best Subset Selection: Using regsubsets()
- BIC-based model (Model 5)
- Forward, Backward and both directions Stepwise Regression (Model 6):

**4. Model Evaluation**

Metrics Used:

- R-squared & Adjusted R-squared
- Mallows’ Cp
- Akaike Information Criterion (AIC)

Model 6 selected as the best-performing model based on overall performance across all metrics.

**5. Generalized Linear Models**
Converted all linear models (Model 1–6 + full model) to GLMs for comparison.

**6. Diagnostic Checks**
- Residual analysis (standardized & studentized residuals)
- Histogram and scatter plot visualization with ggplot2
- Diagnostic plots from plot(model)
- Confidence Intervals for coefficients
- ANOVA on final model

## Final Model
Model 6 shows that **RAM, number of CPU cores, CPU frequency, PPI, internal memory, battery, screen size and thickness and front camera** significantly influences the mobile price.

## Implications
To target the higher-end customers, where customers are willing to pay more, mobile company could tailor the mobile design according to the significant features. For instance:
- invest in advanced display technology and higher memory capacities
- invest in mobile with longer battery life
- reduce thickness of mobile phone

### Acknowledgement
This project was completed as part of a Regression Analysis class assignment at Sunway University. 
