# 🍫 Awesome Chocolates Sales Dashboard

## 📌 Project Objective

This Power BI dashboard analyzes the sales performance of **Awesome Chocolates**, with a focus on profitability, shipment volume, and sales team/product effectiveness. 

Key objectives include:

- Tracking total sales, cost, profit, and box shipments
- Identifying low box shipments (used as samples)
- Monitoring monthly performance (MoM changes)
- Measuring salespeople and product contribution to profits
- Evaluating profit margins against set targets

---

## 🧠 Key Business Questions

- Are we achieving our monthly sales and profit targets?
- How many shipments fall under "Low Box Shipments" (< 50 boxes)?
- Which salespersons and products are meeting profitability goals?
- What are the trends in cost, profit, and volume over time?

---

## 📊 Dashboard Highlights

| Feature                     | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| ✅ KPI Cards                | Show Total Sales, Cost, Profit, Boxes, and Shipments                        |
| 📈 Dynamic Line Chart       | With a button slicer to toggle between metrics (Sales, Boxes, Cost, etc.)   |
| 🎯 Profit Gauge             | Indicates profit % vs. 60% target                                          |
| 🧪 Low Box Shipment Analysis| Histogram to show shipment volume distribution                             |
| 👤 Salesperson Table        | KPIs by salesperson, with performance indicators                           |
| 📦 Product Table            | KPIs by product, with LBS% and profit tracking                             |

---
![Image](https://github.com/user-attachments/assets/5958eb40-3c32-4066-985f-ae212affd5aa) 
---
## 🛠️ Tools & Technologies Used

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Power Query**
- **Calculation Groups (for dynamic measure switching)**
- **Star Schema Modeling**

---

## 🧮 Key DAX Measures

- `Total Sales`, `Total Profit`, `Total Boxes`, `Total Shipments`
- `Low Box Shipment Count` and `LBS %`
- `Profit %` with conditional indicator (target: 60%)
- `Month-over-Month Change %` for key metrics
- `Latest Date` context variable for dynamic filtering

---

## 🗃️ Data Model

A star schema was used, consisting of:

- **Fact Table:** `Shipments`
- **Dimension Tables:** `Products`, `People`, `Locations`, `Calendar`

**Relationships:**

- `Shipments[Product ID]` → `Products[Product ID]`
- `Shipments[Date]` → `Calendar[Date]`
- `Shipments[Geography]` → `Locations[Geo]`
- `Shipments[Sales Person]` → `People[Sales Person]`

---

## 📈 Analysis Conducted

- Sales and Profitability Trends (MoM %)
- Product-level and Salesperson-level profitability
- Shipment frequency by volume (binning logic)
- Low box shipment identification and tracking
- Performance against profitability target (60%)

---
## 📊 Key Insights

This dashboard revealed several data-driven insights across sales performance, profitability, shipment behavior, and team effectiveness:

### 🔹 1. Sales & Profitability Overview
- The average **profit margin holds steady at ~60%**, meeting the target.
- **Sales and shipments show consistent growth**, with no significant dips.
- **Costs are well-controlled**, not outpacing revenue growth.

### 🔹 2. Month-over-Month (MoM) Performance
- **Lowest Sales**: February 2023 – $2.53M  
- **Highest Sales**: December 2023 – $2.94M  
- **Lowest Profit**: November 2023 – $1.3M  
- **Highest Profit**: December 2023 – $1.8M  
- Monthly trends show stability without sharp fluctuations.

### 🔹 3. Low Box Shipments (LBS) Analysis
- **Top LBS% Salespersons**: Husein Auger (20%), Curtice Advani (19%), Marney O’Breen (16%) , only Marney met the profit target.
- **Top-sampled products** like *50% Dark Bites*, *Eclairs*, and *Mint Chip Choco* had low profitability due to **high product costs**, not due to LBS.
- **No clear correlation** between high LBS% and low profit % , in fact, several high-LBS products maintain strong margins.

### 🔹 4. Sales Team Performance
- **Top performers** by profit %: Marney O’Breen, Kelci Walkden, Van Tuxwell.
- **Underperformers** with high LBS%: Wilone O’Kielt, Mallorie Waber.
- High performers are often selling **high-margin products**, indicating strategic alignment.

### 🔹 5. Product-Level Profitability
- **Most profitable low-volume products**: *Choco Coated Almonds* and *Milk Bars* (76% and 75% profit).
- **No high-volume product** underperforms — demonstrating strong pricing and product strategy.
- LBS does not appear to hinder product conversion or profitability.

### 🔹 6. Shipment Volume Distribution
- **Average shipment size** is ~80 boxes.
- Only **10% of shipments** qualify as low-box (<50), indicating sample distribution is under control.

---

## 📁 Files Included

- `Awesome Chocolates Data.pbix` – Main Power BI report file
- `/assets` – Screenshots of dashboard pages 
- `README.md` – This file

---

## 📌 Key Takeaways

- Built a modular, clean, and dynamic sales dashboard in Power BI
- Applied advanced DAX with calculation groups for interactivity
- Leveraged business rules (LBS < 50) to create meaningful filters
- Designed for decision-makers in product, sales, and operations

---

