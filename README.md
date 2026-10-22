# E-Commerce Customer Insights Engine | GetIntern Week-02

**Intern:** M. Narendra [mampanarendra246@gmail.com]
**Program:** 8-Week Data Science & ML Track - Phase 1: Data Wrangling & Analytics
**Project:** Week 2 - Merging Tables & Calculating Business Metrics
**Mentor:** Mr. Kalash Jaiswal, Founder & Designated Mentor, GetIntern.in
**Deadline:** October 24, 2026 at 11:59 PM IST

### Objective
To join transactional datasets (`customers.csv` + `orders.csv`) using `pd.merge()` and extract consumer behavior KPIs using `.groupby()` and `.agg()`.

### Core Objectives Implemented
1.  **Relational Joins:** `pd.merge(customers, orders, on=\'customer_id\', how=\'inner\')` and `how=\'left\'`
2.  **Metric Aggregation:** Total spend per customer, AOV, total orders by city/region via `groupby().agg()`
3.  **Cohort Filtering:** Filtered non-converting accounts and created Top 5 Leaderboard

### Dataset Description
- `customers.csv`: 6 customers with customer_id, city, region
- `orders.csv`: 8 orders linked via customer_id
- `merged_inner`: 8 rows (only buyers) | `merged_left`: 9 rows (includes 1 non-buyer - Anjali)

### Top 5 Highest-Spending Customers
| customer_id | customer_name | city | Total_Spend | Order_Count | Average_Order_Value |
|---|---|---|---|---|---|
| 103 | Aman | Mumbai | 13000 | 3 | 4333.33 |
| 101 | Rahul | Mumbai | 12000 | 2 | 6000.00 |
| 105 | Vikash | Delhi | 10000 | 2 | 5000.00 |
| 102 | Priya | Delhi | 3000 | 1 | 3000.00 |

*Generated via `customer_kpi.sort_values(by=\'Total_Spend\', ascending=False).head(5)`*

### City-wise Segmentation
| city | Total_Orders | Total_Revenue |
|---|---|---|
| Mumbai | 5 | 25000 |
| Delhi | 3 | 13000 |

Overall AOV: 4750.00

### Files in Repository
1. `Week2_ECommerce_Insights.ipynb` - Fully executed notebook
2. `customers.csv` - Customer master data
3. `orders.csv` - Order transaction data
4. `top5_customers.csv` - Leaderboard export
5. `README.md` - This file

### How to Run
Open in Google Colab and Run All cells sequentially.

