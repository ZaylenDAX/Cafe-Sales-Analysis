# Sales Dashboard Project Documentation

## 1. Introduction

This document provides a comprehensive explanation of the design, structure, data transformation steps, and interactive features used to build the Excel Sales Dashboard of a dataset which contains 10,000 rows of synthetic data representing sales transactions in a cafe in 2023. The project demonstrates real-world data cleaning, analysis, and visualization techniques using Excel.

---

## 2. Project Overview

The objective of this project was to explore, clean, transform, and visualize a large sales dataset to produce meaningful insights. A dynamic dashboard was built to allow end users to filter and interact with the data easily.

<img src="Visuals/Screenshot 2025-11-19 204430.png" alt="Image">

### **Key Deliverables**

- Cleaned sales transaction dataset
- Pivot-table based dashboard visuals
- Interactive slicers
- KPI summary cards
- Trend analysis and performance breakdowns

### **Tools Used**

- Microsoft Excel
- Excel PivotTables
- Excel Formulas (XLOOKUP, SUMIFS, TEXT, DATE functions)
- Pivot Charts

---

## 3. Project Structure

- [Dirty Data](https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training?utm_source=chatgpt.com) #Link to the dirty dataset used for the project
- [Clean Data](Data) #.xlsm file containing the cleaned data
- [Visuals](Visuals) #Dashboard screenshot





## 4. Dataset Description

The dataset used for the dashboard consisted of transactional sales data containing the following columns:

- Transaction Date
- Transaction ID
- Item
- Quantity
- Price Per Unit&#x20;
- Total Spent
- Payment Method
- Location

The raw dataset included inconsistencies such as missing values, duplicated rows, inconsistent date formats, and spelling variations that required data cleaning.

---

## 4. Data Cleaning Steps

### **4.1 Remove Duplicates**

Duplicate records were identified and removed using:

- Data → Remove Duplicates
- Conditional formatting to highlight repeated transaction IDs

### **4.2 Handle Missing Values**

- Blank Price per units were replaced using lookup tables
- Missing sales amounts were recalculated as:\
  Total Spent = Quantity \* Price Per Unit

---

## 5. Data Transformation

To prepare the dataset for analysis:

- New calculated columns were added (e.g., Year, Month)
- A Pivot Table was created from the cleaned data

### **5.1 Date Helper Columns**

- Month Name = `TEXT([@Date], "mmmm")`
- Year = `YEAR([@Date])`

---

## 6. Dashboard Design & Wireframe

The dashboard layout was structured as follows:

### **6.1 KPI Section (Top Row)**

- Total Quantity Sold
- Total Order
- Total Sales
- Top Selling Product
- Average Order Value

### **6.2 Main Charts**

- **Line Chart:** Sales trend over time
- **Bar Chart:** Sales by Product, Sales by Day
- **Pie / Donut Chart:** Sales by Payment Method, Sales by Location

### **6.3 Filters**

- Slicers for Year, Location, Payment Method, Item and Month



---

## 7. Interactivity Features

### **Slicers**

Slicers were added to provide quick filtering for:

- Day
- Location
- Payment Method
- Item
- Month

All slicers were connected to each pivot chart/table via the PivotTable Connections menu.

---

## 8. Final Dashboard Features

The completed dashboard allows the user to:

- View overall sales performance
- Track monthly sales trends
- See top-performing products
- Compare sales across locations
- Filter results dynamically using slicers

---

## 9. Challenges Encountered

- Rebuilding missing sales values where totals didn’t match
- Ensuring charts updated dynamically with dropdown filters
- Filtering data using combo box
- Maintaining dashboard performance with a large dataset

---

## 10. Recommendations & Future Improvements

- Add automated data refresh using Power Query
- Migrate the dashboard to Power BI for scalability
- Add forecasting using Excel trendlines
- Implement macros to automate repetitive tasks

---

## 11. Conclusion

This Excel Sales Dashboard project showcases real-world data cleaning, transformation, and visualization skills. The interactive features demonstrate practical analytical abilities that are valuable for business decision-making and suitable for inclusion in a professional portfolio.

