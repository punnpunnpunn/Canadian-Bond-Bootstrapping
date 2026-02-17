# Canadian Bond Bootstrapping

This repository contains a fixed income term structure analysis project based on Canadian government bond data collected daily from **January 5, 2026, to January 29, 2026**. The project focuses on bootstrapping the term structure, constructing spot and forward curves, and analyzing short-to-intermediate maturity rates via Principal Component Analysis (PCA).

---

## Project Structure

The report is divided into two components:

1. **Fundamental Questions** – Fundamental questions of fixed income and mathematical finance.
2. **Empirical Analysis** – Yield curve construction, spot and forward rates, extraction of 1–5 year rates, and PCA-based factor analysis.

---

## Data

- Source: Canadian government bond market quotes (manually collected)  
- Frequency: Daily, weekdays only  
- Period: Jan 5, 2026 – Jan 29, 2026  
- Instruments: Bonds across multiple maturities  

---

## Methodology

### 1. Bootstrapping the Spot Curve
- Sequentially derive zero-coupon rates from observed bond prices  
- Calculate discount factors and strip implied spot rates  
- Extend recursively to longer maturities  

### 2. Yield Curve Construction
- Compute Yield to Maturity (YTM) and par yields  
- Generate term structure across maturities  

### 3. Forward Rate Calculation
Forward rates are derived from spot rates:

```math
f(t, t+n) = (\frac{(1 + s_{t+n})^{t+n}}{(1 + s_{t})^{t}})^{(\frac{1}{n})} - 1
```

---

## Repository Structure

```
Canadian-Bond-Bootstrapping/
│
├── Report Latex           # Latex of the report
├── data/                  # Collected bond data
├── A1.ipynb               # Jupyter notebooks with analysis
├── Assignment_Details.pdf
├── Report.pdf
└── README.md
```

---

## Tools & Libraries

- Python,
- Pandas,
- Matplotlib,
- Scipy

---

## Author

Punnawit Payapvattanavong
