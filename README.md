# Analyzing_Motorcycle_Part_Sales

This project analyzes wholesale orders from a motorcycle parts company to calculate net revenue by product line, month, and warehouse—adjusted for payment method fees.

## 📦 Data Summary
- Timeframe: June–August 2021
- Warehouses: North, Central, West
- Payments: Credit card, Transfer, Cash (each with a fee)

Only `Wholesale` orders are included. Net revenue = total – (payment_fee × total).

## 📁 Repo Contents
- `sales_data.csv`: Sample input data
- `analysis_query.sql`: SQL query used for analysis
- `results_output.csv`: Final output format

## 📈 Output Format

| product_line | month | warehouse | net_revenue |
|--------------|-------|-----------|-------------|
| Example      | June  | North     | 12,300.50   |

## 🎯 Purpose
Support decision-making by revealing revenue trends across locations and time.

---

# Analyzing_Motorcycle_Part_Sales
Analyzing sales data for a Company that sells motorcycle parts.

Targeted analysis of wholesale sales data to calculate monthly net revenue by product line and warehouse—adjusting for payment method fees—in order to help stakeholders better understand performance trends and guide strategic decisions.

They operate three warehouses in the area, selling both retail and wholesale. They offer a variety of parts and accept credit cards, cash, and bank transfer as payment methods. However, each payment type incurs a different fee.

To gain a better understanding of wholesale revenue by product line, and how this varies month-to-month and across warehouses. Calculating net revenue for each product line and grouping results by month and warehouse. Filter results so that only `"Wholesale"` orders are included.

Database contains the following table called `sales`:

## Sales
| Column | Data type | Description |
|--------|-----------|-------------|
| `order_number` | `VARCHAR` | Unique order number. |
| `date` | `DATE` | Date of the order, from June to August 2021. |
| `warehouse` | `VARCHAR` | The warehouse that the order was made from&mdash; `North`, `Central`, or `West`. |
| `client_type` | `VARCHAR` | Whether the order was `Retail` or `Wholesale`. |
| `product_line` | `VARCHAR` | Type of product ordered. |
| `quantity` | `INT` | Number of products ordered. | 
| `unit_price` | `FLOAT` | Price per product (dollars). |
| `total` | `FLOAT` | Total price of the order (dollars). |
| `payment` | `VARCHAR` | Payment method&mdash;`Credit card`, `Transfer`, or `Cash`. |
| `payment_fee` | `FLOAT` | Percentage of `total` charged as a result of the `payment` method. |


Query output format:

| `product_line` | `month` | `warehouse` |	`net_revenue` |
|----------------|-----------|----------------------------|--------------|
| product_one | --- | --- | --- |
| product_one | --- | --- | --- |
| product_one | --- | --- | --- |
| product_one | --- | --- | --- |
| product_one | --- | --- | --- |
| product_one | --- | --- | --- |
| product_two | --- | --- | --- |
| ... | ... | ... | ... |



