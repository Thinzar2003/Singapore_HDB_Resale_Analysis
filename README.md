# 🏠 Singapore HDB Resale Price Analysis

> Exploratory analysis of 180k+ Singapore HDB resale transactions (2017–2024) using Python, Pandas & Plotly. Interactive charts on price trends, town comparison, lease impact & flat type value.

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?style=flat&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-5.18-3F4F75?style=flat&logo=plotly&logoColor=white)
![Colab](https://img.shields.io/badge/Google%20Colab-Notebook-F9AB00?style=flat&logo=googlecolab&logoColor=white)
![License](https://img.shields.io/badge/Data-Open%20Data%20SG-red?style=flat)

---

## 📌 Project Overview

This project performs an end-to-end exploratory data analysis (EDA) on Singapore's public HDB resale flat transaction data sourced from [data.gov.sg](https://data.gov.sg/collections/189/view).

The goal is to uncover **what drives HDB resale prices** — is it location? flat size? remaining lease? — and present the findings through clear, interactive Plotly visualisations inside a single Google Colab notebook.

---

## 🔑 Key Findings

| # | Finding |
|---|---------|
| 1 | **Location dominates price** — Bukit Timah and Queenstown command a 40–60% premium over towns like Woodlands and Jurong West for equivalent flat sizes |
| 2 | **Remaining lease strongly predicts price/sqm** — every 10-year drop in remaining lease correlates with roughly 8–12% lower price per sqm |
| 3 | **Post-COVID surge** — prices dipped ~3% in 2020 then rebounded to all-time highs by 2022, driven by construction delays and pent-up demand |
| 4 | **Executive flats show the widest spread** — making them the highest-risk, highest-reward flat type depending on location |

---

## 📊 Charts & Analysis

| Chart | Question answered |
|-------|------------------|
| 📊 Bar chart | Which towns have the highest median resale prices? |
| 📈 Line chart | How have prices trended from 2017 to present? |
| 🔵 Scatter plot | Does remaining lease length affect price per sqm? |
| 📦 Box plot | Which flat type gives the best value per sqm? |
| 🗺️ Heatmap | How does price vary across town × flat type combinations? |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.10 | Core language |
| Pandas | Data loading, cleaning & feature engineering |
| NumPy | Numerical operations |
| Plotly Express | Interactive charts |
| Google Colab | Development environment & notebook |

---

## 🚀 How to Run

### Option A — Open directly in Google Colab (recommended)

1. Click the button below to open the notebook in Colab

   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Thinzar2003/Singapore_HDB_Resale_Analysis/blob/main/SG_HDB_Analysis_Colab.ipynb)

2. Download the dataset from [data.gov.sg](https://data.gov.sg/collections/189/view)
   - Choose: **"Resale flat prices based on registration date from Jan-2017 onwards"**
   - Save it as `resale-flat-prices.csv`

3. Run **Cell 2** — upload your CSV when prompted

4. Run all cells: **Runtime → Run all**

---

### Option B — Run locally

```bash
# 1. Clone the repo
git clone https://github.com/Thinzar2003/Singapore_HDB_Resale_Analysis.git
cd Singapore_HDB_Resale_Analysis

# 2. Install dependencies
pip install pandas numpy plotly notebook

# 3. Launch Jupyter
jupyter notebook SG_HDB_Analysis_Colab.ipynb
```

---

## 📁 Repository Structure

```
Singapore_HDB_Resale_Analysis/
│
├── SG_HDB_Analysis_Colab.ipynb   ← Main notebook (all code + charts)
├── README.md                      ← You are here
└── data/
    └── .gitkeep                   ← Download CSV here (not committed)
```

> ⚠️ The dataset CSV is **not included** in this repo due to file size.
> Download it for free from [data.gov.sg](https://data.gov.sg/collections/189/view).

---

## 📂 Dataset

| Field | Detail |
|-------|--------|
| Source | [data.gov.sg](https://data.gov.sg/collections/189/view) |
| Publisher | Housing & Development Board (HDB), Singapore |
| File used | Resale flat prices based on registration date from Jan-2017 onwards |
| Rows | ~180,000+ transactions |
| Period | January 2017 – Present |
| License | [Singapore Open Data Licence](https://data.gov.sg/open-data-licence) |
| Key columns | `month`, `town`, `flat_type`, `floor_area_sqm`, `resale_price`, `remaining_lease` |

---

## ✨ Features engineered

- `price_per_sqm` — resale price ÷ floor area (fairest cross-flat comparison)
- `storey_mid` — numeric midpoint extracted from storey range (e.g. "07 TO 09" → 8.0)
- `remaining_lease_years` — extracted from "61 years 04 months" string format
- `year` — extracted from month column for time-series analysis

---

## 👩‍💻 Author

**Thinzar Su Hlaing** — IT Graduate | Data Science & AI

[![GitHub](https://img.shields.io/badge/GitHub-Thinzar2003-181717?style=flat&logo=github)](https://github.com/Thinzar2003)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/your-linkedin-here)

---

## 📄 License

This project is open source under the [MIT License](LICENSE).
The dataset is published under the [Singapore Open Data Licence](https://data.gov.sg/open-data-licence) by the Housing & Development Board.
