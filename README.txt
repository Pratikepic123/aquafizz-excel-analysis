AQUAFIZZ EMPLOYEE COMPLIANCE AND SALES ANALYSIS (EXCEL)
=======================================================

An Excel project for AquaFizz, a health-focused sparkling water startup.
It has two parts:

  1. Employee compliance analysis: checks whether employees meet the
     required working hours.
  2. Sales analysis: studies customer orders to find top customers, cities,
     months and beverages.


DASHBOARD PREVIEW
-----------------
See screenshots/dashboard.png (add a screenshot of the Dashboard sheet).


BUSINESS OBJECTIVES
-------------------
  - Make sure employee working hours comply with company policy.
  - Understand customer behaviour from order data.
  - Identify top-performing products, cities and customers.


TOOLS AND EXCEL SKILLS USED
---------------------------
  - Microsoft Excel
  - Formulas: IF, INT, ROUND, TEXT, VLOOKUP, CONCAT
  - Excel Tables and structured references
  - Pivot Tables, Pivot Charts and Slicers
  - Dashboard design


PART 1: EMPLOYEE COMPLIANCE ANALYSIS
------------------------------------
File: AquaFizz_Employee_Compliance_Analysis.xlsx

Data: 198 records of entry and exit times (Workers Timing dataset,
2019 to 2023).

Rule: the standard working time is 8 hours 30 minutes (8.5 hours), with a
6-minute tolerance.

  Actual working hours : (Exit - Entry) * 24
  Compliance           : "Compliant" if hours >= 8.5 - 0.1, otherwise
                         "Non-Compliant"
  Hours, Minutes       : Actual time split into hours and minutes
  Deviation minutes    : Minutes short of the standard (0 if compliant)
  Message              : Auto-generated note for each non-compliant day

Result: 104 records are compliant and 94 are non-compliant. Non-compliant
days fall short by up to 60 minutes (36 minutes on average).


PART 2: SALES ANALYSIS
----------------------
File: AquaFizz_Employee_Sales_Analysis.xlsx

  Customers   : 2,849 customers with name, email, city and country
  Orders      : 19,929 orders from 2023 with beverage, cost price, selling
                price, profit and margin
  Calculation : 5 pivot tables that feed the dashboard
  Dashboard   : 4 charts with slicers

Calculated columns in Orders: Profit (Selling Price - Cost Price),
Customer City and Customer Name (VLOOKUP from Customers), and Profit margin.

Dashboard charts:
  Top 5 Customers by Sales  : Who spends the most?
  Top Cities by Sales       : Which cities bring in the most revenue?
  Monthly Sales Analysis    : How does profit change month to month?
  Profit Margin by Beverage : Which beverages are the most profitable?

Key numbers:
  - Total sales: about 4.79 million
  - Total profit: about 1.85 million
  - Top city by sales: Sydney
  - Most orders by one customer: Ava Martinez (292 orders)
  - Highest monthly profit: November


REPOSITORY STRUCTURE
--------------------
  aquafizz-excel-analysis/
      AquaFizz_Employee_Compliance_Analysis.xlsx
      AquaFizz_Employee_Sales_Analysis.xlsx
      screenshots/
          dashboard.png
      README.txt


HOW TO USE
----------
  1. Download both .xlsx files.
  2. Open them in Microsoft Excel (pivot tables and slicers work best in
     desktop Excel).
  3. In the sales file, open the Dashboard sheet and use the slicers to
     filter.
  4. In the compliance file, change the working time in cells B3 and C3 to
     test a different policy.


DATA NOTES
----------
  - 9 orders belong to customer IDs that do not exist in the Customers
    sheet, so their city and name show #N/A.
  - "Profit margin" is calculated as (Selling - Cost) / Cost, which is a
    markup. Divide by selling price for a true margin.
  - A few orders have a near-zero cost price, which inflates the average
    profit margin for some beverages.


AUTHOR
------
Pratik
Aspiring Data Analyst | Excel | SQL | Tableau | Python
