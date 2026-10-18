# Methodology

## `DataScienceEcosystem.ipynb`

A tour notebook, not an analysis: it lists popular data science languages (Python, R, Julia), core libraries (Pandas, NumPy, scikit-learn), common tools (Jupyter Notebook, RStudio, VS Code), and a couple of basic Python arithmetic expressions. It exists to demonstrate familiarity with the ecosystem, not to produce results.

## `CreateandShareyourJupyterNotebook.ipynb` — statistical hypothesis testing

Runs four classic hypothesis tests on the Boston Housing dataset, each at α = 0.05:

| Test | Question | Result |
|---|---|---|
| Independent t-test | Does median home value (`MEDV`) differ for homes bordering the Charles River (`CHAS`)? | p = 0.0001 → reject H₀ (significant difference) |
| One-way ANOVA (`f_oneway`) | Does `MEDV` differ across property age groups? | p ≈ 0.0000 → reject H₀ (significant difference) |
| Pearson correlation | Are industrial land proportion (`INDUS`) and nitric oxide concentration (`NOX`) correlated? | r² = 0.5832 (58.3% of variance explained), p < 0.00000001 → reject H₀ |
| OLS regression | Does distance to employment centers (`DIS`) predict `MEDV`? | R² = 0.0625, p < 0.000001 → statistically significant but explains only ~6% of the variance in home value |

The OLS result is a useful teaching point: statistical significance (a very small p-value, driven by sample size) doesn't imply strong predictive power — `DIS` alone barely explains home value variation, which is why real-world housing models (see `PRODIGY_ML_01` in this author's other repos) use multiple features together.

## `WebScarping.ipynb` — data acquisition

Combines two acquisition methods for the same two tickers (Tesla, GameStop):

1. **`yfinance`**: pulls historical stock price data directly from Yahoo Finance's API.
2. **`requests` + `BeautifulSoup`**: scrapes a quarterly revenue table from an HTML page, since revenue history isn't available through the price API.

Both series are then plotted together per company using interactive Plotly dashboards (price on one axis, revenue on the other) to visually compare stock price movement against underlying revenue trends.
