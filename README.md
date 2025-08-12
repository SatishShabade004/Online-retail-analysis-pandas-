# **Online Retail Analysis**

## 📌 Project Overview
This project analyzes an **Online Retail** dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail) to extract meaningful business insights.  
The dataset contains transactions from a UK-based online store between **01/12/2010 and 09/12/2011**.

The goal is to:
- Clean and prepare the data for analysis
- Handle missing and invalid values
- Perform exploratory data analysis (EDA)
- Identify sales patterns, customer behavior, and top-performing products
- Generate actionable insights for business decision-making

---

## 📂 Dataset
- **Source:** UCI ML Repository – Online Retail Dataset
- **File:** `Online Retail.xlsx`
- **Rows:** ~500,000 transactions
- **Key Columns:**
  - `InvoiceNo` — Transaction ID
  - `StockCode` — Product code
  - `Description` — Product name
  - `Quantity` — Number of items purchased
  - `InvoiceDate` — Date of purchase
  - `UnitPrice` — Price per item (GBP)
  - `CustomerID` — Unique customer identifier
  - `Country` — Country of purchase

---

## ⚙️ Project Workflow
### **1. Data Loading**
- Loaded the dataset into Pandas from Excel
- Verified data types and structure

### **2. Data Cleaning**
- **Missing Values:**
  - Filled missing product descriptions using the most frequent description for the same StockCode
  - Dropped remaining nulls in `Description`
  - Retained null `CustomerID` values (validated with business context)
- **Invalid Values:**
  - Removed transactions with negative `Quantity` or `UnitPrice`
  - Filtered out cancelled orders (InvoiceNo starting with "C")

### **3. Exploratory Data Analysis (EDA)**
- **Top-selling products** by quantity and revenue
- **Country-wise sales distribution**
- **Monthly sales trends**
- **Customer purchase frequency and value**

### **4. Visualization**
- Used **Matplotlib** for:
  - Sales trends over time
  - Top product charts
  - Country-wise revenue distribution

---

## 📊 Key Insights
- Majority of revenue comes from the UK, but high-value customers exist internationally
- Seasonal peaks observed before Christmas

- Few products contribute disproportionately to total sales (Pareto principle)
- Cancelled orders are concentrated in specific products/customers

---

## 🛠️ Tech Stack
- **Python**: Data processing and analysis
- **Pandas**: Data cleaning and manipulation
- **Matplotlib**: Data visualization
- **Excel**: Source data format

---
