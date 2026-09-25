# Learn and explain the project

Start by reading the HTML report. Then open the notebook and run one cell at a time.
Read its output before moving on. Allow several study sessions instead of trying to memorize the code.

## Key ideas

| Code | Plain-language meaning |
|---|---|
| pd.read_excel(...) | Load a spreadsheet into a table |
| df.head() | Preview the first five rows |
| df.isna().sum() | Count missing values in each column |
| df[condition] | Select rows that satisfy a rule |
| .copy() | Make a separate table for the next step |
| Quantity * UnitPrice | Calculate a line's sales value |
| groupby(...).sum() | Collect matching rows and add their values |
| nunique() | Count distinct values |
| sort_values() | Put values in order |
| plot(...) | Draw a chart |
| to_csv(...) | Save a table |

## A short explanation you can adapt

"I explored a public online retail dataset using Python. I inspected missing values and repeated records,
selected eleven complete months, and documented how I handled cancellations and invalid quantities.
I grouped the data by month, country and product, and created five charts using Matplotlib.
I checked that the chart totals agreed with the overall sales total and wrote findings with limitations."

Only use this description after you can explain and reproduce the work. Disclose AI assistance when asked.

## Practice tasks

1. Make the country chart show five countries instead of ten.
2. Add a chart for the top five products by sales value.
3. Compare mean and median order value. Explain which you would use to describe a typical order.
4. Write two findings in your own words, including the numbers and the relevant date range.
5. Explain why the dataset cannot establish profit or prove that a proposed action will increase sales.

## CV wording after you understand and personalize the project

**Online Retail Sales Analysis | Python, Pandas, Matplotlib, Jupyter**

- Explored public retail transaction data, documented cleaning rules and analyzed monthly, country and product sales patterns.
- Created five visualizations and validated aggregated sales totals; communicated findings and data limitations in a reproducible notebook.

Do not list SQL or Power BI for this project: they are not used. Do not add invented business-impact percentages.
