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

