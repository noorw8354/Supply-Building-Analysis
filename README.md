# 📦 Mega Campaign Supply Optimization Dashboard

## 📊 Project Overview

This project was developed to analyze **product supply and performance across different price buckets and categories** during mega campaigns.  
The main goal was to identify **high-demand but under-supplied segments**, optimize assortment strategy, and support category managers in **data-driven decision-making** to maximize campaign revenue.

The underlying SQL script powered an **automated Power BI dashboard** that combined data from multiple sources to give a unified view of **availability, demand, and sales performance** across key categories.

---

## 🧩 Problem Statement

During large-scale campaigns, product performance heavily depends on maintaining the **right supply levels at the right price points**.  
However, several challenges made this difficult:
- Data scattered across multiple systems (ads, transactions, and catalog data)
- Lack of visibility into **out-of-stock (OOS)** items by price range
- Manual and time-consuming analysis across categories and campaigns

The business needed an automated and scalable approach to **track product availability, conversion trends, and identify missed revenue opportunities** due to supply gaps.

---

## 🧠 Approach

1. **SQL-Based Data Integration**
   - Combined multiple datasets:
     - `ads_drz_prd_assortment_battle_1m` → product visibility & impressions  
     - `dim_drz_prd_sku_core` → catalog-level pricing & category hierarchy  
     - `dwd_drz_trd_core_df` → order-level sales & GMV data  
     - `dwd_drz_trd_cart_ent_di` → add-to-cart behavior  
     - `dws_drz_log_sku_visitor_1d` → traffic & UV data  
   - Joined data at **Month–Category–Price Bucket** level for unified analysis.

2. **Dynamic Price Bucketing**
   - Products were grouped into 250 PKR price intervals (e.g., `0–250`, `251–500`, … `3000+`)  
   - Enabled category-wise performance comparison across price tiers.

3. **Metric Computation**
   - Calculated key KPIs such as:
     - **Live Assortment**, **ATP (Available-to-Promise)**, **Out-of-Stock (OOS)** items  
     - **Impressions**, **Page Views**, **Add-to-Cart (A2C)**, **Orders**, **GMV**, **Unique Visitors (UV)**  
     - **CTR (Click-Through Rate)** and conversion ratios  
   - Aggregated all metrics by **venture_category1–3** and **price bucket** to enable granular insights.

4. **Output View Creation**
   - Final output table `nw_5` served as a **single source of truth** for the dashboard,  
     feeding data directly into Power BI for real-time visualization.

---

## 📈 Key Insights & Impact

Through this analysis, we were able to:
- Identify **price buckets with strong demand but limited assortment**.  
- Highlight **under-supplied SKUs** and **high-performing categories** with unmet potential.  
- Provide **data-backed recommendations** to category and supply teams on where to focus inventory buildup.  
- Enable **proactive supply planning** for future mega campaigns.  

As a result:
- Improved **revenue capture** by optimizing supply allocation.  
- Enhanced **visibility of assortment health** and **category performance** across campaigns.  
- Reduced manual reporting efforts through full dashboard automation.

---

## ⚙️ Tools & Technologies

| Category | Tools Used |
|-----------|-------------|
| **Querying & Data Integration** | SQL (Hive/Presto) |
| **Data Sources** | Ads, Transaction, Catalog, Cart & Visitor Logs |
| **Visualization** | Power BI |
| **Automation** | Scheduled SQL job feeding Power BI model |

---

## 🚀 Business Outcome

- **Data-driven supply planning** during mega campaigns.  
- Clear **visibility into demand vs. supply gaps** at a granular level.  
- Reduced reporting turnaround time from hours to minutes.  
- Helped identify **optimal price buckets** to build assortment and maximize GMV.

---

## 🔒 Confidentiality Note

Due to data privacy and business confidentiality, real datasets, internal dashboards, and performance figures are not shared.  
This documentation focuses on the **approach, logic, and analytical impact** of the project.

---

## 👤 Author

**Noor Wali**  
Expert Data Analyst – Daraz (Alibaba Group)  
[LinkedIn](https://www.linkedin.com/in/your-link) | [GitHub](https://github.com/noorw8354)

---

### 🔖 Tags
#Daraz #SQL #PowerBI #MegaCampaign #AssortmentAnalytics #DataDrivenDecisions  
#GMV #EcommerceAnalytics #PriceBuckets #Automation #DataIntegration #CategoryOptimization
