# Sepal Length vs. Petal Length Scatter Plot

## Overview
This project visualizes the relationship between **sepal length** and **petal length** in a dataset using **Seaborn** and **Matplotlib**. The plot differentiates species using distinct colors, making it easier to identify patterns and trends.

## Description
The script creates a **scatter plot** where:
- The x-axis represents **sepal length (cm)**.
- The y-axis represents **petal length (cm)**.
- Each data point corresponds to an individual sample.
- Species are visually distinguished using a customized **color palette**.

## Code Implementation
```python
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd

# Sample dataset loading (Replace with actual data)
df = pd.read_csv("your_dataset.csv")

# Create the scatter plot
plt.figure(figsize=(8, 5))
sns.scatterplot(data=df, x='sepal length (cm)', y='petal length (cm)', hue='species', 
                palette={'setosa': 'purple', 'versicolor': 'orange', 'virginica': 'cyan'})

# Add titles and labels
plt.title("Sepal Length vs. Petal Length")
plt.xlabel("Sepal Length (cm)")
plt.ylabel("Petal Length (cm)")

# Display legend and show the plot
plt.legend()
plt.show()
