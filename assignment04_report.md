# Assignment 04 Interpretation Memo

**Student Name:** [Your Name]
**Date:** [Submission Date]
**Assignment:** REIT Annual Returns and Predictors (Simple Linear Regression)

---

## 1. Regression Overview

You estimated **three** simple OLS regressions of REIT *annual* returns on different predictors:

| Model | Y Variable | X Variable | Interpretation Focus |
|-------|------------|------------|----------------------|
| 1 | ret (annual) | div12m_me | Dividend yield |
| 2 | ret (annual) | prime_rate | Interest rate sensitivity |
| 3 | ret (annual) | ffo_at_reit | FFO to assets (fundamental performance) |

For each model, summarize the key results in the sections below.

--- Only the prime rate shows meaningful predictive power for REIT returns. Rising interest rates hurt REIT's. 

## 2. Coefficient Comparison (All Three Regressions)

**Model 1: ret ~ div12m_me**
- Intercept (β₀): [value] (SE: [value], p-value: [value])
- Slope (β₁): [value] (SE: [value], p-value: [value])
- R²: [value] | N: [value]

**Model 2: ret ~ prime_rate**
- Intercept (β₀): [value] (SE: [value], p-value: [value])
- Slope (β₁): [value] (SE: [value], p-value: [value])
- R²: [value] | N: [value]

**Model 3: ret ~ ffo_at_reit**
- Intercept (β₀): [value] (SE: [value], p-value: [value])
- Slope (β₁): [value] (SE: [value], p-value: [value])
- R²: [value] | N: [value]

*Note: Model 3 may have fewer observations if ffo_at_reit has missing values; statsmodels drops those rows.*

--- Dividend yield and prime rate have negatice slopes. FFO/ Assets has a positive slope although it is insignificant. Prime rate has the smallest standard error. Prime rate is the most relaible predictor with a T value of -6.49. All R-squared values are low. 

## 3. Slope Interpretation (Economic Units)

**Dividend Yield (div12m_me):**
- A 1 percentage point increase in dividend yield (12-month dividends / market equity) is associated with a [slope value] change in annual return.
- [Your interpretation: Is higher dividend yield associated with higher or lower returns? Why might this be?] 

**Prime Loan Rate (prime_rate):**
- A 1 percentage point increase in the year-end prime rate is associated with a [slope value] change in annual return.
- [Your interpretation: Does the evidence suggest REIT returns are sensitive to interest rates? In which direction?]

**FFO to Assets (ffo_at_reit):**
- A 1 unit increase in FFO/Assets (fundamental performance) is associated with a [slope value] change in annual return.
- [Your interpretation: Do more profitable REITs (higher FFO/Assets) earn higher returns?]

--- Lower Returns. This is because dividend yield = dividends/price, so a falling price raises yield while returns suffer. Yes, strongly sensitive, in a negative direction. No, profitable REIT's do not earn higher returns. 

## 4. Statistical Significance

For each slope, at the 5% significance level:
- **div12m_me:** [Significant / Not significant] — [one sentence conclusion]
- **prime_rate:** [Significant / Not significant] — [one sentence conclusion]
- **ffo_at_reit:** [Significant / Not significant] — [one sentence conclusion]

**Which predictor has the strongest statistical evidence of a relationship with annual returns?** [Your answer]

--- Prime rate. The prime rate's t-stat is three times larger than dividend yield's and six times larger than FFO/Assets. It's p value is also pretty much zero. 

## 5. Model Fit (R-squared)

Compare R² across the three models:
- [Your interpretation: Which predictor explains the most variation in annual returns? Is R² high or low in general? What does this suggest about other factors driving REIT returns?]

--- Prime rate explains the most variation but all R squared values are low. R squared is low across all models. REIT return variation is driven by other vactors. 

## 6. Omitted Variables

By using only one predictor at a time, we might be omitting:
- [Variable 1]: [Why it might matter] Omitting market returns means the slope estimates may capture market exposure rather than the true effect of the predictor.
- [Variable 2]: [Why it might matter] Sector-specific factors could be correlated with both dividend yield and returns (e.g., retail REITs may have high yields and poor returns).
- [Variable 3]: [Why it might matter] Larger REITs may have lower yields and more stable returns. Size is likely correlated with all three predictors.

**Potential bias:** If omitted variables are correlated with both the X variable and ret, our slope estimates may be biased. [Brief discussion of direction if possible]

--- If distressed REITs have both high yields and low returns (value trap), omitting distress indicators makes dividend yield appear more negative than its causal effect.

## 7. Summary and Next Steps

**Key Takeaway:**
[2-3 sentences summarizing which predictor(s) show the strongest relationship with REIT annual returns and whether the evidence is consistent with economic theory]

**What we would do next:**
- Extend to multiple regression (include two or more predictors)
- Test for heteroskedasticity and other OLS assumption violations
- Examine whether relationships vary by time period or REIT sector

--- The prime rate shows the strongest and most statistically significant relationship with REIT annual returns (slope = -0.019, p < 0.001), with higher interest rates associated with lower returns — consistent with economic theory that REITs face higher borrowing costs and competition from fixed-income alternatives when rates rise. Dividend yield also shows a significant negative relationship, though weaker, potentially reflecting a "value trap" dynamic rather than a causal effect. FFO/Assets shows no reliable relationship with returns, suggesting that current profitability is already priced into REIT valuations, consistent with market efficiency.

## Reproducibility Checklist
- [ ] Script runs end-to-end without errors
- [ ] Regression output saved to `Results/regression_div12m_me.txt`, `regression_prime_rate.txt`, `regression_ffo_at_reit.txt`
- [ ] Scatter plots saved to `Results/scatter_div12m_me.png`, `scatter_prime_rate.png`, `scatter_ffo_at_reit.png`
- [ ] Report accurately reflects regression results
- [ ] All interpretations are in economic units (not just statistical jargon)
