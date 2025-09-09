# Task 7 - Data Source Information

## 📊 Dataset: Walmart Sales Forecast

**Source:** [Kaggle Datasets](https://www.kaggle.com/datasets/aslanahmedov/walmart-sales-forecast)

**Creator:** Aslan Ahmedov

## 📋 Dataset Description

This dataset contains historical sales data for Walmart stores, including weekly sales, store information, and various features that could affect sales. The data is perfect for time series analysis, forecasting, and retail analytics.

## 📈 Dataset Characteristics

- **Type:** Time Series, Retail Sales Data
- **Subject Area:** Retail, Sales Forecasting
- **Time Period:** Historical sales data
- **Stores:** Multiple Walmart store locations
- **File Format:** CSV files
- **Features:** Sales data, store info, promotional features

## 📁 Dataset Files

### Core Files
- **train.csv** - Training data with historical sales
- **test.csv** - Test data for validation
- **stores.csv** - Store information and characteristics
- **features.csv** - Additional features affecting sales

## 🔧 Data Structure

### train.csv / test.csv
- **Store** - Store number
- **Dept** - Department number
- **Date** - Week ending date
- **Weekly_Sales** - Sales for the given store and department
- **IsHoliday** - Whether the week is a holiday week

### stores.csv
- **Store** - Store number
- **Type** - Store type (A, B, C)
- **Size** - Store size in square feet

### features.csv
- **Store** - Store number
- **Date** - Week ending date
- **Temperature** - Average temperature in the region
- **Fuel_Price** - Cost of fuel in the region
- **MarkDown1-5** - Anonymized data related to promotional markdowns
- **CPI** - Consumer Price Index
- **Unemployment** - Unemployment rate
- **IsHoliday** - Whether the week is a holiday week

## 📥 How to Download

1. Visit the [Kaggle Dataset Page](https://www.kaggle.com/datasets/aslanahmedov/walmart-sales-forecast)
2. Click "Download" button (requires Kaggle account)
3. Save all CSV files to this directory:
   - `train.csv`
   - `test.csv`
   - `stores.csv`
   - `features.csv`

## 🔑 Kaggle Account Required

- You need a free Kaggle account to download the dataset
- Sign up at [kaggle.com](https://www.kaggle.com) if you don't have an account
- Accept the dataset's terms and conditions

## 🐍 Python Usage

```python
import pandas as pd

# Load datasets
train_df = pd.read_csv('train.csv')
test_df = pd.read_csv('test.csv')
stores_df = pd.read_csv('stores.csv')
features_df = pd.read_csv('features.csv')

# Merge datasets
merged_df = pd.merge(train_df, features_df, on=['Store', 'Date', 'IsHoliday'], how='left')
merged_df = pd.merge(merged_df, stores_df, on='Store', how='left')

# Convert date column
merged_df['Date'] = pd.to_datetime(merged_df['Date'])
```

## 🎯 Analysis Applications

### Time Series Analysis
- **Trend Analysis:** Identify sales trends over time
- **Seasonality:** Detect seasonal patterns in sales
- **Decomposition:** Separate trend, seasonal, and residual components
- **Forecasting:** Predict future sales using various methods

### Retail Analytics
- **Store Performance:** Compare performance across different stores
- **Department Analysis:** Analyze sales by department
- **Holiday Impact:** Study the effect of holidays on sales
- **External Factors:** Impact of temperature, fuel prices, unemployment

### Machine Learning
- **Feature Engineering:** Create new features from existing data
- **Model Training:** Train forecasting models
- **Validation:** Test model performance on test data
- **Ensemble Methods:** Combine multiple models for better predictions

## 📊 Key Insights Potential

- **Seasonal Patterns:** Holiday sales spikes, summer/winter trends
- **Store Type Impact:** Performance differences between store types
- **External Factors:** Weather, economic indicators affecting sales
- **Department Performance:** Which departments drive sales
- **Forecasting Accuracy:** Model performance for future predictions

## 📄 License

This dataset is available under Kaggle's standard terms of use. Please review the specific license terms on the dataset page.

## 🔗 Related Resources

- [Walmart Sales Forecasting Competition](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting)
- [Time Series Analysis Tutorial](https://www.kaggle.com/learn/time-series)
- [Retail Analytics Best Practices](https://www.kaggle.com/discussions)
