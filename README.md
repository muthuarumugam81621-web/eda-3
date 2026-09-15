# EDAtask3
# 📈 Shopify (SHOP) Stock — Exploratory Data Analysis

Exploratory data analysis of Shopify (SHOP) historical stock price data, covering data cleaning, feature engineering, and visualization of price and volume trends.

## 🔍 Overview

This notebook (`EDAtask3.ipynb`) performs an end-to-end EDA workflow on daily Shopify stock data:

- Loads and inspects the raw dataset
- Cleans missing values and duplicate rows
- Parses and sorts data by date
- Engineers derived financial metrics
- Computes summary statistics
- Visualizes trading volume, price range, and return distribution

## 🗂️ Dataset

- **File:** `SHOP_2015-05-21.csv`
- **Expected columns:** `date`, `open`, `high`, `low`, `close`, `volume`
- The notebook expects the CSV at `/content/SHOP_2015-05-21_2025-03-16 - SHOP_2015-05-21_2025-03-16 (1).csv.xls` (default Google Colab path). Update this path if running locally.

## ⚙️ Workflow

1. **Load & Inspect** — read the CSV, check shape, dtypes, and null counts
2. **Clean** — drop duplicate rows, parse `date` to datetime, drop rows with invalid/missing values, sort and set `date` as the index
3. **Feature Engineering**
   - `Daily_Price_Change` = `close` − `open`
   - `Daily_Return_%` = `(close − open) / open × 100`
   - `Price_Range` = `high` − `low`
4. **Statistics** — descriptive stats, variance and standard deviation of daily returns
5. **Visualization**
   - Trading volume trend over time
   - Distribution of daily returns (histogram)
   - Price range trend over time

## 📦 Requirements

```bash
pip install pandas matplotlib
```

## ▶️ Usage

1. Place `SHOP_2015-05-21.csv` in the working directory (or update the file path in the notebook).
2. Open and run `Task3EDA.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
3. Run all cells sequentially to reproduce the cleaning steps, statistics, and charts.

## 📊 Output

- Console summaries: dataset info, null counts, descriptive statistics, return variance/standard deviation
- Charts: volume trend, daily return distribution, price range trend

<!--
## 🖼️ Sample Charts
Add screenshots of your generated plots here, e.g.:

<img width="1326" height="603" alt="Screenshot 2026-09-11 223244" src="https://github.com/user-attachments/assets/e60d1e20-490a-46f3-9f8d-15943debe36a" />

<img width="1221" height="606" alt="Screenshot 2026-09-11 223300" src="https://github.com/user-attachments/assets/e314da6b-b214-4e0a-8990-9f1d439ec762" />

<img width="1330" height="611" alt="Screenshot 2026-09-11 223314" src="https://github.com/user-attachments/assets/968c68b0-e1c3-460c-bef0-383de6e4899a" />

-->

## 📄 License

Add a license of your choice (e.g., MIT) if distributing this project publicly.
