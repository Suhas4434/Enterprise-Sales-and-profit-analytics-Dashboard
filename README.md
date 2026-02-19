# Enterprise-Sales-and-profit-analytics-Dashboard
End-to-End Business Intelligence Project using Power BI
📌 Project Overview
The Retail Performance Intelligence Dashboard is a complete end-to-end Business Intelligence solution built using Power BI.
This project integrates multiple datasets (Sales, Customers, Products, Returns, and Targets) into a structured Star Schema data model, enabling executive-level performance analysis.

The dashboard provides insights into:
Sales performance
Profitability
Target achievement
Customer segmentation
Product performance
Return rate analysis

🎯 Business Objective
To design and develop a professional BI dashboard that enables stakeholders to:
Monitor revenue and profitability
Compare actual sales vs targets
Analyze performance across regions and segments
Identify high-performing products
Track return rates
Support strategic decision-making

🗂️ Datasets Used
The project uses multiple structured datasets:

1️⃣ Sales Dataset (Fact Table)
OrderID
OrderDate
CustomerID
ProductID
Quantity
SalesAmount
Discount
NetSales
Cost
Profit

2️⃣ Customers Dataset (Dimension)
CustomerID
CustomerName
Segment
Region
Country
SignupDate

3️⃣ Products Dataset (Dimension)
ProductID
ProductName
Category
SubCategory
UnitPrice

4️⃣ Returns Dataset
OrderID
ReturnDate
ReturnReason

5️⃣ Targets Dataset
Year
Month
TargetSales

🧱 Data Modeling (Star Schema)

The data model follows a Star Schema architecture:
Central Fact Table → Sales
Dimension Tables → Customers, Products, Date
Supporting Tables → Returns, Targets
Month-level aggregation handled via MonthTable

Relationship Flow:
Customers →
Products →
DateTable → Sales → Returns
MonthTable → Targets
This structure ensures:
Clean one-to-many relationships
No circular dependencies
Optimized filtering
Proper time intelligence

📐 Data Transformation Steps

Corrected data types (Date, Text, Numeric)
Created DateTable using DAX
Created MonthTable for monthly aggregation
Established proper one-to-many relationships
Ensured consistent granularity (daily vs monthly)
📊 Key Performance Indicators (KPIs)

The dashboard includes the following measures:

🔹 Total Sales
Total Sales = SUM(sales_dataset[NetSales])

🔹 Total Profit
Total Profit = SUM(sales_dataset[Profit])

🔹 Total Orders
Total Orders = DISTINCTCOUNT(sales_dataset[OrderID])

🔹 Profit Margin %
Profit Margin % = DIVIDE([Total Profit], [Total Sales])

🔹 Target Sales
Target Sales = SUM(targets_dataset[TargetSales])

🔹 Sales vs Target %
Sales vs Target % = DIVIDE([Total Sales], [Target Sales])

🔹 Return Rate %
Return Rate % =
DIVIDE(
    COUNT(returns_dataset[OrderID]),
    [Total Orders]
)

📈 Dashboard Features
🔝 Executive KPI Section

Total Sales
Total Profit
Profit Margin
Sales vs Target %
Return Rate %

📊 Performance Analysis
Monthly Sales Trend
Sales by Region
Profit by Category
Top 10 Products by Sales
Segment Distribution

🎛 Interactive Filters
Year
Region
Segment
Category

🛠 Tools & Technologies Used
Power BI Desktop
DAX (Data Analysis Expressions)
Data Modeling (Star Schema)
CSV Data Integration

Time Intelligence Functions
🧠 Key Insights Generated
Identification of top-performing products
Regional revenue comparison
Segment-wise contribution analysis
Monthly sales trend evaluation
Target achievement tracking
Return behavior analysis

🚀 Skills Demonstrated
Data Cleaning & Transformation
Star Schema Modeling
Relationship Management
Advanced DAX Calculations
KPI Development
Executive Dashboard Design
Business Insight Generation

📂 Project Structure
Retail-Performance-Intelligence-Dashboard/
│
├── Data/
│   ├── sales_dataset.csv
│   ├── customers_dataset.csv
│   ├── products_dataset.csv
│   ├── returns_dataset.csv
│   ├── targets_dataset.csv
│
├── Retail_Dashboard.pbix
└── README.md

📌 Future Enhancements
Year-over-Year growth analysis
Customer Lifetime Value calculation
Discount impact analysis
Drill-through customer insights
Forecasting model integration

🏆 Conclusion
This project demonstrates a complete Business Intelligence workflow — from raw data integration to advanced data modeling and executive-level reporting.

It reflects real-world enterprise BI implementation practices and provides actionable insights for strategic business decisions.
