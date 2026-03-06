# Épiphanie Boutique – Sales and Product Performance Analysis

## Project Overview

This project analyzes sales data from **Épiphanie Boutique**, a small retail business that sells **shoes, bags, accessories, and beauty products**. The business originally operated as an **online store**, and later expanded to include a **physical retail location**.

The goal of this analysis is to transform raw business data into **actionable insights** that help answer key business questions such as:

- Which products generate the most revenue?
- What are the best-selling product categories?
- How are sales distributed across categories?
- What are the profit margins across products?
- Did opening a **physical store** change sales performance?

This project demonstrates practical skills in **data cleaning, data merging, exploratory analysis, and business analytics using Python**.

---

# Business Questions

The analysis focuses on answering the following questions:

1. **Which items are the best-selling products?**  
2. **How are sales distributed across product categories?**  
3. **What are the revenue and profit trends over time?**  
4. **Which categories contribute the most to overall revenue?**  
5. **Did opening a physical store change the volume of sales?**

---

# Data Sources

The analysis uses two datasets exported from the Shopify store.

## 1. Products Dataset

Contains information about each product and its variants.

Key variables include:

- Product title
- Vendor
- Product type
- Variant SKU
- Variant price
- Inventory quantity
- Cost per item

Because Shopify stores **variants as separate rows**, the dataset required additional cleaning to reconstruct product-level information.

---

## 2. Orders Dataset

Contains transaction-level data including:

- Order ID
- Product title
- Quantity sold
- Total price
- Order date

This dataset represents the **actual customer purchases**.

---

# Data Cleaning and Preparation

Several preprocessing steps were required before performing the analysis.

## Product Data Cleaning

Key steps included:

- Selecting relevant columns
- Filling missing values using forward filling
- Harmonizing product types into standardized categories

Example business categories created:

- Shoes
- Bags
- Accessories
- Beauty
- Make Up

This step ensures that products can be analyzed at a **higher business category level**.

---

## Creating a Matching Product Key

To merge the product dataset with the order dataset, a **clean product identifier** was created.

Product titles were standardized by:

- converting to lowercase
- removing variant information
- removing parentheses
- trimming spaces


This allowed consistent matching between product and order records.

---

## Merging Product and Order Data

Once standardized titles were created, the datasets were merged so that each order could be linked with:

- product category
- cost per item
- inventory information

This enabled calculation of **revenue, cost, and profit**.

---


## Monthly Aggregation

Sales data was aggregated by month to analyze business performance over time.

Example metrics computed:

- Monthly revenue
- Monthly cost
- Monthly profit
- Number of orders

---

## Store Opening Indicator

The boutique opened a **physical store in August 2025**.

We use comparison of:

- sales **before the store**
- sales **after the store**

---

# Key Insights

## Product Performance

The analysis identifies the **best-selling products** by:

- revenue
- quantity sold

This helps guide **inventory decisions and restocking priorities**.

---

## Category Sales Distribution

Sales were grouped into broader categories such as:

- Shoes
- Bags
- Accessories
- Beauty

This helps determine which product categories drive the majority of revenue.

---

## Revenue and Profit Trends

Monthly analysis shows:

- fluctuations in sales over time
- strong relationship between revenue and profit
- relatively stable margins across months

---

## Impact of Opening the Physical Store

By comparing sales **before and after August 2025**, the analysis explores whether opening a retail location increased overall sales.

This type of analysis resembles a **simple business impact evaluation**, similar to what companies use when measuring the effect of a new store or product launch.

