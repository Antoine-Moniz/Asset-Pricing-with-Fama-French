# Estimation and Validation of the Fama-French 5-Factor Model

This project focuses on estimating and testing the Fama-French 5-Factor Model. This model is a popular framework in finance for explaining variations in portfolio returns based on several systematic factors.

## Objectives

1. Estimate the coefficients of the Fama-French 5-Factor Model for stock portfolios listed on the NYSE, AMEX, and Nasdaq.
2. Assess how well these factors explain the variations in expected returns.
3. Test the model's fit over the period **1963-07-01** to **2024-09-01**.

## Data Used

The Fama-French factor data was retrieved from [Kenneth French's Data Library](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html). It includes monthly series for the following factors:

- **Mkt-RF**: Market return adjusted for the risk-free rate.
- **SMB**: The difference in returns between small and large companies.
- **HML**: The difference in returns between companies with high and low book-to-market ratios.
- **RMW**: The difference in returns between firms with high (robust) and low (weak) profitability.
- **CMA**: The difference in returns between conservative (low investment) and aggressive (high investment) firms.
- **RF**: The risk-free rate.

## Project Steps

1. **Data Import**:
   - Load the Fama-French factor data from the `F-F_Research_Data_5_Factors_2x3.csv` file.
   - Check for missing values and clean the data if necessary.

2. **Model Estimation**:
   - Decompose portfolio returns based on the five factors.
   - Estimate the coefficients $\beta_i$ for each factor using multiple linear regressions.

3. **Result Analysis**:
   - Check if the estimated coefficients are statistically significant.
   - Validate if $\alpha_i = 0$, indicating that the factors explain the variations in expected returns.

4. **Extended Period Validation**:
   - Repeat the analysis over the period **1963-07-01** to **2024-09-01** to validate the model's robustness.
