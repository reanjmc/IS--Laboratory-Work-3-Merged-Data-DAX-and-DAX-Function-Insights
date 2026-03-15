# Part 1: Review the Merged Dataset - Guide Questions

### 1. Is the dataset in flat-table format?
Yes. All customer and sales information is stored in a single table.

### 2. Which columns describe customers?
CustomerName, City, Region, and CustomerID describe the customer.

### 3. Which columns represent transactions?
OrderID, OrderDate, and SalesAmount represent transactions.


# Part 2: Identify Fact and Dimension Tables - Guide Questions

### 1. Why must dimension tables contain unique keys?
Dimension tables must contain unique keys so that each record represents one entity and relationships work correctly.

### 2. What problems occur if duplicates exist in DimCustomer?
Duplicates can cause incorrect relationships and inaccurate analysis results.


# Part 3: Define Primary & Foreign Keys - Guide Questions

### 1. What is a primary key?
A primary key is a column that uniquely identifies each record in a table.

### 2. Why is CustomerID a foreign key in FactSales?
CustomerID connects the sales records to the customer information in the DimCustomer table.


# Part 4: Create Relationships - Guide Questions

### 1. Why should relationships flow from dimension to fact?
Because dimension tables filter the fact table during analysis.

### 2. What happens if the relationship is Many-to-Many?
It may cause incorrect results and ambiguous relationships.


# PART 5 — Validate the Data Model - Guide Questions

### 1. Did sales aggregate correctly per customer?
Yes, sales were correctly grouped and summed for each customer.

### 2. What would happen if relationships were missing?
The data would not connect properly and calculations would produce incorrect results.


# PART 6 — Introduction to DAX and Guide Questions

## Guide Questions
### 1. What is a DAX measure?
A DAX measure is a calculation used to analyze data in Power BI reports.

### 2. Difference between SUM and AVERAGE?
SUM adds all values together, while AVERAGE calculates the mean value.

### 3. Why use measures instead of calculated columns?
Measures calculate results dynamically based on the report filters.


# PART 7 — DAX Time Intelligence and Guide Questions
## List of DAX formulas
### 1. Total Sales
Total Sales = SUM(FactSales[SalesAmount])
### 2. Total Quantity
Total Quantity = SUM(FactSales[Quantity])
### 3. Average Sales
Average Sales = AVERAGE(FactSales[SalesAmount])

## Guide Questions
### 1. What is time intelligence in DAX?
Time intelligence allows analysis of data across time periods such as months or years.
### 2. Why is a date table required?
A date table is required for time-based calculations and proper time analysis.
### 3. How does PREVIOUSMONTH help analyze trends?
It compares the current month's performance with the previous month.
### 4. What insights can YTD Sales provide?
It shows the total sales accumulated from the beginning of the year until the current date.

# This is a Star Schema.
DimCustomer (1)
      |
      | CustomerID
      |
FactSales
      |
      | OrderDate
      |
DimDate


