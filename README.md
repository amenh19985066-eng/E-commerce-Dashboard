
```markdown
 📊 E-Commerce Business Performance Dashboard

Project Overview
This interactive Power BI dashboard provides a comprehensive analysis of sales, profits, and customer distribution for an e-commerce platform. The project focuses on transforming raw data into actionable business insights, helping stakeholders understand profitability drivers and customer behavior.

---

Key Insights & Business Value
  **Profitability vs. Sales:** Discovered that while **Electronics** drives the highest sales volume, **Clothing** yields a higher net profit margin.
  **Product Performance:** Identified **Printers** as the top profit-generating sub-category, whereas **Electronic Games** showed underperformance.
  **Geographical & Payment Analysis:** Tracked order distributions across cities and analyzed preferred payment modes to optimize marketing and logistics.

---

🛠️ Technical Skills Applied
  **Data Modeling:** Established proper relationships between primary data tables and summary tables to avoid visualization conflicts.
  **Time-Series Sorting:** Resolved chronological sorting issues by binding text months to numerical values using the `Sort by Column` feature.
  **UI/UX Dashboard Design:** Developed a polished, modern interface featuring rounded container cards and a dedicated sidebar for intuitive filtering.

---

 🧮 DAX Measures Used

To calculate the monthly sales and growth rates accurately, the following DAX measures were created:

Current Month Sales:
  ```dax
  Current Month Sales = SUM(Sales_Summary_Table[Sales])

```
Previous Month Sales:
   ```dax
   Previous Month Sales = 
   CALCULATE(
       SUM(Sales_Summary_Table[Sales]), 
       DATEADD(Sales_Summary_Table[Date], -1, MONTH)
   )
   
   ```
Growth Rate %:
   ```dax
   Growth Rate % = 
   DIVIDE(
       [Current Month Sales] - [Previous Month Sales], 
       [Previous Month Sales], 
       0
   )
   
   ```
 Dashboard Preview
 1. Financial & Product Performance Page
<img width="1643" height="858" alt="Screenshot 2026-06-28 181328" src="https://github.com/user-attachments/assets/a732ce70-0190-4577-9515-cb986a61a364" />
<img width="1612" height="848" alt="Screenshot 2026-06-28 181347" src="https://github.com/user-attachments/assets/3eab9730-e366-4dd1-a644-e56c1082405c" />
<img width="1597" height="862" alt="Screenshot 2026-06-28 181401" src="https://github.com/user-attachments/assets/e3d55ac1-fa29-4499-b62d-54cd977c81d6" />


 2. Customers & Geography Page
<img width="1658" height="831" alt="Screenshot 2026-06-28 181305" src="https://github.com/user-attachments/assets/24874f9a-eb9c-4d5b-ba35-f9364a4c8e37" />


```

`
