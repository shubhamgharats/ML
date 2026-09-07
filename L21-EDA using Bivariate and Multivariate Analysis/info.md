# EDA Using Bivariate and Multivariate Analysis

## What is Bivariate Analysis?

**Bivariate Analysis** is a type of EDA where we analyze the **relationship between two variables**.

It helps us understand how one variable is related to another variable.

### Examples

- Gender and Salary
- Age and Salary
- Height and Weight
- Gender and Purchased

---

# Types of Bivariate Analysis

Bivariate Analysis is mainly divided into:

1. **Numerical vs Numerical**
2. **Categorical vs Numerical**
3. **Categorical vs Categorical**

---

# 1. Numerical vs Numerical

Both variables contain numerical values.

### Examples

- Age and Salary
- Height and Weight
- Experience and Salary

### Scatter Plot

A **Scatter Plot** is used to visualize the relationship between two numerical variables.

```python
sns.scatterplot(data=df, x='age', y='salary')
```

It helps identify:

- Positive relationship
- Negative relationship
- No relationship
- Outliers
- Patterns

### Correlation

**Correlation** measures the **strength and direction** of the relationship between two numerical variables.

```python
df[['age', 'salary']].corr()
```

Correlation ranges from **-1 to +1**:

- `+1` → Strong positive relationship
- `0` → No linear relationship
- `-1` → Strong negative relationship

---

# 2. Categorical vs Numerical

One variable is categorical and the other is numerical.

### Examples

- Gender and Salary
- Department and Salary
- City and Age

### Box Plot

A **Box Plot** compares the distribution of numerical values across different categories.

```python
sns.boxplot(data=df, x='gender', y='salary')
```

It helps identify:

- Median
- Quartiles
- Spread of data
- Outliers

### Bar Plot

A **Bar Plot** is used to compare numerical values across different categories.

```python
sns.barplot(data=df, x='gender', y='salary')
```

It is useful for comparing the **average value** of a numerical variable across different categories.

---

# 3. Categorical vs Categorical

Both variables contain categorical values.

### Examples

- Gender and Purchased
- Department and Job Role
- City and Education

### Crosstab

A **Crosstab** creates a frequency table showing the relationship between two categorical variables.

```python
pd.crosstab(df['gender'], df['purchased'])
```

### Count Plot

A **Count Plot** displays the number of observations belonging to different categories.

```python
sns.countplot(data=df, x='gender', hue='purchased')
```

### Heatmap

A Crosstab can be visualized using a **Heatmap**.

```python
ct = pd.crosstab(df['gender'], df['purchased'])

sns.heatmap(ct, annot=True, fmt='d')
```

---

# What is Multivariate Analysis?

**Multivariate Analysis** is a type of EDA where we analyze **three or more variables at the same time**.

It helps us understand complex relationships and interactions between multiple variables.

### Example

We can analyze:

- Age
- Salary
- Experience
- Gender

together to understand how these variables are related.

---

# Common Graphs for Multivariate Analysis

### 1. Pair Plot

A **Pair Plot** shows the relationships between multiple numerical variables.

```python
sns.pairplot(df)
```

It helps identify:

- Relationships
- Correlations
- Distributions
- Patterns
- Outliers

---

### 2. Scatter Plot with Hue

A third variable can be represented using different colors.

```python
sns.scatterplot(
    data=df,
    x='age',
    y='salary',
    hue='gender'
)
```

Here:

- `age` → X-axis
- `salary` → Y-axis
- `gender` → Color

---

### 3. Correlation Heatmap

A **Correlation Heatmap** shows the correlation between multiple numerical variables.

```python
sns.heatmap(
    df.corr(numeric_only=True),
    annot=True
)
```

It helps identify:

- Strong positive correlations
- Strong negative correlations
- Weak correlations
- Highly related features

---

# Pivot Table with Heatmap

A **Pivot Table** can be used to summarize data using multiple variables.

Example using the `flights` dataset:

```python
pivot = flights.pivot_table(
    values='passengers',
    index='month',
    columns='year'
)

sns.heatmap(pivot, annot=True, fmt='g')
```

Here:

- `month` → Rows
- `year` → Columns
- `passengers` → Values

It helps identify patterns in passenger numbers across different months and years.

---

# Bivariate vs Multivariate Analysis

| Bivariate Analysis | Multivariate Analysis |
|-------------------|-----------------------|
| Studies two variables | Studies three or more variables |
| Focuses on one relationship | Focuses on multiple relationships |
| Easier to interpret | More complex |
| Scatter Plot, Box Plot, Bar Plot | Pair Plot, Heatmap, Scatter Plot |

---

# Quick Summary

| Analysis Type | Common Graphs |
|--------------|---------------|
| Numerical vs Numerical | Scatter Plot, Correlation |
| Categorical vs Numerical | Box Plot, Bar Plot |
| Categorical vs Categorical | Count Plot, Crosstab, Heatmap |
| Multivariate | Pair Plot, Heatmap, Scatter Plot |

---

# Steps for Bivariate and Multivariate Analysis

1. Select two or more columns from the dataset.
2. Identify the data type of each column.
3. Choose an appropriate visualization.
4. Create graphs to understand relationships.
5. Look for patterns, trends, correlations, and outliers.
6. Compare different variables and categories.
7. Draw meaningful conclusions from the analysis.

---

# Importance of Bivariate and Multivariate Analysis

These analyses help us:

- Understand relationships between variables
- Find correlations
- Discover hidden patterns
- Detect outliers
- Compare different groups
- Understand interactions between features
- Select useful features for Machine Learning

---

# Conclusion

**Bivariate Analysis** focuses on the **relationship between two variables**, while **Multivariate Analysis** focuses on **three or more variables together**.

Graphs such as **Scatter Plot, Box Plot, Bar Plot, Pair Plot, and Heatmap** help us understand relationships, patterns, correlations, trends, and outliers in a dataset.