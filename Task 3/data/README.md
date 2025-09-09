# Task 3 - Data Source Information

## 📊 Dataset: Online Retail

**Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail)

**Citation:** Chen, D. (2015). Online Retail [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33.

## 📋 Dataset Description

This is a transactional dataset containing all transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail company. The company mainly sells unique all-occasion gifts, and many customers are wholesalers.

## 📈 Dataset Characteristics

- **Type:** Multivariate, Sequential, Time-Series
- **Subject Area:** Business
- **Instances:** 541,909 transactions
- **Features:** 6 variables
- **Missing Values:** No
- **File Size:** 22.6 MB

## 🔧 Variables

| Variable Name | Type        | Description                                                                                                                       |
| ------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------- |
| InvoiceNo     | Categorical | 6-digit integral number uniquely assigned to each transaction. 'C' prefix indicates cancellation |
| StockCode     | Categorical | 5-digit integral number uniquely assigned to each distinct product                                                              |
| Description   | Categorical | Product name                                                                                                                      |
| Quantity      | Integer     | Quantities of each product per transaction                                                                             |
| InvoiceDate   | Date        | Day and time when each transaction was generated                                                                              |
| UnitPrice     | Continuous  | Product price per unit in sterling                                                                                                            |
| CustomerID    | Categorical | 5-digit integral number uniquely assigned to each customer                                                                      |
| Country       | Categorical | Name of the country where each customer resides                                                                               |

## 📥 How to Download

1. Visit the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail)
2. Click "Download (22.6 MB)" button
3. Save the `Online Retail.xlsx` file to this directory
4. Ensure the file is named exactly `Online Retail.xlsx`

## 🐍 Python Import (Alternative)

```python
from ucimlrepo import fetch_ucirepo

# fetch dataset
online_retail = fetch_ucirepo(id=352)

# data (as pandas dataframes)
X = online_retail.data.features
y = online_retail.data.targets

# metadata
print(online_retail.metadata)
```

## 📄 License

This dataset is licensed under a [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license.

## 🔗 Related Research

**Paper:** "Data mining for the online retail industry: A case study of RFM model-based customer segmentation using data mining"  
**Authors:** Daqing Chen, Sai Laing Sain, Kun Guo  
**Published:** Journal of Database Marketing and Customer Strategy Management, Vol. 19, No. 3, 2012
