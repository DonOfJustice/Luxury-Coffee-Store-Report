# 📊 Luxury Coffee Store Report – Technical Documentation

![image](https://github.com/user-attachments/assets/95722af4-b5cd-47e8-bdac-2b6b8664df66)


**Project Title:** Luxury Coffee Store Report
**Author:** Donald Njoaguani
**Platform:** Microsoft Excel
**Date Created:** March 21st, 2025
**Version:** v1.0

---

## 🔎 Overview

This dashboard provides a visual summary of a luxury coffee store's key performance indicators (KPIs), including total orders, revenue, customer loyalty engagement, and sales distribution by coffee type, country, and customer. Built entirely in Microsoft Excel using structured tables, formulas, and pivot charts, this report delivers powerful insights in a user-friendly format.

---

## 🛠️ Data Sources

All data was manually entered or imported into structured Excel tables across separate sheets for:

* **Orders**
* **Customers**
* **Products/Coffee Types**
* **Sales Transactions**
* **Monthly Units Sold**
* **Loyalty Status**

---

## 📐 Data Modeling Structure

Excel sheets are connected using *lookup functions* and are logically modeled to emulate a **relational structure**, as follows:

| Table       | Primary Key | Description                              |
| ----------- | ----------- | ---------------------------------------- |
| `Orders`    | Order ID    | Contains order details                   |
| `Customers` | Customer ID | Customer demographics and loyalty status |
| `Products`  | Product ID  | Coffee types and price information       |
| `Sales`     | Order ID    | Line-level transaction data              |
| `Calendar`  | Month       | Time-series breakdown for trend analysis |

---

## ⚙️ Excel Features & Formulas Used

### 1. **Pivot Tables & Pivot Charts**

Used to create interactive visualizations for:

* Sales by country
* Coffee type performance
* Monthly unit trends
* Top customer purchases
* Loyalty segmentation

### 2. **Named Ranges & Structured Tables**

* All raw data is in Excel Tables (`Ctrl + T`) for scalability and easy referencing.
* Named ranges are used for dynamic charts and slicers.

### 3. **Formulas Used**

Key formulas include:

* **Revenue Calculation:**

  ```excel
  =Units_Sold * Unit_Price
  ```

* **Top Customer Ranking:**

  ```excel
  =LARGE(array, k) + INDEX/MATCH for lookup
  ```

* **Loyalty Card Split:**

  ```excel
  =COUNTIF(Customer_Loyalty_Status, "Yes") / Total_Customers
  ```

* **Dynamic Monthly Units:**

  ```excel
  =SUMIFS(Units_Sold, Date_Range, ">=01/"&A1, Date_Range, "<01/"&A2)
  ```

---

## 📈 Visuals Breakdown

| Visualization                        | Purpose                                     |
| ------------------------------------ | ------------------------------------------- |
| **KPI Cards**                        | Highlight Orders, Units, Revenue, Customers |
| **Pie Chart (Loyalty Card)**         | Loyalty segmentation                        |
| **Column Chart (Country Sales)**     | Regional performance                        |
| **Column Chart (Coffee Type Sales)** | Product preference insights                 |
| **Line Chart (Monthly Units)**       | Trend of unit sales                         |
| **Bar Chart (Top Customers)**        | Customer value segmentation                 |

---

## 🎨 Design Choices

* **Color Scheme:** Dark-themed coffee-tone palette for visual branding.
* **Typography:** Clear, readable sans-serif fonts.
* **Layout:** Balanced grid-based layout using grouped shapes and charts.

---

## 🧠 Insights Derived

* U.S. accounts for over 70% of total coffee sales.
* Loyalty program has near-even split (48.7% enrolled).
* Arabica and Excelsa dominate preferences.
* Sales peak in March and May, drop during November–December.

---

## ✅ Conclusion

This Excel-based dashboard project demonstrates how Microsoft Excel can be used to produce high-impact business intelligence solutions with no-code tools. It is ideal for SMEs seeking affordable, interpretable reporting systems.
