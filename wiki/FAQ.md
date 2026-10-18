# FAQ

**Are these three notebooks related to each other?**
Not directly — they're independent labs from the same coursework track, grouped in one repository because they share the "working with files/data in Jupyter" theme. Each can be read and run on its own.

**Where does the Boston Housing dataset come from, and is it still recommended for use?**
It's the classic Boston Housing dataset commonly bundled with older versions of scikit-learn (it was later removed from scikit-learn due to ethical concerns about one of its features). It's used here purely as a teaching dataset for hypothesis testing, not as a modeling recommendation.

**Why does `WebScarping.ipynb` sometimes fail to run?**
It depends on Yahoo Finance's API (via `yfinance`) and scrapes a live HTML page for revenue data. Either can break without warning if the upstream site changes its structure or rate-limits requests — this is a known fragility of any live web-scraping notebook, which is why CI only checks its structure rather than executing it.

**What's the practical takeaway from the OLS regression result?**
A statistically significant p-value (rejecting the null hypothesis) doesn't mean the predictor is practically useful — `DIS` alone explains only about 6% of the variance in home value (R² = 0.0625), so distance to employment centers is a weak standalone predictor of price.

**Do I need an API key for `yfinance`?**
No, `yfinance` scrapes public Yahoo Finance data without requiring authentication.

**Does CI execute any of the notebooks?**
No — it only validates that all three `.ipynb` files are structurally well-formed JSON/notebook documents, so it catches corrupted notebooks but not broken cells or runtime errors.
