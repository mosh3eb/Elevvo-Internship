# Task 5 - Data Source Information

## 📊 Dataset: Chinook Database

**Source:** [Kaggle Datasets](https://www.kaggle.com/datasets/ranasabrii/chinook)

**Creator:** Rana Sabrii

## 📋 Dataset Description

The Chinook database is a sample database representing a digital music store. It contains information about artists, albums, tracks, customers, employees, invoices, and sales. This database is perfect for learning SQL and understanding database relationships in a real-world context.

## 📈 Database Characteristics

- **Type:** Relational Database (SQLite)
- **Subject Area:** Music Store, E-commerce
- **Tables:** 11 tables with relationships
- **File Format:** .sqlite (SQLite database)
- **Size:** Small to medium (sample data)

## 🗃️ Database Schema

### Core Tables
- **artists** - Music artists information
- **albums** - Album details linked to artists
- **tracks** - Individual songs with album and genre info
- **genres** - Music genre classifications
- **media_types** - Media format types (MP3, MP4, etc.)

### Business Tables
- **customers** - Customer information and contact details
- **employees** - Store employee information
- **invoices** - Sales transaction records
- **invoice_lines** - Individual line items for each invoice

### Supporting Tables
- **playlists** - Customer playlist information
- **playlist_track** - Many-to-many relationship between playlists and tracks

## 📥 How to Download

1. Visit the [Kaggle Dataset Page](https://www.kaggle.com/datasets/ranasabrii/chinook)
2. Click "Download" button (requires Kaggle account)
3. Save the `Chinook_Sqlite.sqlite` file to this directory
4. Ensure the file is named exactly `Chinook_Sqlite.sqlite`

## 🔑 Kaggle Account Required

- You need a free Kaggle account to download the dataset
- Sign up at [kaggle.com](https://www.kaggle.com) if you don't have an account
- Accept the dataset's terms and conditions

## 🐍 Python Usage

```python
import sqlite3
import pandas as pd

# Connect to database
conn = sqlite3.connect('Chinook_Sqlite.sqlite')

# Query data
query = "SELECT * FROM tracks LIMIT 5"
df = pd.read_sql_query(query, conn)

# Close connection
conn.close()
```

## 🎯 Learning Objectives

- **SQL Queries:** Practice SELECT, JOIN, WHERE, GROUP BY, ORDER BY
- **Window Functions:** RANK(), ROW_NUMBER(), PARTITION BY
- **Aggregations:** SUM(), COUNT(), AVG(), MAX(), MIN()
- **Date Functions:** Working with dates and time-based queries
- **Business Analytics:** Revenue analysis, customer segmentation, product performance

## 📊 Sample Queries

```sql
-- Top selling tracks
SELECT t.Name, SUM(il.Quantity) as TotalSold
FROM tracks t
JOIN invoice_lines il ON t.TrackId = il.TrackId
GROUP BY t.Name
ORDER BY TotalSold DESC;

-- Revenue by country
SELECT c.Country, SUM(il.Quantity * il.UnitPrice) as Revenue
FROM customers c
JOIN invoices i ON c.CustomerId = i.CustomerId
JOIN invoice_lines il ON i.InvoiceId = il.InvoiceId
GROUP BY c.Country
ORDER BY Revenue DESC;
```

## 🎵 Business Context

- **Music Store:** Digital music sales platform
- **Global Operations:** Customers from multiple countries
- **Product Catalog:** Various artists, albums, and tracks
- **Sales Tracking:** Complete transaction history
- **Customer Management:** Customer profiles and purchase history

## 📄 License

This dataset is available under Kaggle's standard terms of use. Please review the specific license terms on the dataset page.

## 🔗 Related Resources

- [SQLite Documentation](https://www.sqlite.org/docs.html)
- [Chinook Database Schema](https://github.com/lerocha/chinook-database)
- [SQL Tutorial](https://www.w3schools.com/sql/)
