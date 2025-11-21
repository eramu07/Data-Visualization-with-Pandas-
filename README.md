# Data Visualization with Pandas — A Complete Beginner-Friendly Guide.
Data visualization is essential for data analysis, helping us uncover patterns, trends, and communicate findings effectively. With the Pandas library in Python, paired with visualization libraries such as Matplotlib and Seaborn, creating informative charts is straightforward—even for beginners!

Below are six essential charts we should know, with simple explanations and examples of how to create them with Pandas.


## 1. Line Chart

**What it shows:** Trends over time or continuous data  
**Why it's useful:** Perfect for analyzing time series (stock prices, temperature, etc.)  
**Common uses:** Tracking values as they change (e.g., sales per month)

```python
import pandas as pd
import matplotlib.pyplot as plt

data = pd.DataFrame({
    "Month": ["Jan", "Feb", "Mar", "Apr"],
    "Sales": [100, 120, 140, 130]
})

data.plot(x="Month", y="Sales", kind="line", marker="o")
plt.title("Monthly Sales")
plt.ylabel("Sales")
plt.show()
```

---

## 2. Bar Chart

**What it shows:** Comparisons between categories  
**Why it's useful:** Shows differences between groups (regions, products, etc.)  
**Common uses:** Comparing quantities, frequencies, or means

```python
data = pd.DataFrame({
    "Fruit": ["Apple", "Banana", "Cherry"],
    "Count": [10, 15, 7]
})

data.plot(x="Fruit", y="Count", kind="bar", color="skyblue")
plt.title("Fruit Count")
plt.ylabel("Count")
plt.show()
```

---

## 3. Histogram

**What it shows:** Distribution of a single numerical variable  
**Why it's useful:** Visualizes how data values are spread (or binned)  
**Common uses:** Examining distributions, outliers, and skew

```python
import numpy as np
data = pd.DataFrame({
    "Age": np.random.randint(10, 60, 100)
})

data["Age"].plot(kind="hist", bins=10, edgecolor="black")
plt.title("Age Distribution")
plt.xlabel("Age")
plt.show()
```

---

## 4. Scatter Plot

**What it shows:** Relationship between two numeric variables  
**Why it's useful:** Reveals possible correlations or clusters  
**Common uses:** Studying associations (e.g., height vs. weight)

```python
data = pd.DataFrame({
    "Height": [160, 165, 170, 175, 180],
    "Weight": [55, 60, 65, 70, 75]
})

data.plot(kind="scatter", x="Height", y="Weight")
plt.title("Height vs Weight")
plt.show()
```

---

## 5. Box Plot

**What it shows:** Summary of numeric data (median, quartiles, outliers)  
**Why it's useful:** Quickly compares distributions, finds outliers  
**Common uses:** Comparing test scores, sales, or any measurable variable

```python
data = pd.DataFrame({
    "Math": [70, 80, 75, 90, 60, 85, 77, 88, 70]
})

data.boxplot(column="Math")
plt.title("Math Scores")
plt.ylabel("Score")
plt.show()
```

---

## 6. Pie Chart

**What it shows:** Proportions of categories as parts of a whole  
**Why it's useful:** Visualizes simple composition data  
**Common uses:** Market share, survey breakdown, budget allocation

```python
data = pd.Series([40, 35, 25], index=["Product A", "Product B", "Product C"])
data.plot(kind="pie", autopct="%1.1f%%")
plt.title("Market Share")
plt.ylabel("")  # Hide y-label
plt.show()
```

---

## Tips for Beginners

- Use `plt.show()` after your Pandas plots to display the chart.
- Install Seaborn for more advanced and attractive visualizations (`pip install seaborn`).
- Use `data.head()` and `data.info()` to understand your DataFrame before plotting.

**Keep experimenting! Visualization is key to unlocking insights from your data.**

---
