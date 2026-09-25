# Findings — Online Retail Sales Analysis

Scope: January–November 2011; positive-quantity, positive-price, non-cancellation invoice lines.
Sales value excludes the effect of returns and is not profit or net revenue. Exact repeated rows are retained.

1. Included sales total **GBP 9,204,145.72** across **17,582 invoices**.
2. **2011-11** has the highest monthly sales value, **GBP 1,509,496.33**.
3. **United Kingdom** contributes **83.5%** of included sales value.
4. **MEDIUM CERAMIC TOP STORAGE JAR** (code 23166) leads the eligible product codes with **77,826 units**.
5. **Thursday** has the most recorded orders: **3,608**.
6. Mean order value is **GBP 523.50** and the median is **GBP 305.48**.

**Outlier check:** The largest included line contains 74,215 units of stock 23166. There are 1 possible reversal records with matching customer, product, price and opposite quantity. Investigate these before treating the product ranking as demand or making stock decisions.

## Suggested next steps for a business
- Review inventory for the highest-volume products; check stock availability and returns before increasing purchases.
- Compare the busiest month and weekdays with opening hours, promotions and staffing records before changing staffing.
- Investigate dependence on the leading country; compare delivery costs and margins before choosing markets for expansion.

## Limitations
- Historical data from one retailer; some buyers are wholesalers. Results do not represent all online retail.
- Returns/cancellations are excluded instead of reconciled to purchases. No profit, retention or causal claims are made.
- Missing customer IDs are retained for sales analysis. Exact repeated rows may affect totals if they are errors.
- Product-code filtering is a simple heuristic; non-product charges may remain in invoice-level sales totals.
- No cost, stock, promotion or opening-hours data is available. A single year cannot establish recurring seasonality.
- The histogram omits orders above the 95th percentile visually only; all orders remain in summary metrics.
