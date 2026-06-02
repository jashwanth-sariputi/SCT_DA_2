# SCT_DA_2 - Data Cleaning and Preprocessing

## Overview

This project focuses on cleaning and preprocessing the SuperStore Orders dataset using Python and Pandas. The dataset was analyzed to identify missing values, verify data quality, standardize column names, convert date columns into proper datetime format, and prepare the data for future analysis and visualization.

---

## Objective

The objectives of this project are:

- Load and inspect the dataset
- Explore dataset structure and data types
- Identify missing values
- Check for duplicate records
- Standardize column names
- Convert date columns into datetime format
- Validate data quality
- Export the cleaned dataset

---

## Dataset Information

- **Dataset Name:** SuperStore Orders
- **Original File:** SuperStoreOrders.csv
- **Total Records:** 51,290
- **Total Columns:** 21

---

## Tools Used

- Python
- Pandas
- Jupyter Notebook
- Git
- GitHub

---

## Project Files

| File | Description |
|--------|------------|
| dataset/SuperStoreOrders.csv | Original dataset |
| data_cleaning.ipynb | Jupyter Notebook containing the cleaning process |
| Cleaned_SuperStoreOrders.csv | Cleaned dataset |
| README.md | Project documentation |

---

## Data Cleaning Process

### Step 1: Import Required Libraries

```python
import pandas as pd
```

### Step 2: Load Dataset

```python
df = pd.read_csv("dataset/SuperStoreOrders.csv")
```

### Step 3: Preview Dataset

```python
df.head()
```

This provides a quick overview of the dataset and verifies successful loading.

### Step 4: Inspect Dataset Information

```python
df.info()
```

This helps identify:

- Total rows and columns
- Data types
- Non-null values

### Step 5: Standardize Column Names

```python
df.columns = df.columns.str.lower().str.replace(" ", "_")
```

Purpose:

- Improve consistency
- Simplify column access

### Step 6: Check Missing Values

```python
df.isnull().sum()
```

Result:

- No missing values found.

### Step 7: Check Duplicate Records

```python
df.duplicated().sum()
```

Result:

- No duplicate records found.

### Step 8: Convert Date Columns

```python
df['order_date'] = pd.to_datetime(df['order_date'], errors='coerce')
df['ship_date'] = pd.to_datetime(df['ship_date'], errors='coerce')
```

Purpose:

- Convert date fields into datetime format
- Enable date-based analysis

### Step 9: Validate Cleaned Dataset

```python
df.info()

df.isnull().sum()

df.columns.tolist()
```

Validation confirms:

- Correct data types
- No missing values
- Properly formatted column names

### Step 10: Export Cleaned Dataset

```python
df.to_csv("Cleaned_SuperStoreOrders.csv", index=False)

print("Dataset saved successfully")
```

Output:

```text
Dataset saved successfully
```

---

## Results

### Before Cleaning

- Rows: 51,290
- Columns: 21
- Date columns stored as text
- Column names not standardized

### After Cleaning

- Rows: 51,290
- Columns: 21
- Missing Values: 0
- Duplicate Records: 0
- Date columns converted to datetime format
- Column names standardized

---

## Final Dataset Columns

```text
order_id
order_date
ship_date
ship_mode
customer_name
segment
state
country
market
region
product_id
category
sub_category
product_name
sales
quantity
discount
profit
shipping_cost
order_priority
year
```

---

## Key Learnings

- Data inspection using Pandas
- Data preprocessing techniques
- Missing value analysis
- Duplicate detection
- Date-time conversion
- Dataset validation
- Exporting cleaned datasets
- Git and GitHub workflow

---

## Screenshots

### Dataset Preview

![Dataset Preview](screenshots/Screenshot%202026-06-02%20133747.png)

### Dataset Information

![Dataset Information](screenshots/Screenshot%202026-06-02%20133802.png)

### Missing Value Analysis

![Missing Value Analysis](screenshots/Screenshot%202026-06-02%20133816.png)

### Data Cleaning Process

![Data Cleaning Process](screenshots/Screenshot%202026-06-02%20133908.png)

### Final Output

![Final Output](screenshots/Screenshot%202026-06-02%20134019.png)

---

## Repository

**Repository Name:** SCT_DA_2

---

## Outcome

Successfully cleaned and preprocessed the SuperStore Orders dataset using Python and Pandas. The cleaned dataset is ready for exploratory data analysis, visualization, and business intelligence applications.
