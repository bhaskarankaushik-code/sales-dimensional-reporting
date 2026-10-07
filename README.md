# Sales Dimensional Reporting System

A SQL-based dimensional reporting project built using MySQL.

## Project Overview

This project demonstrates how a sales data warehouse can be designed using a Star Schema and analyzed using advanced SQL techniques.

The project includes:

- Star Schema
- Window Function Ranking
- CTE-based Month-over-Month Analysis
- ROLLUP for Subtotals and Grand Totals
- EXPLAIN for Query Optimization
- Indexing for improved query performance

## Technologies Used

- MySQL 9.3
- MySQL Workbench
- SQL
- Git
- GitHub

## Database Design

The database consists of one fact table and three dimension tables.

### Fact Table

`fact_sales`

Contains:

- sale_id
- date_id
- product_id
- customer_id
- quantity
- amount

### Dimension Tables

`dim_customer`

Contains customer information.

`dim_product`

Contains product information.

`dim_date`

Contains date and time-related information.

## Star Schema

```text
                 dim_customer
                      |
                      |
dim_product ---- fact_sales ---- dim_date