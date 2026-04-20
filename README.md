# 🏠 Singapore HDB Resale Price Analysis

An interactive data analysis dashboard exploring **900,000+ HDB resale flat transactions** across Singapore (2000–2024), built with Python, Pandas, Plotly, and Streamlit.

> **Live demo:** [your-app-name.streamlit.app](https://your-app-name.streamlit.app) *(deploy to Streamlit Cloud and update this link)*

---

## Key findings

1. **Location dominates price** — Bukit Timah and Queenstown command a **40–60% premium** over towns like Woodlands and Jurong West for equivalent flat sizes.
2. **Remaining lease strongly predicts price per sqm** — every 10-year drop in remaining lease correlates with roughly 8–12% lower price per sqm.
3. **Post-COVID surge** — median prices dropped ~3% in 2020 then rebounded sharply, reaching all-time highs by 2022 driven by construction delays and pent-up demand.
4. **Executive flats show the widest price spread** — making them the highest-risk, highest-reward flat type depending on location.

---

## Dashboard features

- **KPI cards** — total transactions, median price, avg price per sqm
- **Bar chart** — median resale price ranked by town
- **Line chart** — price trend over time with COVID annotation
- **Scatter plot** — remaining lease years vs price per sqm, coloured by flat type
- **Box plot** — price per sqm distribution by flat type
- **Heatmap** — median price by town × flat type
- **Sidebar filters** — filter by year range, town, and flat type — all charts update live

---

## Project structure

```
sg-hdb-analysis/
├── data/
│   └── resale-flat-prices.csv   # Download from data.gov.sg (not committed)
├── app.py                        # Streamlit dashboard
├── data_loader.py                # Data loading, cleaning & feature engineering
├── charts.py                     # All 5 Plotly chart functions
├── eda.py                        # Exploratory data analysis script
├── requirements.txt
└── README.md
```

---

## How to run locally

**1. Clone the repo**
```bash
git clone https://github.com/Thinzar2003/sg-hdb-analysis.git
cd sg-hdb-analysis
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Download the dataset**

Go to [data.gov.sg](https://data.gov.sg/dataset/resale-flat-prices) → download the CSV → save it as `data/resale-flat-prices.csv`.

**4. (Optional) Run EDA first**
```bash
python eda.py
```

**5. Launch the dashboard**
```bash
streamlit run app.py
```

Open [http://localhost:8501](http://localhost:8501) in your browser.

---

## Deploy to Streamlit Cloud (free)

1. Push this repo to GitHub
2. Go to [streamlit.io/cloud](https://streamlit.io/cloud) → New app
3. Select your repo → set main file to `app.py` → Deploy
4. Add your dataset via Streamlit Secrets or host the CSV in the repo (small file)

---

## Tech stack

| Tool | Purpose |
|------|---------|
| Python 3.10+ | Core language |
| Pandas | Data cleaning & analysis |
| NumPy | Numerical operations |
| Plotly | Interactive charts |
| Streamlit | Web dashboard |

---

## Data source

**HDB Resale Flat Prices** — Singapore Government Open Data  
[https://data.gov.sg/dataset/resale-flat-prices](https://data.gov.sg/dataset/resale-flat-prices)  
Licensed under the [Singapore Open Data Licence](https://data.gov.sg/open-data-licence).

---

## Author

**Thinzar Su Hlaing** — IT Graduate, Data Science & AI  
[GitHub](https://github.com/Thinzar2003) · [LinkedIn](https://linkedin.com/in/thinzarsu)
