# Supply Chain Analytics with SQL (The Look E-commerce Dataset)

## 1. Business Context  
E-commerce companies rely heavily on supply chain efficiency: how fast items are shipped, where inventory is held, and how returns impact revenue. Inefficiencies can lead to higher costs, slower deliveries, or lost sales.  

This project analyzes **The Look E-commerce dataset** (Google BigQuery public data) to uncover actionable insights on fulfillment, returns, distribution centers, and customer purchasing patterns. The work demonstrates how SQL-based analysis can inform **supply chain strategy, demand planning, and customer experience improvements**.

Dataset link: [The Look E-commerce (BigQuery Public Dataset)](https://console.cloud.google.com/marketplace/product/bigquery-public-data/thelook-ecommerce)

---

## 2. Approach  
- **SQL Analysis**: Queries written in BigQuery SQL, organized into descriptive, diagnostic, and strategic insights.  
- **Outputs**: Key tables extracted (top 5–10 rows or aggregated results).  
- **Business Framing**: Each query is connected to a supply chain or business strategy implication.  
- **Visualization**: Outputs are designed for integration into a Power BI dashboard for executive decision-making.  

---

## 3. Analysis & Key Insights  

### 📊 Descriptive Insights (What happened?)  
- **Fulfillment Speed**:  
   - Avg shipping ≈ **1 day**, avg delivery ≈ **2 days** → strong logistics baseline.
   - Delivery time may be a potential bottleneck
- **Distribution Center Processing**:  
   - All DCs process orders in <0.4 days → very lean operations.  
- **Geography of Sales**:  
   - Top demand from **China (Guangdong, Shanghai, Beijing)**, **US (California, Texas, New York)**. and **England**.
- **Order Size by Region**:  
   - Certain small regions (e.g., Iwate, Alaska) show higher items/order, but with low revenue impact.  

### 🔍 Diagnostic Insights (Why did it happen?)  
- **Return Rates**:  
   - Highest return rates in **Jumpsuits & Rompers, Activewear, Jeans** (>10%).  
   - Indicates potential issues in **fit/quality or shipping accuracy**.  
- **Stockouts/Overstocks**:  
   - Many jeans SKUs have **>60% unsold inventory** → over-purchasing or weak demand.  
   - High potential revenue leakage in apparel categories.  
- **Bottleneck Finder**:  
   - Fulfillment: ~36 hrs, Transit: ~59 hrs → main delay comes from **carrier logistics**, not DCs.  

### 🚀 Strategic Insights (What should we do?)  
- **Distribution Center Utilization**:  
   - Memphis, Chicago, Houston handle highest volumes → may risk overload.  
   - Opportunity to **rebalance across underutilized DCs** (e.g., Charleston, Savannah).  
- **Cohort Analysis**:  
   - Some cohorts show **repeat purchases months/years later** → loyalty exists but is **sporadic**.  
   - Targeted retention strategies could smooth this out.
   - Currently present but extremely thin
- **ABC Analysis (Pareto 80/20)**:  
   - Revenue is highly concentrated → top 20% of SKUs (“A”) drive ~80% of revenue.  
   - Focus forecasting, promotions, and inventory prioritization here.  

---

## 4. Deliverables  
- [`sql_queries.sql`](./sql_queries.sql): All queries used in the project.  
- [`query_outputs.md`](./query_outputs.md): Top rows & insights for each query.  

---

## 5. Next Steps  
- **Looker Dashboard**: Build visuals grouped into 3 sections:  
   - Operations (fulfillment speed, bottlenecks, DC performance)  
   - Returns & Inventory (return rates, stock imbalances)  
   - Revenue & Demand (geographic sales, cohorts, ABC analysis)  
- **Business Strategy**:  
   - Revenue is evenly distributed across products → focus inventory planning on breadth, not depth.
   - High return rates in some categories → invest in quality checks or better sizing guides.
   - Customer retention matters → loyalty programs/retention campaigns could drive repeat purchases.
   - Orders are spread across multiple DCs → rebalance inventory placement to reduce shipping times/costs.
   - Seasonal/demand spikes exist → forecasting and demand planning should guide promotions and stock levels. 

---
