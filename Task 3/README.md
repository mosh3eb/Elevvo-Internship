# Task 3: RFM Analysis for Customer Segmentation

## 📊 Project Overview

This project implements a comprehensive RFM (Recency, Frequency, Monetary) analysis on an online retail dataset to segment customers and identify valuable customer groups. RFM analysis is a powerful customer segmentation technique that helps businesses understand customer behavior and optimize marketing strategies.

## 🎯 Objectives

- Perform RFM analysis on online retail transaction data
- Segment customers into meaningful groups based on their purchasing behavior
- Identify high-value customers and those at risk of churning
- Provide actionable insights for customer relationship management

## 📁 Project Structure

```
Task 3/
├── data/
│   └── Online Retail.xlsx          # Source dataset
├── RFM Analysis.ipynb              # Main analysis notebook
└── README.md                       # This file
```

## 🔍 What I Accomplished

### 1. Data Preprocessing
- **Data Cleaning**: Removed records with missing CustomerID and filtered out negative quantities/prices
- **Feature Engineering**: Created `TotalPrice` feature by multiplying `Quantity` and `UnitPrice`
- **Data Quality**: Ensured data integrity for accurate RFM calculations

### 2. RFM Metrics Calculation
- **Recency**: Calculated days since last purchase for each customer
- **Frequency**: Counted unique invoice numbers per customer
- **Monetary**: Summed total spending per customer
- **Reference Date**: Used the day after the last transaction as the reference point

### 3. RFM Scoring System
- **Quantile-based Scoring**: Applied 5-point scale (1-5) for each RFM dimension
- **Score Interpretation**: 
  - Higher Recency scores = more recent purchases
  - Higher Frequency scores = more frequent purchases  
  - Higher Monetary scores = higher spending amounts

### 4. Customer Segmentation
- **RFM Combination**: Created unique RFM segments by combining individual scores
- **Overall RFM Score**: Summed R, F, M scores for comprehensive ranking
- **Business Segments**: Categorized customers into 5 strategic groups:
  - **Champions** (RFM Score ≥ 12): Best customers, high value and loyalty
  - **Loyal Customers** (RFM Score 9-11): Regular customers with good value
  - **Potential Loyalists** (RFM Score 6-8): Customers with growth potential
  - **Needs Attention** (RFM Score 3-5): Customers requiring engagement
  - **At Risk** (RFM Score < 3): Customers likely to churn

### 5. Visualization & Analysis
- **Segment Distribution**: Bar chart showing customer distribution across segments
- **RFM Heatmap**: Visual representation of average RFM values per segment
- **Insights Generation**: Identified patterns and opportunities for each segment

## 🛠️ Technical Implementation

### Key Libraries Used
- `pandas`: Data manipulation and analysis
- `numpy`: Numerical computations
- `matplotlib` & `seaborn`: Data visualization
- `datetime`: Date handling for recency calculations

### Methodology
1. **Data Exploration**: Analyzed dataset structure and quality
2. **RFM Calculation**: Implemented standard RFM methodology
3. **Scoring Algorithm**: Used quantile-based approach for fair distribution
4. **Segmentation Logic**: Applied business rules for customer categorization
5. **Visualization**: Created informative charts for stakeholder communication

## 📈 Key Insights

- **Customer Distribution**: Identified the proportion of customers in each segment
- **Value Patterns**: Discovered relationships between recency, frequency, and monetary values
- **Business Opportunities**: Highlighted segments requiring immediate attention or growth strategies

## 🎯 Business Applications

- **Marketing Strategy**: Tailor campaigns based on customer segments
- **Retention Programs**: Focus on "At Risk" customers to prevent churn
- **Growth Initiatives**: Target "Potential Loyalists" for upselling
- **Resource Allocation**: Prioritize high-value "Champions" segment

## 🚀 Future Enhancements

- Implement dynamic RFM analysis with rolling time windows
- Add predictive modeling for customer lifetime value
- Create automated reporting dashboards
- Integrate with CRM systems for real-time segmentation

## 📊 Results Summary

The RFM analysis successfully segmented customers into actionable groups, providing a foundation for data-driven customer relationship management strategies. The visualization outputs clearly demonstrate the distribution of customer value and behavior patterns across different segments.

---

*This analysis demonstrates proficiency in customer analytics, data preprocessing, and business intelligence techniques essential for modern data science applications.*
