# Looker-E-Commerce-Analaysis
A BigQuery + Power BI project analyzing retail sales data to uncover trends, diagnose performance drivers, and predict demand for actionable business impact.

# Data Dictionary
## Data Dictionary

| Table | Key Columns | Notes |
|-------|------------|------|
| users | id, gender, country, state, city | Customer info, can segment revenue by demographics or location |
| orders | order_id, user_id, created_at, shipped_at, status | Track order timing, fulfillment, and returns |
| order_items | order_id, product_id, quantity, sale_price, status | Core for revenue & inventory KPIs |
| products | id, category, brand, retail_price | Product metadata for revenue segmentation, promotions |
| events | event_id, user_id, event_type, event_time | Track user interactions (optional enrichment) |
| inventory_items | inventory_item_id, product_id, distribution_center_id, quantity_on_hand | Track stock levels (optional) |
| distribution_centers | id, name, state, city | Locations for inventory fulfillment |

EDA findings:
DESCRIPTIVE ANALYSIS

Order table:
- majority of orders were shipped, completed, or proccessing
- total orders per month showed a steady increase with respect to time
- avg items per order was 1.45

Order Items table
- product_id 19136 was ordered the most amount of times at 19
- product_id 24428 netted in the most total sales at $1448

Users table:
- Guangdong, England, and California had the most users
- The average age of users was 41
- Search was by far the most effective method of sourcing traffic

- 
