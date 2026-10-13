> **MoneyWiz CRM · Version 1 (Nov 2025)**: the original Jupyter Notebook data-processing project.
> **Version 2**, a deployed Streamlit CRM with forecasting and segmentation, lives in [MoneyWiz-CRM-NewUpdate](https://github.com/vighnesh-shetty-vs/MoneyWiz-CRM-NewUpdate) ([live app](https://moneywiz-crm-newupdate-bexgwqs8fhq96q5aks7anm.streamlit.app/)).

# 📌 MoneyWiz CRM Data Processing Project

## 📂 Project Overview

This project is part of the **MSc Data Analytics for Business (DAB)**
coursework at **KEDGE Business School**.\
The objective is to build a small-scale **Customer Relationship
Management (CRM)** data processing system named **MoneyWiz**, using
Python and core data-handling concepts.

The project demonstrates: - Reading, transforming, and writing Excel
datasets\
- Cleaning and validating customer records\
- Grouping, summarizing, and visualizing data\
- Basic file operations and helper utilities\
- Automating common CRM-related workflows

All functionalities are implemented using **Jupyter Notebook**,
**Pandas**, and **Matplotlib**.

------------------------------------------------------------------------

## 📁 Repository Structure

    ├── CRM project code.ipynb      # Main Jupyter Notebook with all code
    ├── customers.xlsx              # Sample CRM dataset
    ├── README.md                   # Documentation
    └── /outputs                    # (Optional) Saved plots and processed files

------------------------------------------------------------------------

## 🛠️ Key Features

### 1. Excel I/O Helper Functions

Reusable functions for safe reading/writing of Excel files: -
`read_excel(filename, sheet_name=0)` -
`write_excel(filename, df, sheet_name="Sheet1")`

### 2. Data Cleaning

-   Date format standardization (`DD/MM/YYYY`)
-   Restricting `Returned` values to {0,1,2}
-   Random discount generation (0--5)
-   Replacement of customer names with synthetic names

### 3. Grouping & Summaries

Example:

``` python
result = df[df["StoreLocation"].astype(str) == store]
summary = result.groupby("Product", as_index=False)["TotalPrice"].sum()
```

### 4. Visualizations

Charts generated using Matplotlib: - Product sales\
- Store sales\
- Discount distribution

------------------------------------------------------------------------

## 📦 Requirements

Install dependencies:

``` bash
pip install pandas matplotlib openpyxl
```

------------------------------------------------------------------------

## ▶️ How to Use

1.  Open the notebook\
2.  Load `customers.xlsx`\
3.  Run all cells sequentially\
4.  Export cleaned data using `write_excel()`

------------------------------------------------------------------------

## 👨‍💻 Author

**Vighnesh Shetty**\
MSc Data Analytics for Business\
KEDGE Business School

------------------------------------------------------------------------

## 📜 License

MIT License
