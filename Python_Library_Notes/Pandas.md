
# **pandas: The Data Analysis Powerhouse for Python**

> A fast, flexible, and expressive data analysis library built on top of NumPy. Perfect for manipulating tabular, labeled, or time-series data.

---

## **Installation**

```bash
pip install pandas
```

---

## **Importing pandas**

```python
import pandas as pd
```

---

## **Core Data Structures**

### **1. Series**
- A **one-dimensional** labeled array.
```python
s = pd.Series([10, 20, 30])
```

### **2. DataFrame**
- A **two-dimensional** table of rows and columns (like an Excel sheet).
```python
df = pd.DataFrame({
    'Name': ['Alice', 'Bob'],
    'Age': [25, 30]
})
```

---

## **Reading & Writing Data**

| Format     | Read                             | Write                            |
|------------|----------------------------------|----------------------------------|
| CSV        | `pd.read_csv('file.csv')`       | `df.to_csv('file.csv')`          |
| Excel      | `pd.read_excel('file.xlsx')`    | `df.to_excel('file.xlsx')`       |
| JSON       | `pd.read_json('file.json')`     | `df.to_json('file.json')`        |
| SQL        | `pd.read_sql(query, conn)`      | `df.to_sql('table', conn)`       |

---

## **Quick Data Exploration**

```python
df.head()         # First 5 rows
df.tail()         # Last 5 rows
df.shape          # (rows, columns)
df.columns        # Column names
df.info()         # Data types and null counts
df.describe()     # Summary statistics
df.dtypes         # Data types of each column
```

---

## **Selecting Data**

### **Columns**
```python
df['Name']            # Single column
df[['Name', 'Age']]   # Multiple columns
```

### **Rows**
```python
df.iloc[0]            # First row (by index)
df.loc[0]             # First row (by label)
```

### **Slicing**
```python
df[0:3]               # First 3 rows
```

---

## **Filtering Rows**

```python
df[df['Age'] > 25]                     # Age greater than 25
df[(df['Age'] > 25) & (df['Gender'] == 'Male')]   # Multiple conditions
```

---

## **Modifying Data**

```python
df['Age'] = df['Age'] + 1              # Modify existing column
df['Salary'] = df['Age'] * 1000        # Create new column
df.rename(columns={'Age': 'Years'})    # Rename column
```

---

## **Handling Missing Values**

```python
df.isnull()                      # Detect missing values
df.dropna()                      # Drop rows with nulls
df.fillna(0)                     # Replace nulls with a value
```

---

## **Sorting & Reordering**

```python
df.sort_values(by='Age')         # Sort by column
df.sort_values(by='Age', ascending=False)
df.sort_index()                  # Sort by index
```

---

## **Grouping and Aggregation**

```python
df.groupby('Gender')['Age'].mean()     # Group and get mean
df.groupby('Gender').agg({
    'Age': 'mean',
    'Salary': 'sum'
})
```

---

## **Merging and Joining**

```python
pd.merge(df1, df2, on='ID')         # Merge on common column
df1.join(df2, how='inner')          # Join by index
```

---

## **Useful Tricks**

```python
df['Name'].unique()         # Unique values
df['Age'].value_counts()    # Frequency count
df.sample(5)                # Random sample of 5 rows
df.memory_usage()          # Memory usage of DataFrame
```

---

## **Saving Your Work**

```python
df.to_csv('output.csv', index=False)     # Save without index
df.to_excel('output.xlsx')               # Save to Excel
```

---

## **Mini Project Example**

```python
import pandas as pd

# Load data
df = pd.read_csv('students.csv')

# Clean & analyze
df = df.dropna()
df['Grade'] = df['Marks'].apply(lambda x: 'Pass' if x >= 40 else 'Fail')

# Summary
print(df.groupby('Grade')['Name'].count())
```

---

## **Why Use pandas?**

- Simplifies data cleaning, filtering, and analysis.
- Works great with NumPy, matplotlib, and scikit-learn.
- Ideal for Excel replacements and data pipelines.

---

## **Learn More**

- [Official Docs](https://pandas.pydata.org/docs/)
- [pandas Cheat Sheet (PDF)](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)

---

> **"Data is the new oil — pandas is your refinery."**

