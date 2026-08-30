# Data Science with Python — Lab Notebooks

![CI](https://github.com/Bosaj/Lab-Working-with-files-in-Jupyter-Notebooks/actions/workflows/ci.yml/badge.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Python](https://img.shields.io/badge/python-3.x-blue.svg)

A set of introductory data science labs covering the Python data science ecosystem, statistical hypothesis testing, and web scraping.

## Overview

Three self-contained notebooks from a Python data science coursework track:

| Notebook | Topic |
|---|---|
| [`DataScienceEcosystem.ipynb`](DataScienceEcosystem.ipynb) | Tour of the data science landscape: popular languages (Python, R, Julia), core libraries (Pandas, NumPy, scikit-learn), common tools, and basic Python arithmetic. |
| [`CreateandShareyourJupyterNotebook.ipynb`](CreateandShareyourJupyterNotebook.ipynb) | Statistical analysis of the Boston Housing dataset: exploratory visualizations plus formal hypothesis testing (t-test for Charles River proximity, ANOVA across property age groups, Pearson correlation between industrial land use and pollution, and OLS regression of home value on distance to employment centers). |
| [`WebScarping.ipynb`](WebScarping.ipynb) | Extracting stock price history with `yfinance` and quarterly revenue via web scraping (`requests` + `BeautifulSoup`) for Tesla and GameStop, then visualizing both with interactive Plotly dashboards. |

## Tech Stack

Python, pandas, NumPy, Matplotlib, Seaborn, SciPy, statsmodels, yfinance, Requests, BeautifulSoup4, Plotly.

## Getting Started

### Installation
```bash
pip install -r requirements.txt
```

### Usage
```bash
jupyter notebook
```
Open any of the three notebooks listed above. `WebScarping.ipynb` makes live network requests (Yahoo Finance via `yfinance`, and an HTML table scrape) and needs internet access to run end to end.

## Testing / CI

[`.github/workflows/ci.yml`](.github/workflows/ci.yml) validates the structural integrity of all three notebooks on every push.

## Project Structure

```
Lab-Working-with-files-in-Jupyter-Notebooks/
├── DataScienceEcosystem.ipynb
├── CreateandShareyourJupyterNotebook.ipynb
├── WebScarping.ipynb
└── requirements.txt
```

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## License

This project is licensed under the MIT License — see [LICENSE](LICENSE).

## Author

Oussama EL HADJI — [github.com/Bosaj](https://github.com/Bosaj)


## 📊 Monitoring, Controlling, Evaluation & QA

This project includes a standardized 4-Pillar Observability and QA framework:
- **Logs & Prometheus/Grafana Monitoring**: Configured in `monitoring/` with Prometheus scraper configs and Grafana dashboards.
- **Health Controlling & Evaluation**: Liveness/readiness controllers in `monitoring/health.py` and evaluation harness in `scripts/eval_harness.py`.
- **QA & Testing**: Automated Pytest/Vitest integration and CI workflows via `.github/workflows/ci_qa_monitoring.yml`.

For complete instructions, architecture details, and commands, see [docs/MONITORING_AND_QA.md](file:///C:\Users\ROG FLOW\Desktop\Projects\Github_Projects\Lab-Working-with-files-in-Jupyter-Notebooks\docs\MONITORING_AND_QA.md).
