# SCT_DA_2 - Data Cleaning and Preprocessing

## Overview

This project focuses on cleaning and preprocessing the SuperStore Orders dataset using Python and Pandas. The dataset was inspected for missing values, duplicate records, incorrect data types, and overall data quality issues before being prepared for future analysis and visualization.

## Objective

The main objectives of this task were:
# SCT_DA_2 - Data Cleaning and Preprocessing

## Overview

This project focuses on cleaning and preprocessing the SuperStore Orders dataset using Python and Pandas. The dataset was examined for missing values, duplicate records, inconsistent data formats, and overall data quality issues. The cleaned dataset is then exported for future analysis and visualization.

---

## Objective

The objectives of this project are:

- Load and inspect the dataset
- Explore dataset structure and data types
- Identify missing values
- Check for duplicate records
- Convert date columns into proper datetime format
- Standardize column names
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

## Project Structure

```text
SCT_DA_2/
│
├── dataset/
│   └── SuperStoreOrders.csv
│
├── screenshots/
│
├── data_cleaning.ipynb
├── Cleaned_SuperStoreOrders.csv
└── README.md
```

---

## Data Cleaning Process

### Step 1: Import Required Libraries

```python
import pandas as pd
```

### Step 2: Load the Dataset

```python
df = pd.read_csv("dataset/SuperStoreOrders.csv")
```

### Step 3: Preview the Dataset

```python
df.head()
```

This step helps verify that the dataset has loaded correctly and provides an overview of the available columns.

### Step 4: Inspect Dataset Information

```python
df.info()
```

This provides:

- Number of rows and columns
- Data types of each column
- Non-null value counts

### Step 5: Standardize Column Names

```python
df.columns = df.columns.str.lower().str.replace(" ", "_")
```

This ensures consistency and easier column referencing.

### Step 6: Check Missing Values

```python
df.isnull().sum()
```

Result:

- No missing values were found in the dataset.

### Step 7: Check Duplicate Records

```python
df.duplicated().sum()
```

Result:

- No duplicate records were found.

### Step 8: Convert Date Columns

```python
df['order_date'] = pd.to_datetime(df['order_date'], errors='coerce')
df['ship_date'] = pd.to_datetime(df['ship_date'], errors='coerce')
```

Purpose:

- Convert date columns into datetime format
- Enable date-based analysis and visualization

### Step 9: Validate Cleaned Data

```python
df.isnull().sum().sum()

df.columns.tolist()

df.info()
```

Validation confirms:

- No missing values
- Correct data types
- Standardized column names

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
- Column names contained formatting inconsistencies

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
- Data cleaning and preprocessing techniques
- Missing value analysis
- Duplicate detection
- Date-time conversion
- Data validation
- Exporting cleaned datasets
- Git and GitHub workflow

---

## Screenshots

### Dataset Preview

![Dataset Preview](screenshots/Screenshot%202026-06-02%20004450.png)

### Dataset Information

![Dataset Information](screenshots/Screenshot%202026-06-02%20004517.png)

### Missing Value Analysis

![Missing Value Analysis](screenshots/Screenshot%202026-06-02%20004541.png)

### Data Cleaning Process

![Data Cleaning Process](screenshots/Screenshot%202026-06-02%20004651.png)

### Final Output

![Final Output](screenshots/Screenshot%202026-06-02%20004843.png)

---

## Repository

**Repository Name:** SCT_DA_2

---

## Outcome

Successfully cleaned and prepared the SuperStore Orders dataset using Python and Pandas. The dataset is now ready for exploratory data analysis, visualization, and business intelligence applications.
- Load and inspect the dataset
- Explore dataset structure and data types
- Identify missing values
- Check for duplicate records
- Convert date columns into proper datetime format
- Standardize column names
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

## Project Structure

```text
SCT_DA_2/
│
├── dataset/
│   └── SuperStoreOrders.csv
│
├── screenshots/
│   ├── Screenshot1.png
│   ├── Screenshot2.png
│   ├── Screenshot3.png
│   ├── Screenshot4.png
│   └── Screenshot5.png
│
├── data_cleaning.ipynb
├── Cleaned_SuperStoreOrders.csv
└── README.md
```

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

Purpose:

- Verify successful loading
- Understand dataset structure

---

### Step 4: Inspect Dataset Information

```python
df.info()
```

Purpose:

- Check column names
- Verify data types
- Identify missing values

---

### Step 5: Standardize Column Names

```python
df.columns = df.columns.str.lower().str.replace(" ", "_")
```

Purpose:

- Improve consistency
- Simplify column referencing

---

### Step 6: Check Missing Values

```python
df.isnull().sum()
```

Result:

- No missing values found in the dataset.

---

### Step 7: Check Duplicate Records

```python
df.duplicated().sum()
```

Result:

- No duplicate records found.

---

### Step 8: Convert Date Columns

```python
df['order_date'] = pd.to_datetime(df['order_date'], errors='coerce')
df['ship_date'] = pd.to_datetime(df['ship_date'], errors='coerce')
```

Purpose:

- Enable date-based analysis
- Ensure correct datetime format

---

### Step 9: Validate Cleaned Dataset

```python
df.info()

df.isnull().sum()

df.columns.tolist()
```

Validation Checks:

- Correct data types
- No missing values
- Proper column names

---

### Step 10: Export Cleaned Dataset

```python
df.to_csv("Cleaned_SuperStoreOrders.csv", index=False)
```

Output:

```text
Cleaned_SuperStoreOrders.csv
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
- Date columns converted to datetime
- Column names standardized
- Missing Values: 0
- Duplicate Records: 0

---

## Key Learnings

- Data inspection using Pandas
- Data quality assessment
- Handling date-time conversion
- Detecting duplicates
- Checking missing values
- Exporting processed datasets
- Git and GitHub workflow

---

## Screenshots

### Dataset Preview

![Dataset Preview](screenshots/Screenshot1.png)

### Dataset Information

![Dataset Information](screenshots/Screenshot2.png)

### Missing Value Analysis

![Missing Values](screenshots/Screenshot3.png)

### Validation After Cleaning

![Validation](screenshots/Screenshot4.png)

### Final Dataset Columns

![Final Output](screenshots/Screenshot5.png)

---

## Repository

Repository Name:

```text
SCT_DA_2
```

---

## Outcome

Successfully cleaned and prepared the SuperStore Orders dataset for future data analysis, visualization, and business intelligence applications using Python and Pandas.
