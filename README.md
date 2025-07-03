# 🚀 Power BI Project: Interactive Economic Insights Dashboard

> **Author**: [Your Name]  
> **Date**: [Insert Date]  
> **Tool Used**: Power BI Desktop  
> **Data Type**: Country-wise Economic Indicators (GDP)  

---

## 🧭 Table of Contents
- [🔍 Project Overview](#-project-overview)
- [📁 Data Sources](#-data-sources)
- [📊 Visualizations Summary](#-visualizations-summary)
  - [1️⃣ KPI Card](#1️⃣-kpi-card-total-gdp)
  - [2️⃣ GDP Table View](#2️⃣-table-view-across-years)
  - [3️⃣ Filled Map](#3️⃣-filled-map-gdp-by-country)
  - [4️⃣ Bubble Map](#4️⃣-bubble-map-multi-indicator-plot)
  - [5️⃣ Bar Chart](#5️⃣-bar-chart-gdp-by-sector)
  - [6️⃣ Matrix Filter](#6️⃣-matrix-filter-panel)
- [🧠 Data Modeling](#-data-modeling)
- [🎨 Design Highlights](#-design-highlights)
- [📈 Key Learnings](#-key-learnings)
- [📷 Screenshots](#-screenshots)
- [🔮 What’s Next](#-whats-next)

---

## 🔍 Project Overview

This interactive dashboard showcases country-level economic metrics, focusing on **GDP analysis** across years, sectors, and indicators using **dynamic visuals and smart filters**.  

The report highlights:
- Key performance indicators (KPI)
- Year-wise matrix breakdowns
- Geographical insights using map visuals
- Sector-based GDP breakdowns

---

## 📁 Data Sources

| Table Name        | Description                          |
|-------------------|--------------------------------------|
| `real_data_Set`   | Main fact table with GDP & other indicators |
| `Countries`       | Lookup table with country names     |
| `Indicators`      | Indicator types (e.g., GDP, GNI, etc.) |
| `Sectors`         | Economic sectors per country        |

✅ **Model Type**: Star Schema  
✅ **Join Logic**:  
- `Countries[Country]` → `real_data_Set[Country]`

---

## 📊 Visualizations Summary

<details>
  <summary>📌 <strong>1️⃣ KPI Card: Total GDP</strong></summary>

- **Visual Type**: Card  
- **Metric**: Sum of `Value`  
- **Filter**: `Indicator = GDP`  
- 🎯 Shows overall GDP in a clean numeric format
</details>

---

<details>
  <summary>📌 <strong>2️⃣ Table View (Across Years)</strong></summary>

- **Visual Type**: Matrix Table  
- **Axis**: Countries × Years  
- **Filter**: `Indicator` (GDP)  
- 📅 Useful for analyzing GDP changes over time by country
</details>

---

<details>
  <summary>📌 <strong>3️⃣ Filled Map: GDP by Country</strong></summary>

- **Visual Type**: Filled Map  
- **Field**: `Country`  
- **Color Legend**: `Value`  
- 🌍 Activated via: `File > Options > Security > Enable Map Visuals`
</details>

---

<details>
  <summary>📌 <strong>4️⃣ Bubble Map: Multi-Indicator Plot</strong></summary>

- **Visual Type**: Bubble Map  
- **Field**: Country (Location), Value (Bubble Size)  
- **Legend**: Indicator  
- 🧠 Helps visualize **GDP vs. other indicators**
</details>

---

<details>
  <summary>📌 <strong>5️⃣ Bar Chart: GDP by Sector</strong></summary>

- **Visual Type**: Clustered Bar  
- **X-Axis**: Sector  
- **Y-Axis**: Sum of GDP `Value`  
- **Filter**: `Indicator = GDP`  
- 🏭 Highlights economic contribution by sectors
</details>

---

<details>
  <summary>📌 <strong>6️⃣ Matrix Filter Panel</strong></summary>

- **Visual Type**: Matrix with Filters  
- **Filter**: `Indicator` Slicer (Basic Filtering)  
- 📊 Foundation for dynamic filtering & dashboard slicing
</details>

---

## 🧠 Data Modeling

✅ **Relationships:**
```text
real_data_Set[Country] ← Countries[Country]
real_data_Set[Indicator] ← Indicators[Indicator]
real_data_Set[Sector] ← Sectors[Sector]
````

✅ **Model Optimization:**

* Only fact table fields exposed in report view
* Lookup tables hidden for a clean data layer
* Ensured **1-to-many relationships** for filter propagation

---

## 🎨 Design Highlights

* 📌 **Consistent color palette** for branding
* 📊 **Aligned visuals** using grid layout
* 🧭 **Filter pane usage** for clarity
* 🌐 **Interactive maps** for geographic storytelling
* 🎛️ **Minimal clutter** – data-to-ink ratio respected

---

## 📈 Key Learnings

* Hands-on practice with:

  * Card, Table, Matrix, Map, and Bar Visuals
* Experience with:

  * Page-level, visual-level, and report-level filters
  * Map activation and configuration in Power BI
* Built a **solid layout and data model** from scratch

---

## 📷 Screenshots

> *(Replace these image links with your actual report screenshots)*

| Dashboard View                                                              | Map Visual                                                      |
| --------------------------------------------------------------------------- | --------------------------------------------------------------- |
| ![Dashboard](https://via.placeholder.com/400x200?text=Dashboard+Screenshot) | ![Map](https://via.placeholder.com/400x200?text=Map+Screenshot) |

---

## 🔮 What’s Next

* 🧠 Add **DAX measures** for YOY growth and averages
* 📆 Use **Time Intelligence functions** to compare over periods
* 🔘 Add **Bookmarks & Buttons** for UX
* 🌐 Publish via **Power BI Service** for web interaction

---

> ✨ *Stay tuned as we expand this into a fully dynamic, business-ready analytics product!*
> 📬 Want the report file or GitHub export version? Let me know and I’ll generate it.

---
