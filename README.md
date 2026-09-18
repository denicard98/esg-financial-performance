Impact of ESG Factors on Corporate Financial Performance
==========================================================

MSc thesis (MSc in Business Analytics, ISCTE Business School, 2024-2026), completed in July 2026. Studies the impact of ESG (Environmental, Social, Governance) factors on the financial performance of S&P 500 firms between 2019 and 2023, combining panel econometrics with a machine learning model.

**Status: completed.** Advisor: Dr. Ricardo Joao Lourenco Abreu (ISCTE).

## Objective

To test whether ESG scores (and their E, S and G components) explain variation in firms' financial performance, and to compare the explanatory power of a classic econometric approach with that of a non-linear model.

## Methodology

- Data: panel of S&P 500 firms, 2019-2023 (Refinitiv Eikon), ~500 firms / ~2500 firm-year observations
- Econometric model: fixed-effects panel regression (firm and year fixed effects)
- Machine learning model: Random Forest, to capture non-linear relationships between ESG variables and financial performance
- Dependent variables: Tobin's Q, ROA, ROE
- Tools: Python (pandas, statsmodels, linearmodels, scikit-learn), Google Colab

## Key findings

- Fixed-effects panel models find **no statistically significant linear effect** of ESG (aggregated or by pillar) on Tobin's Q, ROA or ROE, a result that holds with lagged variables and when pillars are analyzed individually
- The **Random Forest** model achieves substantial out-of-sample predictive power (R2 up to 0.55 for Tobin's Q; 0.37 for ROA), clearly outperforming a linear model (OLS) with the same variables — evidence of non-linear relationships that linear models fail to capture
- **Disaggregating by pillar (E, S, G)** consistently outperforms the ESG Combined Score in predictive power
- **Sector-level analysis** reveals opposite-signed effects that cancel out in the average effect: positive and significant in Industrials, negative in Real Estate
- The limited within-firm variation of ESG scores (26% to 52% of total variation, depending on the pillar) helps explain the lack of significance in the fixed-effects models

## Repository structure

```
esg-financial-performance/
├── notebooks/
│   └── Main_AnalysisTese_Organizado.ipynb   # full notebook: data, panel models, regressions, VIF, Random Forest
├── report/
│   └── Dissertacao_Denilson_Cardoso.pdf     # final dissertation
└── README.md
```

## How to reproduce

```
pip install pandas numpy linearmodels statsmodels scikit-learn scipy
jupyter notebook notebooks/Main_AnalysisTese_Organizado.ipynb
```

Note: the data (Refinitiv Eikon, accessed via the ISCTE library) is not redistributed due to licensing restrictions.

---

Academic project — ISCTE Business School, 2024-2026.
