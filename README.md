# Maven-Electronic-Global-Store
This project delivers a full business intelligence reporting solution designed to help management understand **why revenue has been declining since 2020**, and how different business drivers—products, customers, and stores—contribute to overall performance. 

The solution includes a complete **data model**, automated DAX measures, and four executive-ready dashboards built for decision-making, scenario exploration, and performance tracking.

---

##  Project Overview

The business identified several challenges:
- Revenue has shown a **consistent downward trend** from 2020 onward.
- Management lacked a consolidated view across regions, products, channels, and customer segments.
- There was no single source of truth for monitoring KPIs or understanding performance variations.
- Store-level and customer-level performance differences were hidden in spreadsheets.

**This Power BI solution provides clarity, structure, and visibility**, enabling leaders to answer critical questions such as:
- What is driving the revenue decline?
- Which products and categories are outperforming or underperforming?
- How are customer demographics influencing spending behavior?
- How do newer stores compare to older stores in performance and growth?
- Which regions or customer groups need strategic attention?

---

##  Data Model Architecture

This solution is built on a clean star-schema model:

**Fact Table**
- `Sales` – core transactional dataset containing revenue, quantity, prices, discounts, and associated keys.  

**Dimension Tables**
- `Customers` – demographics, birthdate (used to calculate age & segments), first purchase.
- `Products` – product attributes, category labels, cost & margin reference.
- `Stores` – store metadata, region, open date (used to calculate store age groups).
- `Date` – full calendar table with year, quarter, month, week fields (custom-generated in Power Query).

**Screenshot of the Data Model:**  
![Data Model Screenshot](assets/data_model.png)

---

##  Key DAX Measures

Total Revenue = SUMX(Sales, Sales[Quantity] * Sales[UnitPrice])

Total Profit = [Total Revenue] - [Total Cost]

Profit Margin % = DIVIDE([Total Profit], [Total Revenue])

---

## Dashboard Pages

The report is structured into four executive-focused dashboards, each designed to answer a specific set of business questions while allowing interactive exploration across time, geography, products, customers, and stores.

---

### Trends Dashboard

**Purpose:**  
Provide leadership with a high-level view of overall business performance and revenue direction.

**Key KPIs:**
- Total Revenue
- Total Profit
- Quality Sold
- Customer Count
- Year-over-Year 
  

**Executive Questions Answered:**
- Is revenue improving or declining?
- Are there seasonal patterns or structural drops?
- How does current performance compare year-over-year?

---

### Product Performance Dashboard

**Purpose:**  
Evaluate product-level contribution to revenue and profitability.

**Key KPIs:**
- Total Revenue by Product
- Total Profit by Product
- Profit Margin (%)
- Units Sold


**Executive Questions Answered:**
- Which products drive the most value?
- Which products generate revenue but hurt margins?
- Are there underperforming categories dragging results?

---

### Customer Insights Dashboard

**Purpose:**  
Understand customer behavior, value distribution, and demographic impact on revenue. 

**Key KPIs:**
- Customers Count
- Average Revenue per Customer (ARPU)
- Returning Customers
- Total Revenue


**Executive Questions Answered:**
- Who are the most valuable customers?
- Which customer segments generate the highest revenue?
- How diversified is customer revenue concentration?

Click ![here](/blob/main/Customer Dashboard.png) to view the dashboard

---

###  Store Performance Dashboard

**Purpose:**  
Analyze store contribution, maturity impact, and geographic performance.

**Key KPIs:**
- Revenue per Store
- Profit per Store
- Profit Margin
- Average transaction


**Executive Questions Answered:**
- How do new stores compare to established ones?
- Which regions are over- or under-performing?
- Where should expansion or optimization be focused?

---

##  Executive Summary

This Power BI solution was developed to address declining revenue trends and the lack of a unified performance view across the organization.

The dashboard provides a consolidated, interactive reporting layer that enables leadership to:
- Monitor revenue and profitability trends over time
- Identify top-performing and underperforming products
- Understand customer value distribution and demographics
- Evaluate store performance based on age, region, and contribution

Key findings indicate that revenue decline is driven by a combination of underperforming product categories, regional disparities, and heavy dependence on a small group of high-value customers. Store maturity plays a significant role in revenue generation, with established locations outperforming newer stores.

The final deliverable supports data-driven decision-making and enables management to quickly identify risks, opportunities, and strategic focus areas.

---

##  Deployment & Distribution

The final Power BI report was deployed using best practices for performance, accessibility, and scalability.

**Deployment Steps:**
- Published the PBIX file to Power BI Service
- Configured scheduled data refresh
- Optimized the data model for performance
- Implemented page navigation for a seamless report experience

**Access & Usability:**
- Interactive slicers for time, region, product, and customer segments
- Drill-down and cross-filtering enabled across all visuals
- Report structured for both executive review and analyst exploration

This deployment ensures stakeholders have timely access to reliable insights while maintaining a single source of truth for business performance reporting.

