# YData-Profiling Library

## What is YData-Profiling?

**YData-Profiling** is a Python library used for **automated Exploratory Data Analysis (EDA)**.

It automatically generates a detailed report about a dataset with very little code.

> YData-Profiling was previously known as **Pandas Profiling**.

---

# Installation

Install the library using:

```bash
pip install ydata-profiling
```

---

# Importing the Library

```python
from ydata_profiling import ProfileReport
```

---

# Basic Usage

First, load a dataset using Pandas.

```python
import pandas as pd
from ydata_profiling import ProfileReport

df = pd.read_csv('data.csv')
```

Create a profiling report:

```python
profile = ProfileReport(df)
```

Display the report in Jupyter Notebook:

```python
profile.to_notebook_iframe()
```

---

# Generating an HTML Report

We can also save the profiling report as an HTML file.

```python
profile.to_file('report.html')
```

The generated file can be opened in a web browser.

---

# What Does YData-Profiling Analyze?

YData-Profiling automatically provides information about:

- Number of rows and columns
- Data types
- Missing values
- Duplicate rows
- Descriptive statistics
- Data distribution
- Correlations
- Outliers
- Unique values

---

# Advantages

- Saves time during EDA
- Requires very little code
- Generates detailed reports automatically
- Helps identify data quality problems
- Useful for quickly understanding a new dataset

---

# Limitations

- Can be slow for very large datasets
- Generated reports may contain more information than required
- Manual EDA is still important for deeper analysis

---

# Quick Summary

| Feature | Description |
|---------|-------------|
| Library | YData-Profiling |
| Previous Name | Pandas Profiling |
| Purpose | Automated EDA |
| Input | Pandas DataFrame |
| Output | Detailed EDA Report |

---

# Conclusion

**YData-Profiling** is a useful library for performing automated **Exploratory Data Analysis**.

It helps quickly understand a dataset by automatically generating information about **missing values, distributions, correlations, duplicates, and other important data characteristics**.