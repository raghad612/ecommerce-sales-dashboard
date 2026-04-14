# 📊 Sales & Revenue Analytics Dashboard — Power BI
### CodeAlpha Internship | Data Analytics | Task 3

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![Task](https://img.shields.io/badge/CodeAlpha-Task%203-blue?style=for-the-badge)

---

## 📌 Project Overview

This is an interactive **Sales & Revenue Analytics Dashboard** built using **Microsoft Power BI** as part of my **Task 3** at the **CodeAlpha Data Analytics Internship**. The dashboard provides a comprehensive view of business performance, covering gross sales, revenue trends, product performance, geographic distribution, and return rates — all in a single, interactive page.

---

## 🎯 Objective

To design a professional, single-page Power BI dashboard that enables business stakeholders to:
- Monitor key financial KPIs at a glance
- Analyze revenue trends over time
- Identify top-performing products
- Understand revenue distribution by country
- Track order volume and return rate

---

## 📂 Dataset

The dataset (`data`) contains retail/e-commerce transactional records with the following key fields:

| Field | Description |
|---|---|
| `InvoiceNo` | Unique invoice/order identifier |
| `InvoiceDate` | Date of the transaction |
| `Description` | Product name/description |
| `Revenue` | Revenue generated per transaction |
| `Gross Sales` | Total gross sales value |
| `Net Revenue` | Revenue after deductions |
| `Country` | Customer's country |
| `Return Rate %` | Percentage of returned orders |

---

## 🛠️ Tools & Technologies

- **Microsoft Power BI Desktop** — Dashboard design & visualization
- **DAX (Data Analysis Expressions)** — Custom measures and calculations
- **Power Query** — Data transformation and cleaning
- **AccessibleOrchid Theme** — Applied for consistent and accessible visual styling

---

## 📊 Dashboard Visuals

The dashboard is built on a **1280 × 720** canvas and includes the following components:

### 🔢 KPI Cards (4 Cards)
| Card | Metric | Description |
|---|---|---|
| 1 | **Gross Sales** | Total gross sales with currency formatting |
| 2 | **Total Orders** | Count of distinct invoices |
| 3 | **Return Rate %** | Percentage of returned transactions |
| 4 | **Net Revenue** | Revenue after returns/deductions |

### 📈 Line Chart — Revenue Trend Over Time
- **X-Axis:** Invoice Date (Date Hierarchy: Year → Quarter → **Month** → Day)
- **Y-Axis:** Sum of Revenue
- Allows drill-down from year level down to individual days
- Shows seasonal trends and revenue growth/decline patterns

### 📊 Clustered Bar Chart — Top 10 Products by Revenue
- **Category:** Product Description
- **Value:** Revenue Volume (custom measure)
- Horizontal bar chart ranked to highlight the best-selling products

### 🍩 Donut Chart — Revenue by Country
- **Legend:** Country
- **Value:** Sum of Revenue
- Visualizes the geographic distribution of revenue across all markets

### 🔽 Slicer — Date Filter
- **Field:** Invoice Date
- Enables dynamic filtering of all visuals by a custom date range
- Makes the entire dashboard interactive and time-period specific

---

## ✨ Key DAX Measures Created

```dax
-- Gross Sales
Gross Sales = SUM(data[Gross Sales])

-- Net Revenue
Net Revenue = [Gross Sales] - [Total Returns]

-- Return Rate %
Return Rate % = DIVIDE([Total Returns], [Gross Sales], 0)

-- Revenue Volume (for Top 10 Products)
Revenue Volume = SUM(data[Revenue])
```

---

## 🔍 Key Insights Enabled

- **Which months drive the highest revenue?** → Line Chart with month-level drill
- **Which products generate the most revenue?** → Top 10 Bar Chart
- **Which countries are the biggest markets?** → Donut Chart breakdown
- **What is the overall business health?** → KPI Cards for Gross Sales, Net Revenue, Return Rate
- **How many transactions were processed?** → Total Orders card

---

## 📁 Repository Structure

```
📦 codealpha-task3-powerbi
 ┣ 📊 task3_codeAlpha_updated.pbix            ← Power BI Dashboard file
 ┣ 📄 README.md            ← Project documentation (this file)
 ┗ 📁 assets/              ← Screenshots of the dashboard (optional)
     ┗ 🖼️ dashboard_preview.png
```

---

## 🚀 How to Open the Dashboard

1. Download and install [**Power BI Desktop**](https://powerbi.microsoft.com/desktop/) (free)
2. Clone or download this repository
3. Open `d2.pbix` in Power BI Desktop
4. Explore the dashboard — use the **Date slicer** to filter by time range

```bash
git clone https://github.com/raghad612/ecommerce-sales-dashboard.git
```

---

## 📸 Dashboard Preview

> *See the demo video on LinkedIn for a full interactive walkthrough!*

---

## 🏅 About This Internship Task

This dashboard was completed as **Task 3** of the **CodeAlpha Data Analytics Internship**. The task required building an end-to-end analytical dashboard using a real-world dataset, applying data cleaning, DAX measure creation, and interactive visualization design.

---

## 🤝 Connect With Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin)]((https://www.linkedin.com/in/raghad-alloush-849093295/))
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=for-the-badge&logo=github)](https://github.com/raghad612)

---

> 💡 *Feel free to fork this repo, explore the dashboard, and reach out if you have any questions!*
