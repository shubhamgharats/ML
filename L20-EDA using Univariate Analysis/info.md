# EDA Using Univariate Analysis

## What is Univariate Analysis?

**Univariate Analysis** is a type of Exploratory Data Analysis (EDA) where we analyze **only one variable or column at a time**.

The main purpose is to understand the characteristics and distribution of an individual column.

---

# Types of Data Columns

Before performing Univariate Analysis, we must first identify the type of data present in the column.

Data columns are mainly divided into two types:

1. **Categorical Data**
2. **Numerical Data**

Choosing the correct visualization technique depends on the type of column.

> Always use graphs during Univariate Analysis for better visualization and to discover hidden patterns in the data.

---

# 1. Categorical Data

Categorical data contains values that belong to specific categories or groups.

### Examples

- Gender
- City
- Department
- Blood Group

## Common Graphs for Categorical Data

### 1. Count Plot

A Count Plot displays the frequency or number of occurrences of each category.

**Example:**

If a column contains Gender:

- Male → 500
- Female → 400

A Count Plot helps us visually compare the number of records in each category.

### 2. Pie Chart

A Pie Chart displays the proportion or percentage of each category relative to the whole dataset.

It is useful for understanding the distribution of categories.

---

# 2. Numerical Data

Numerical data consists of numbers that represent measurable quantities.

### Examples

- Age
- Salary
- Height
- Marks

## Common Graphs for Numerical Data

### 1. Histogram

A Histogram shows the distribution of numerical values by dividing the data into different intervals or bins.

It helps us understand:

- Data distribution
- Frequency of values
- Skewness of data
- Common value ranges

---

### 2. Box Plot

A Box Plot provides a statistical summary of numerical data.

It helps identify:

- Minimum value
- Maximum value
- Median
- Quartiles
- Outliers

> Box Plots are especially useful for detecting noise and outliers in a dataset.

---

### 3. Distplot

A Distplot is used to visualize the distribution of numerical data.

It helps us understand:

- Shape of the data distribution
- Density of values
- Whether the data follows a normal distribution

---

# Quick Summary

| Type of Data | Common Graphs |
|-------------|---------------|
| Categorical | Count Plot, Pie Chart |
| Numerical | Histogram, Box Plot, Distplot |

---

# Steps for Univariate Analysis

1. Select a single column from the dataset.
2. Identify whether the column is categorical or numerical.
3. Choose an appropriate visualization method.
4. Create graphs to understand the data.
5. Look for hidden patterns, distributions, noise, or outliers.

---

# Conclusion

Univariate Analysis focuses on analyzing **one variable at a time**.

It is an important part of EDA because it helps us understand the individual characteristics of each column before analyzing relationships between multiple variables.