# Python Code Style Guide
*For Python Programming II (90-819)*

## Quick Reference
This guide removes guesswork from coding decisions. When in doubt, follow these rules.

---

## 1. Variable and Function Names
**Rule: lowercase with underscores for readability**

```python
# Good - Variables
country_name = "United States"
sales_data = pd.read_csv("sales.csv")
customer_age = 25
api_response = requests.get(url)

# Good - Functions
def clean_data(df):
    return df.dropna()

def calculate_total_sales(sales_df):
    return sales_df['amount'].sum()

# Bad - Variables
countryName = "United States"
SalesData = pd.read_csv("sales.csv")
customerage = 25
APIResponse = requests.get(url)

# Bad - Functions
def cleanData(df):
    return df.dropna()

def CalculateTotalSales(sales_df):
    return sales_df['amount'].sum()
```

---

## 2. Class Names
**Rule: capitalize the first letter of each word (PascalCase)**

```python
# Good
class DataProcessor:
    pass

class CustomerAnalyzer:
    pass

# Bad
class data_processor:
    pass

class customerAnalyzer:
    pass
```

---

## 3. Long Strings
**Rule: use triple quotes (""") for multi-line strings**

```python
# Good
sql_query = """
SELECT customer_id, name, total_purchases
FROM customers 
WHERE registration_date >= '2024-01-01'
ORDER BY total_purchases DESC
"""

api_documentation = """
This function scrapes product data from the e-commerce API.
Returns a pandas DataFrame with columns: product_id, name, price, category.
Requires valid API key in headers.
"""

# Bad
sql_query = "SELECT customer_id, name, total_purchases FROM customers WHERE registration_date >= '2024-01-01' ORDER BY total_purchases DESC"
```

---

## 4. String Quotes
**Rule: use double quotes for regular strings, single quotes only when needed**

```python
# Good - use double quotes consistently
name = "John Smith"
file_path = "data/sales.csv"
sql_query = "SELECT * FROM customers WHERE age > 25"

# Use single quotes when string contains double quotes
message = 'The file "sales_data.csv" was not found'
html_snippet = '<div class="container">Hello World</div>'

# Bad - using single quotes when not needed
name = 'John Smith'
```

---

## 5. Comments
**Rule: write comments above the code they describe**

```python
# Good
# Remove rows with missing sales data
clean_sales = sales_df.dropna(subset=['amount'])

# Calculate monthly revenue totals
monthly_revenue = sales_df.groupby('month')['revenue'].sum()

# Connect to the products database
conn = sqlite3.connect('products.db')

# Bad
clean_sales = sales_df.dropna(subset=['amount'])  # Remove rows with missing sales data
monthly_revenue = sales_df.groupby('month')['revenue'].sum()  # Calculate monthly revenue totals
```

---

## 6. Import Organization
**Rule: organize imports in three groups with blank lines between**

```python
# Standard library imports
import re
import sqlite3
from datetime import datetime

# Third-party imports
import pandas as pd
import numpy as np
import requests
from bs4 import BeautifulSoup

# Local imports
from data_cleaner import DataCleaner
from api_client import APIClient
```

---

## 7. Constants
**Rule: ALL_CAPS with underscores**

```python
# Good - API keys, database info, and fixed values
API_KEY = "your_api_key_here"
DATABASE_NAME = "sales_data.db"
TABLE_NAME = "customers"
BASE_URL = "https://api.weather.gov/stations"

# Mathematical constants
PI = 3.14159
SALES_TAX_RATE = 0.08

# Bad
api_key = "your_api_key_here"
databaseName = "sales_data.db"
base_url = "https://api.weather.gov/stations"
```

---

## 8. File Names
**Rule: lowercase with underscores, descriptive names**

```python
# Good
customer_analysis.py
web_scraper.py
sales_data_processor.py

# Bad
CustomerAnalysis.py
webscraper.py
processor.py
```

---

## 9. DataFrame and Data Variables
**Rule: use descriptive names ending in _df for DataFrames**

```python
# Good
sales_df = pd.read_csv("sales.csv")
customer_df = pd.read_csv("customers.csv")
cleaned_data_df = sales_df.dropna()

# Also acceptable for non-DataFrame data
sales_data = [1, 2, 3, 4]
api_response = requests.get(url)
```

---

## 10. Spacing and Line Length
**Rule: keep lines under 100 characters, use spaces around operators**

```python
# Good
total_revenue = (sales_df['quantity'] * sales_df['price']).sum()

long_calculation = (
    customer_df['purchases'] * customer_df['avg_order_value'] 
    + customer_df['shipping_costs']
)

# Bad
total_revenue=(sales_df['quantity']*sales_df['price']).sum()
long_calculation=customer_df['purchases']*customer_df['avg_order_value']+customer_df['shipping_costs']
```

---

## Remember
- **Be consistent** - pick one style and stick with it throughout your project
- **Be descriptive** - `customer_count` is better than `cc` 
- **When in doubt, choose clarity** - your future self will thank you
