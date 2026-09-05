# Understanding Your Data

Before performing data analysis or building a Machine Learning model, we first need to understand the dataset.

## 1. How Big Is the Data?

- The size of a dataset is determined by its **number of rows and columns**.
- **Rows** represent individual records or observations.
- **Columns** represent features or variables.
- Knowing the size helps us understand how large the dataset is.

### Key Point

> Dataset Size = Number of Rows × Number of Columns

---

## 2. How Does the Data Look?

- We can view a few records from the dataset to get an overview.
- This helps us understand:
  - Column names
  - Values stored in each column
  - Overall structure of the dataset
  - Whether the data has been loaded correctly
- Viewing random records can provide a better understanding of different data samples.

### Key Point

> The goal is to get a quick overview of the dataset.

---

## 3. What Are the Data Types of Columns?

Different columns can contain different types of data.

Common data types include:

- **Integer (`int`)** → Whole numbers
- **Float (`float`)** → Decimal numbers
- **Object/String** → Text or categorical data
- **Boolean** → True or False values
- **Date/Time** → Dates and timestamps

Checking the information of columns can also help us identify:

- Number of non-null values
- Missing values
- Memory usage
- Incorrect data types

### Why Is This Important?

The data type determines what operations and analysis can be performed on a column.

---

## 4. Are There Any Missing Values?

Missing values occur when information is unavailable for certain records.

Examples include:

- Empty cells
- Null values
- Missing information

We check every column to find the number of missing values.

### Why Are Missing Values Important?

Missing values can:

- Affect data analysis
- Cause problems while building Machine Learning models
- Reduce the accuracy of predictions

Depending on the dataset, missing values can be:

- Removed
- Replaced with suitable values
- Handled using other techniques

---

## 5. How Does the Data Look Mathematically?

Numerical data can be understood using **descriptive statistics**.

Important statistical values include:

- **Count** → Number of available values
- **Mean** → Average value
- **Standard Deviation** → Variation in the data
- **Minimum** → Smallest value
- **25% (Q1)** → First quartile
- **50% (Median)** → Middle value
- **75% (Q3)** → Third quartile
- **Maximum** → Largest value

### These Statistics Help Us Understand:

- Distribution of numerical data
- Range of values
- Variation in the dataset
- Possible outliers

---

# Quick Summary

| Question | Purpose |
|----------|---------|
| How big is the data? | Understand the number of rows and columns |
| How does the data look? | Get a quick overview of the dataset |
| What are the data types? | Understand the type of information in each column |
| Are there missing values? | Identify incomplete data |
| How does the data look mathematically? | Understand statistical properties of numerical data |

---

## Conclusion

Understanding the dataset is an important first step in **Exploratory Data Analysis (EDA)**.

It helps us:

- Understand the structure of the data
- Identify missing values
- Check data types
- Analyze statistical properties
- Detect potential problems before further analysis or model building