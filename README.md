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














