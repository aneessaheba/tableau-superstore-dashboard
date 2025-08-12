# Tableau Project Report – Superstore Sales & Profit Dashboard

**Watch the full tutorial video here:**
[![Watch on YouTube](https://img.youtube.com/vi/SJLmprySalk/hqdefault.jpg)](https://www.youtube.com/watch?v=SJLmprySalk)

---

## Project Overview

This project is designed to demonstrate how to use **Tableau Public** to build an interactive, data-driven dashboard based on real-world retail sales data. The primary goal is to show how raw tabular data can be transformed into meaningful insights using calculated fields, filters, and visual design techniques in Tableau.

---

## Objectives

* Learn the Tableau interface and key functionality
* Perform basic and advanced data visualization using Tableau Public
* Create calculated fields for deeper analysis
* Build a multi-chart interactive dashboard
* Publish and share a professional-quality dashboard

---

## Step 1: Introduction to Tableau

* Discussed Tableau’s purpose: a data visualization and BI tool
* Explained the differences between Tableau Public, Desktop, Online, and Server
* Covered how Tableau connects to various data sources
* Highlighted why Tableau is preferred in industry and academia for data storytelling

---

## Step 2: Dataset Description (Kaggle – Sample Superstore)

* Source: Kaggle
* Format: Excel (.xlsx)
* Key Fields:

  * **Dimensions**: Category, Sub-Category, Region, Segment, Ship Mode, Country, State, City
  * **Measures**: Sales, Profit, Quantity, Discount
* Purpose of dataset: Simulate a retail business’s sales and profit data across locations and product types
* Data imported and previewed in Tableau Public

---

## Step 3: Tableau Public Installation & Setup

* Downloaded Tableau Public (free version from tableau.com)
* Created a Tableau Public account
* Installed and launched Tableau
* Connected to the Excel file and verified data fields and types

---

## Step 4: Creating Calculated Fields

To add analytical depth, we created the following calculated fields:

* **Profit Margin**: `[Profit] / [Sales]`
* **Sales per Quantity**: `[Sales] / [Quantity]`
* **High/Low Discount Flag**: `IF [Discount] > 0.2 THEN "High" ELSE "Low" END`
* **Profit Category Band**:

  ```
  IF [Profit] < 0 THEN "Loss"
  ELSEIF [Profit] < 100 THEN "Low"
  ELSEIF [Profit] < 1000 THEN "Medium"
  ELSE "High"
  END
  ```
* **Profit After Discount**: `[Sales]*(1-[Discount]) - [Sales] + [Profit]`

These fields helped us create dynamic visuals beyond basic aggregations.

---

## Step 5: Visualizations

We developed the following visualizations using Tableau’s drag-and-drop interface, the Show Me panel, and Marks card:

1. **Profit Margin by Sub-Category** – Bar chart with color and label
2. **Sales per Quantity by Segment and Category** – Side-by-side bar chart
3. **Profit Category Distribution** – Pie chart showing records by profit band
4. **Profit Margin vs Sales** – Scatter plot with Sub-Category and Quantity
5. **Profit After Discount by State** – Filled map showing adjusted profit

Features used:

* Filters (Region, Segment)
* Marks Card (Color, Size, Label, Tooltip, Detail)
* Sort, Format, Show Me suggestions

---

## Step 6: Dashboard Development

* Created a new dashboard
* Dragged individual sheets into the layout using Tiled layout mode
* Applied global filters for Region and Segment
* Used 'Use as Filter' feature to link visualizations
* Customized titles, labels, and spacing

Final dashboard includes:

* Visuals grouped by metrics (profit, sales, geography)
* Color-coded values for better readability
* Interactivity via filters and tooltips

---

## Step 7: Publishing

* Saved the workbook as `.twbx`
* Published to Tableau Public under a free account
* Dashboard link is publicly viewable and shareable

View the live dashboard here:
[Tableau Public Dashboard](https://public.tableau.com/app/profile/anees.saheba.guddi/viz/SuperstoreSalesProfitabilityInsights/Dashboard1?publish=yes)

---

## Tools & Resources Used

* Tableau Public
* Excel (Kaggle Dataset)
* GitHub for version control and documentation

---

## Additional Project Files

* `Superstore_Visualizations.twbx` – Full Tableau Workbook
* `Tableau_CheatSheet.pdf` – Reference material on Tableau basics
* `README.md` – This file

---

## Author & Attribution

* Project By: Anees Saheba Guddi
* Platform: YouTube + GitHub
* Focus: Data Visualization, Business Intelligence, Portfolio Building

---

This README serves as a complete project report, useful for instructors, hiring managers, collaborators, or personal documentation. It outlines every step taken in building and sharing a Tableau dashboard from scratch.
