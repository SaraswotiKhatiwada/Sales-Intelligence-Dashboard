---
title: "📊 Sales Dashboard – Power BI Project"
author: "Saraswoti (Sara) Khatiwada Paudel"
date: "`r Sys.Date()`"
output: github_document
---

# 🔹 Problem Statement  
The business was collecting sales data but lacked a consolidated and interactive reporting system.  
Managers were dependent on static spreadsheets, which created challenges in answering fundamental questions:  

- Which products drive profit versus just volume?  
- How do **Direct, Online, and Wholesale** channels compare in performance?  
- Are seasonal peaks being captured effectively, or are opportunities being missed?  
- What are customers’ preferred payment methods (Cash vs. Online)?  

Without timely, interactive visibility into these areas, executives risked reactive decision-making and inefficient resource allocation.  

---

# 🔹 Business Objective  
The objective of this project was to create an **interactive Power BI Sales Dashboard** that addressed executives’ top priorities:  

- ✅ Track KPIs (Total Sales, Profit, Profit %, Volume) in real time.  
- ✅ Highlight **Top 5 Products** and **Top Categories** to sharpen focus.  
- ✅ Compare performance across Sales Channels and Payment Modes.  
- ✅ Detect **monthly** and **daily** sales trends to support proactive planning.  
- ✅ Replace fragmented reporting with a polished, unified dashboard accessible to all stakeholders.  

---

# 🔹 Data & Approach  

## 📂 Data Sources  
- **Input Data** – Transactional sales data including sales value, buying cost, date, product ID, quantity.  
- **Master Data** – Product details, categories, cost, unit of measure.  

## 🔧 Data Preparation (Power Query)  
- Standardized date formats (year, month, day, weekday).  
- Removed nulls and cleaned discount fields.  
- Created a **Date Table** with fields to support time intelligence.  
- Merged Input Data and Master Data for product-level insights.  
- Verified data quality (Quantity × Unit Price = Total Sales).  

## 🏗 Data Modeling  
- Established one-to-many relationships between sales, product, and category tables.  
- Integrated slicers for **Year, Month, Sales Type, Payment Mode** to enable interactive filtering.  

## 📐 DAX (Business Logic)  
- Created measures for **Total Sales, Profit, Profit %**.  
- Implemented TopN and RANKX to extract **Top Products** and **Top Categories**.  
- Built cumulative measures for trend tracking.  
- Applied conditional formatting to flag profitability thresholds.  
- Enhanced user experience with **dynamic tooltips** (e.g., showing Profit %, Sales, Quantity).  

---

# 🔹 Visualizations  

- **KPI Cards** – Snapshot of Total Sales (401K), Profit (69K), Profit % (21%).  
- **Monthly Trend** – Stacked column chart (Sales & Profit) with Profit % line overlay.  
- **Top 5 Products** – Horizontal bar chart highlighting profit drivers.  
- **Sales Channel Comparison** – Donut chart: Direct, Online, Wholesale.  
- **Payment Mode** – Donut chart: Cash vs. Online.  
- **Category Sales Contribution** – Treemap showing dominant categories.  
- **Daily Trend** – Line chart with benchmark average to detect operational fluctuations.  

---

# 🔹 Key Insights  

- **Top 5 Products** contributed ~38% of total sales, creating dependency on a narrow portfolio.  
- **Direct Sales** had the highest transaction volume, while **Online Sales** delivered better margins.  
- **Seasonal Peaks** (March, June, December) showed clear opportunities for campaign alignment.  
- **Category 1 and Category 5** dominated → weaker categories may require rationalization.  
- **Payment Modes** – While Cash remains dominant, **Online payments are growing steadily**, signaling a shift in customer preference.  

---

# 🔹 Business Recommendations  

- Prioritize **Top 5 Products** for stock availability and promotional campaigns.  
- Reallocate resources to strengthen **Online Channels**, where margins are higher.  
- Develop a **seasonal playbook** to capitalize on high-demand months.  
- Rationalize underperforming categories and focus resources on growth drivers.  
- Provide **digital payment incentives** to accelerate adoption and improve operational efficiency.  

---

# 🔹 Tools & Techniques  

- **Power BI** – data modeling, DAX, interactive dashboards.  
- **Power Query** – data cleaning, transformation, integration.  
- **SQL** – validation checks for accuracy.  
- **Excel** – exploratory analysis and KPI validation.  

---

# 🔹 Dashboard Preview  

```{r, echo=FALSE, out.width="80%"}
knitr::include_graphics("images/dashboard.png")
```

*(Screenshot of the Power BI dashboard with KPIs, trends, and category breakdowns)*  

---

# 🔹 Repository Structure  

```
📂 Sales-Dashboard
 ┣ 📜 README.Rmd
 ┣ 📊 SalesDashboard.pbix
 ┣ 📂 data
 ┃ ┣ input_data.csv
 ┃ ┗ master_data.csv
 ┗ 📂 images
    ┗ dashboard.png
```

---

# 🔹 Author  

👩‍💻 **Saraswoti (Sara) Khatiwada Paudel**  
Data Analytics Professional | Power BI | SQL | Python | Tableau  

📌 *This project showcases how raw transactional data can be transformed into actionable insights, enabling smarter business decisions.*  
