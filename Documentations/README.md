# 🛒 E-Commerce Sales Dashboard (Excel)
## Build Process & Documentation

This document explains the end-to-end process used to design, model, analyze, and visualize an **E-commerce Sales Dashboard** using Microsoft Excel, Power Query, Power Pivot, and DAX.

The dashboard provides insights into revenue, quantity sold, pricing trends, customer behavior, and store performance over time.

---

## 1. Project Objective

The primary goal of this project was to build a **high-performance Excel dashboard** capable of handling large datasets while delivering clear business insights, including:

- Revenue, quantity, and unit price trends
- Customer performance and growth analysis
- Monthly and geographical sales distribution
- Product, supplier, and store division performance
- Year-over-year (YoY) comparisons

The solution prioritizes **scalability, performance, and clean data modeling**.

---

## 2. Tools & Technologies Used

- Microsoft Excel
- Power Query
- Power Pivot (Data Model)
- DAX (Calculated Measures)
- Pivot Tables & Pivot Charts
- Excel Timelines
- PowerPoint (Dashboard Wireframing)

---

## 3. Data Overview

The project uses a multi-table dataset consisting of approximately **1 million rows** in the fact table.

### Tables Used
- **Fact Table:** Transactions (sales, quantity, unit price)
- **Dimension Tables:**
  - Items
  - Stores
  - Customers
  - Time
  - Transactions
- **Measures Table:** Dedicated table for all calculated measures

To avoid performance issues, all tables were loaded **directly into the data model**, not into worksheets.

---

## 4. Data Import & Performance Optimization

### Import Strategy
- CSV files were imported via **Power Query**
- Data was loaded as **Connections Only**
- Tables were added to the **Excel Data Model**

### Reasoning
- Prevent workbook slowdown
- Efficient handling of large datasets
- Enable Power Pivot and DAX functionality

This approach mirrors real-world enterprise Excel modeling practices.

---

## 5. Data Cleaning & Transformation (Power Query)

### Fact Table
- Validated quantity, unit price, and total price calculations
- Standardized text values (e.g., city abbreviations)
- Ensured numerical consistency across columns

### Dimension Tables
- Fixed inconsistent country naming to support map visuals
- Converted date formats using **Locale settings**
- Removed unnecessary columns
- Standardized customer names
- Extracted month names and abbreviations for reporting

Each transformation focused on ensuring **accurate joins, clean visuals, and reliable aggregations**.

---

## 6. Data Modeling (Power Pivot)

A **star-schema model** was created to support accurate analysis.

### Relationships
- One-to-many relationships from dimension tables to the fact table:
  - Item Key → Items
  - Store Key → Stores
  - Time Key → Time
  - Customer Key → Customers
  - Payment Key → Transactions

Incorrect relationships were identified and corrected during validation, highlighting the importance of **model testing**.

---

## 7. Measure Organization (DAX)

A dedicated **Measures table** was created to:
- Store all KPIs
- Improve model readability
- Centralize business logic

### Core KPIs
- Total Sales
- Total Quantity Sold
- Average Unit Price
- Total Customers

All KPIs were built using DAX for consistency and reusability.

---

## 8. Time Intelligence & YoY Analysis

Year-over-Year analysis was implemented using DAX time intelligence functions.

### Calculations Included
- Previous Year Sales
- Previous Year Quantity
- Previous Year Unit Price
- Previous Year Customers

### YoY Growth Formula
- Calculates percentage change between current and previous periods
- Handles missing data gracefully
- Uses visual indicators (up/down arrows with colors)

This allows stakeholders to quickly understand performance trends.

---

## 9. KPI Formatting & Visual Indicators

Custom number formats were applied to:
- Display millions (M) and thousands (K)
- Show percentage growth with directional arrows
- Improve dashboard readability

Conditional formatting enhances insight delivery without overwhelming users.

---

## 10. Dashboard Wireframing (PowerPoint)

Before building visuals in Excel:
- The dashboard was wireframed in **PowerPoint**
- Shapes and layouts were designed to exact scale
- Colors were sampled using the eyedropper tool
- Navigation structure was planned in advance

The wireframe was then transferred into Excel to ensure:
- Clean alignment
- Consistent spacing
- Professional visual layout

---

## 11. Dashboard Pages Overview

### Page 1 – Sales & Customer Insights
- KPI cards (Sales, Quantity, Unit Price, Customers)
- Monthly sales trends
- Customer growth analysis
- Top 5 customers
- Top products by quantity sold
- Geographic sales distribution
- Timeline slicer for period filtering

### Page 2 – Product & Store Performance
- Top selling products
- Store division performance
- Supplier contribution analysis
- Transaction type analysis
- Weekly sales trends
- Progress bars for comparative performance

Each page is fully interactive and synchronized through the timeline.

---

## 12. Visualization Techniques Used

- Pivot Charts for dynamic aggregation
- Combo charts (Area + Line)
- Stacked bar charts for progress indicators
- Map charts for geographic insights
- Donut charts for distribution analysis
- Linked images to maintain formatting consistency

Visuals were optimized for clarity and storytelling.

---

## 13. Interactivity & Navigation

- Excel Timelines allow filtering across multiple years
- Linked visuals ensure real-time updates
- Page navigation mimics BI dashboard behavior
- Clean transitions between dashboard sections

---

## 14. Final Outcome

The completed dashboard enables users to:
- Track revenue and sales performance over time
- Identify top customers, products, and suppliers
- Compare pricing and quantity trends
- Analyze geographical and divisional performance
- Make data-driven business decisions using Excel

---

## 15. Key Learnings

- Efficient handling of large datasets in Excel
- Importance of proper data modeling
- Power of DAX in Excel analytics
- Value of wireframing before visualization
- Enterprise-style Excel dashboard design

---

## 16. Disclaimer

This project was created for **learning and portfolio purposes** using guided resources.
All transformations, modeling decisions, calculations, and documentation reflect independent analytical understanding.

---

📌 **Author:**  
*Data Analyst Portfolio Project*
