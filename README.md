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

# Exploratory Data Analysis (EDA) – The Look E-Commerce Dataset

The goal of this EDA is to uncover patterns in customer behavior, product performance, and order trends to drive actionable business insights.

---

## 1️⃣ Descriptive Analysis

### Orders Table
- **Order Status:** Majority of orders were **Shipped**, **Completed**, or **Processing**, indicating strong fulfillment performance.  
  **Business Insight:** Monitoring cancellations and failed orders can help reduce lost revenue and improve customer satisfaction.
- **Monthly Trends:** Total orders per month showed a **steady increase over time**, reflecting platform growth.  
  **Business Insight:** Identifies peak periods for staffing, promotions, and inventory planning.
- **Average Items per Order:** 1.45 items per order.  
  **Business Insight:** Opportunities exist to **increase basket size** through product bundling or cross-sell promotions.

### Order Items Table
- **Most Ordered Product:** `product_id 19136` ordered **19 times**.  
  **Business Insight:** Indicates high-demand SKUs; ensure stock availability and consider featuring these products.
- **Top Revenue Product:** `product_id 24428` generated **$1,448** in total sales.  
  **Business Insight:** High-revenue SKUs are critical to profitability; focus on promotions, inventory, and margin optimization.

### Users Table
- **Top Regions:** Guangdong, England, and California had the most users.  
  **Business Insight:** Focus marketing and logistics efforts on high-volume regions to maximize conversion and reduce delivery costs.
- **Average Age:** 41 years.  
  **Business Insight:** Enables targeted marketing campaigns and personalized promotions for the core demographic.
- **Traffic Source Effectiveness:** **Search** drove the highest number of users.  
  **Business Insight:** Invest in top-performing acquisition channels; optimize underperforming channels to increase conversions.

---

## 2️⃣ Diagnostic & Prescriptive Analysis (Section 4)

### Returns by Category

| Category      | Total Returns | Total Sold | Return Rate (%) |
|---------------|---------------|------------|----------------|
| Plus          | 437           | 4,176      | 10.46          |
| Accessories   | 1,033         | 9,926      | 10.41          |
| Shorts        | 1,163         | 11,250     | 10.34          |

**Business Insight:** Certain categories have higher return rates (~10%), which increases costs and reduces margins.  
**Actionable Recommendations:**  
- Investigate product quality, sizing, or marketing issues.  
- Improve product descriptions and sizing guides.  
- Focus promotions on low-return categories to improve profitability.

### High-Margin Products

| Name                                                      | Category           | Avg Margin | Total Sold |
|-----------------------------------------------------------|------------------|------------|------------|
| Darla                                                     | Outerwear & Coats | 594.4      | 10         |
| Nobis Yatesy Parka                                        | Outerwear & Coats | 568.1      | 8          |
| The North Face Apex Bionic Soft Shell Jacket - Men's     | Outerwear & Coats | 539.99     | 3          |

**Business Insight:** High-margin products drive significant profits even if sold in smaller quantities.  
**Actionable Recommendations:**  
- Ensure high-margin SKUs are in stock to avoid lost revenue.  
- Promote these products strategically via bundling, upsells, or featured placements.  
- Monitor inventory closely to capitalize on peak demand.

### Shipping Delays by Region

| State      | Total Orders | Avg Delivery Days |
|------------|--------------|-----------------|
| Okinawa    | 9            | 3.67            |
| Yamaguchi  | 5            | 3.60            |
| Gunma      | 2            | 3.50            |

**Business Insight:** Certain regions experience longer delivery times, affecting customer satisfaction and repeat purchases.  
**Actionable Recommendations:**  
- Reallocate inventory closer to high-demand regions.  
- Optimize logistics and fulfillment routes for efficiency.  
- Consider expedited shipping options or proactive customer communication in slow regions.

---

## 3️⃣ Next Steps
- Conduct **predictive analysis** for demand spikes and late deliveries to optimize inventory and logistics.  
- Build **Power BI dashboards** to visualize trends, KPIs, and actionable insights.  
- Integrate insights into business strategy to improve revenue, operational efficiency, and customer satisfaction.

