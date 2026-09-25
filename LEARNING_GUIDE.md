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

## Why the main methods were chosen

Use this table as a quick revision guide. The notebook and HTML report explain the decisions beside the relevant code.

| Method or decision | Problem it solves | Why this choice fits the project |
|---|---|---|
| Pandas, Jupyter and Matplotlib | Manual analysis of a large file is hard to repeat or review | Read the spreadsheet, summarize tables and show code, charts and explanations together |
| IDs loaded as strings | Identifiers can contain letters and are not measurements | Preserve invoice prefixes and product codes for filtering and grouping |
| Missing-value counts | Unknown data quality can silently affect results | Check every column before deciding which missing values matter |
| Retain unknown customer IDs | Dropping incomplete rows would remove usable sales | Quantity and price are enough for this sales analysis; customer analysis would need a separate rule |
| Inspect and retain repeated rows | Identical lines are not proof of an error | Avoid deleting possibly genuine purchases when there is no unique line identifier |
| Date conversion and complete months | Text dates and partial periods can distort comparisons | Use valid date operations and a continuous January–November 2011 window |
| Explicit sales filters | Purchases, returns and adjustments have different meanings | Define positive-line sales clearly; acknowledge that excluding cancellations does not calculate net revenue |
| Quantity multiplied by price | Units alone do not measure monetary contribution | Convert each included line to a comparable GBP value |
| Distinct invoice counts | One order can have several product lines | Count orders once rather than confusing row count with order count |
| Mean and median order value | An average alone hides the effect of large orders | Report both average spend and the middle order value |
| Monthly grouping and line chart | Transaction detail hides changes over time | Aggregate to an ordered time sequence and make month-to-month changes visible |
| Country totals and horizontal bars | A long category list is difficult to compare | Rank monetary contribution and leave room for readable country labels |
| Stock-code grouping and summed units | Descriptions can vary and rows contain different quantities | Combine the same product identifier and measure volume, not line frequency |
| Product-code pattern filter | Service codes can enter a product ranking | Use a simple documented heuristic while acknowledging possible misclassification |
| Largest-line and reversal check | One unusual or reversed order can dominate a ranking | Investigate a concrete exception before turning a chart into an inventory recommendation |
| Weekday grouping and calendar order | Item counts and alphabetical labels obscure order activity | Count invoices and display Monday through Sunday, including absent groups |
| Histogram and 95th-percentile display cutoff | A mean hides distribution; extremes can compress the visible bulk | Show common order ranges while keeping all orders in the metrics and disclosing omitted values |
| Computed written findings | Manually copied figures can become stale | Insert results from calculation variables directly into the explanation |
| Assertions and total reconciliation | Plausible-looking summaries can still contain mistakes | Confirm that inclusion rules and aggregate totals agree internally |
| CSV, PNG and HTML exports | Reviewers may not run Python | Provide tables, charts and a readable report alongside the reproducible notebook |

## How to explain a choice in an interview

Use this sequence: **problem → chosen method → reason → limitation**.

For example: "Each order has several product lines, so counting rows would overstate the number of orders.
I used `nunique()` on the invoice number to count each order once. The count covers only invoices with lines that meet my sales rules."

Another example: "A few large orders can pull the mean upward. I calculated the median as well to describe the middle order.
Neither measure tells me why customers placed those orders."

Ask yourself whether changing a method would change the question. Ranking products by units answers a volume question;
ranking them by sales value answers a monetary-contribution question. Neither answers profitability without cost data.

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
