# Online Retail Sales Analysis

A beginner Python portfolio project exploring an online retailer's sales with Pandas and Matplotlib.
The notebook explains each step, from inspecting data quality to interpreting five charts.

## Start here

1. Open **Retail Sales Analysis.html** to read the completed analysis without installing anything.
2. Open **Retail Sales Analysis.ipynb** in Jupyter Notebook to explore and change the code.
3. Read **LEARNING_GUIDE.md** to prepare to explain the work in an interview.

## Questions

- How did sales change by month?
- Which countries contributed the most sales?
- Which products sold the most units?
- Which weekdays recorded the most orders?
- How are order values distributed?

## Run the project

With Anaconda, open Anaconda Prompt and change into this project's folder. Run:

```sh
python -m pip install -r requirements.txt
jupyter notebook "Retail Sales Analysis.ipynb"
```

Select **Restart Kernel and Run All Cells** (wording may vary). Start Jupyter in the project folder so the relative data paths work.
The first data-loading cell may take a minute. No API key or internet connection is needed after installing packages.

## Files

| File or folder | Purpose |
|---|---|
| Retail Sales Analysis.ipynb | Main notebook, with explanations and executed outputs |
| Retail Sales Analysis.html | Readable browser version |
| data/Online Retail.xlsx | Original source dataset |
| charts/ | Five saved PNG charts |
| outputs/findings.md | Calculated findings, suggested actions and limitations |
| outputs/ | Cleaned CSV and summary tables |
| LEARNING_GUIDE.md | Plain-language concepts, exercises and CV wording |

## Analysis choices

Use January–November 2011 so comparisons use complete months. Define sales value as quantity times unit price on
positive-quantity, positive-price, non-cancellation invoice lines. Returns are not subtracted: this is not net revenue or profit.
Missing customer IDs remain eligible for sales totals. Exact repeated rows are retained because no unique line ID proves they are errors.
Count orders by distinct invoice number, not by row. Product rankings use five-digit stock codes with optional letter suffixes;
invoice totals can include charges and other adjustments. The order-value histogram displays values up to the 95th percentile;
all eligible orders remain in the metrics. This project does not measure customer retention or claim business impact.

## Data credit

Chen, D. (2015). *Online Retail* [Dataset]. UCI Machine Learning Repository.
https://doi.org/10.24432/C5BW33

Source: https://archive.ics.uci.edu/dataset/352/online+retail

Original download: https://archive.ics.uci.edu/static/public/352/online%2Bretail.zip

License: Creative Commons Attribution 4.0 International, https://creativecommons.org/licenses/by/4.0/.
The original dataset is redistributed unchanged. Derived tables filter dates and eligible sales lines and add calculated columns.
Original coverage is December 1, 2010–December 9, 2011. Prices are GBP.

## Portfolio use

This is an AI-assisted learning project. Work through it, make your own improvements and describe your contribution accurately.
Do not claim achieved revenue growth or other measured business impact from these descriptive findings.
