# Transaction-PowerBI-Dashboard

**Project Overview:**
This project focuses on building an interactive Power BI dashboard to analyze transaction performance and fraud indicators.
The dashboard provides a clear operational view of transactions, customer activity, device usage, and fraud distribution using enterprise BI best practices.
The dataset used is synthetic/sample data, and the project is designed to demonstrate Power BI development, DAX modeling, and dashboard design skills.

**Objectives:**
Monitor overall transaction performance
Track key business KPIs such as revenue, volume, and customers
Analyze fraud distribution across transaction types
Compare device-level performance and network metrics
Present insights in a corporate, executive-friendly dashboard

**Key KPIs:**
Total Transactions
Total Revenue
Average Transaction Value
Unique Customers
Fraud Transaction Ratio (Sample Data)

**Dashboard Features:**
Interactive KPI cards with dynamic filtering
Transaction distribution by type (Transfer, Deposit, Withdrawal)
Fraud analysis by transaction type and fraud flag
Revenue contribution by device (Mobile vs Desktop)
Network performance analysis using latency vs bandwidth scatter plot
Detailed transaction table for drill-down analysis
Clean, professional layout aligned with enterprise BI standards

**Tools & Technologies:**
Power BI Desktop
DAX (Measures & KPIs)
Power Query (Data Cleaning & Transformation)

**Key DAX Measures:**
Total Revenue =
SUM ( transaction_data[Transaction Amount] )

Total Transactions =
COUNT ( transaction_data[Transaction ID] )

Average Transaction Value =
DIVIDE ( [Total Revenue], [Total Transactions] )

Unique Customers =
DISTINCTCOUNT ( transaction_data[Sender Account ID] )

Fraud Transactions =
CALCULATE (
    COUNTROWS ( transaction_data ),
    transaction_data[Fraud Flag] = TRUE
)

Fraud Transaction Ratio =
DIVIDE ( [Fraud Transactions], [Total Transactions] )

**Data Preparation:**
Cleaned and transformed data using Power Query
Corrected data types for numeric, date, and text fields
Split and processed latitude & longitude values for geo analysis
Ensured model readiness for DAX and performance optimization

**Note on Data:**
This project uses synthetic/sample data
Fraud ratios may appear higher than real-world scenarios
The focus is on logic, modeling, and visualization best practices

**How to Use:**
Download the .pbix file
Open in Power BI Desktop
Explore visuals using slicers and filters
Review DAX measures and Power Query steps
