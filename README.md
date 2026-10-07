# 📊 Sales Performance & Profitability Analytics | Power BI

An interactive **Power BI Sales Performance Dashboard** designed to analyze multi-year sales performance, profitability, customer behavior, product performance, and geographical sales trends.

The project demonstrates a complete Power BI workflow, including **data preparation with Power Query, data modeling, DAX calculations, time-intelligence analysis, and interactive dashboard development**.

---

## 🎯 Project Aim

The aim of this project is to transform multi-year sales data stored across different Excel tables into a structured and interactive business intelligence dashboard.

The dashboard enables users to:

- Monitor overall sales, costs, and profitability
- Compare business performance across different years and quarters
- Identify high-value customers
- Identify the most profitable products
- Compare sales performance across different counties
- Track Month-to-Date, Quarter-to-Date, and Year-to-Date performance
- Compare current performance with previous-year results
- Explore business performance dynamically using interactive filters

---

## 💼 Business Problem

Sales information is often distributed across multiple datasets containing transactions, customers, products, locations, salespeople, and budget information.

Analyzing these datasets independently makes it difficult to obtain a complete view of business performance.

This Power BI solution consolidates the available data into a structured analytical model and provides an interactive dashboard that allows decision-makers to quickly answer questions such as:

- How much revenue and profit is the business generating?
- Which customers contribute the most revenue?
- Which products generate the highest profit?
- Which geographical areas generate the most sales?
- How is performance changing over time?
- How does current performance compare with the previous year?

---

## 🛠️ Tools & Technologies

- **Microsoft Power BI** – Data modeling, DAX calculations, visualization, and dashboard development
- **Power Query** – Data import, transformation, data-type management, and dataset consolidation
- **DAX (Data Analysis Expressions)** – Business KPIs, profitability calculations, and time-intelligence measures
- **Microsoft Excel** – Source data storage

---

# 📂 Dataset

The project uses an Excel workbook containing transactional sales data and supporting business information.

Rather than using a single flat dataset, the workbook contains separate datasets for sales transactions, customers, products, locations, salespeople, and budgeting.

### Main Tables

| Table | Description |
|---|---|
| **Sales** | Consolidated fact table containing transactional sales records such as Order ID, Customer ID, Product ID, Location ID, Quantity, Price, Purchase Date, and Salesperson ID |
| **Customer_Data** | Customer information used for customer-level sales analysis |
| **Product_Data** | Product information including product details, cost, selling price, discounts, and taxes |
| **Location_Data** | Geographic information including county, state, and location attributes |
| **Salespeople_Data** | Information relating to individual salespeople |
| **Budget_Data** | Budget information used for performance and planning analysis |
| **DimDate** | Dedicated date dimension used for date-based analysis and DAX time-intelligence calculations |

The source workbook also contains separate sales datasets for multiple years, including **2015, 2016, and 2017 sales records**.

---

# 🔄 Data Preparation – Power Query

Power Query was used to import and prepare the Excel data before loading it into the Power BI data model.

The main preparation steps include:

- Connecting Power BI to the Excel workbook
- Importing the required sales and dimension tables
- Assigning appropriate data types
- Preparing customer, product, location, salesperson, and budget datasets
- Consolidating sales records from multiple years
- Creating a unified sales dataset for reporting

### Appending Multi-Year Sales Data

Sales transactions were originally stored separately as:

- `Sales_2015`
- `Sales_2016`
- `Sales_2017`

Power Query was used to append these datasets into a single **Sales** fact table.

Conceptually:

Sales_2015  
↓  
Sales_2016  
↓  
Sales_2017  
↓  
**Consolidated Sales Table**

This provides one centralized transactional dataset that can be analyzed across multiple years.

---

# 🧩 Data Modeling

The project uses a **fact-and-dimension data model** centered around the Sales table.

The **Sales** table contains transactional records, while supporting tables provide descriptive information about customers, products, locations, salespeople, and dates.

### Fact Table

**Sales**

Contains the transactional records used for the majority of sales and profitability calculations.

### Dimension / Supporting Tables

- Customer_Data
- Product_Data
- Location_Data
- Salespeople_Data
- DimDate
- Budget_Data

### Key Modeling Features

- One-to-many relationships
- Centralized Sales fact table
- Separate dimension tables
- Dedicated Date dimension
- Dedicated Key Measures table for organizing DAX calculations
- Relationship-based filtering across dashboard visuals

This structure helps keep the analytical model organized and makes DAX calculations easier to maintain.

### 🗺️ Data Model Preview

![Data Model](Image/Data_Model.png)

---

# 🧮 DAX Measures & Calculations

A dedicated **Key Measures** table is used to organize the DAX calculations used throughout the dashboard.

The measures cover basic aggregation, profitability analysis, comparison metrics, and time-intelligence calculations.

### 💰 Sales & Profitability Measures

| Measure | Purpose |
|---|---|
| **Total Sales** | Calculates total revenue generated from sales transactions |
| **Total Cost** | Calculates the total cost associated with products sold |
| **Total Profit** | Calculates profit after accounting for product costs |
| **Profit Margin** | Measures profit as a percentage of total sales |
| **Average Sales** | Calculates the average sales value |
| **Maximum Sales** | Identifies the maximum sales value |

### 📅 Time-Intelligence Measures

| Measure | Purpose |
|---|---|
| **Sales MTD** | Calculates Month-to-Date sales |
| **Sales QTD** | Calculates Quarter-to-Date sales |
| **Sales YTD** | Calculates Year-to-Date sales |
| **Total Sales LY** | Retrieves previous-year sales for comparison |
| **Total Profit LY** | Retrieves previous-year profit for comparison |
| **Running Sales** | Calculates cumulative sales over time |

### 🔢 Key DAX Concepts

The project demonstrates the use of DAX concepts and functions such as:

- `SUM()`
- `CALCULATE()`
- `DIVIDE()`
- `TOTALMTD()`
- `TOTALQTD()`
- `TOTALYTD()`
- Time-intelligence calculations
- Filter context
- Measure-based calculations
- Cumulative calculations

These measures allow the dashboard to respond dynamically to user selections and provide context-dependent business metrics.

---

# 📊 Dashboard Features

The dashboard combines KPI cards, charts, and interactive filtering to provide an overview of sales and profitability.

## 💳 KPI Cards

The report highlights key business metrics including:

- Total Sales
- Total Cost
- Total Profit
- Profit Margin
- Total Sales Last Year
- Total Profit Last Year

These KPIs provide a quick overview of overall business performance.

---

## 🎛️ Interactive Filters

Users can dynamically explore the dashboard using:

- **Year:** 2015–2018
- **Quarter:** Q1–Q4
- **Reset Button:** Clears selections and restores the default report view

Selections dynamically update the dashboard visuals and KPI calculations.

---

## 📈 Visualizations

| Visualization | Business Purpose |
|---|---|
| **Sales by County** | Compares geographical contribution to overall sales |
| **Sales, Profit & Margin Trend** | Tracks business performance across time |
| **Sales by Customer** | Identifies customers contributing the highest revenue |
| **Profit by Product** | Highlights the most profitable products |
| **Monthly Sales, Profit & Cost Analysis** | Compares revenue, profitability, and costs across months |

Together, these visuals allow users to move from high-level KPIs to more detailed customer, product, geographical, and temporal analysis.

---

# 📌 Dashboard Preview

![Dashboard](Image/Dashboard.png)

---

# 💡 Business Insights

The dashboard provides several useful insights into overall business performance.

### 💵 Revenue Performance

The dataset generated approximately **$26.03M in total sales**, providing a high-level view of overall revenue performance.

### 📈 Profitability

The business achieved an overall **32.52% profit margin**, allowing profitability to be evaluated alongside revenue rather than considering sales alone.

### 🌍 Geographic Performance

County-level analysis highlights which geographical areas contribute the greatest proportion of sales and helps identify differences in regional performance.

### 👥 Customer Analysis

Customer-level analysis identifies the customers generating the highest revenue, helping highlight commercially important customer relationships.

### 📦 Product Performance

Product-level profitability analysis identifies which products contribute most strongly to overall profit.

### 📅 Performance Over Time

Time-intelligence measures allow current sales and profit performance to be compared with previous periods using MTD, QTD, YTD, and previous-year calculations.

---

# 📁 Repository Structure

```text
Sales-Performance-PowerBI/
│
├── README.md
├── Sales Dashboard.pbix
├── Sales Data.xlsx
│
├── Image/
│   ├── Dashboard.png
│   └── Data_Model.png
│
└── Documentation/
    └── DAX Measures.md
