 # Matplotlib – Python Visualization Library

> Create powerful, customizable plots with just a few lines of code.

---

## What is Matplotlib?

Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python. It's highly customizable and works well with Pandas and NumPy.

---

## Getting Started

```bash
pip install matplotlib
```

```python
import matplotlib.pyplot as plt
```

---

## Basic Plot

```python
x = [1, 2, 3, 4]
y = [10, 20, 25, 30]

plt.plot(x, y)
plt.title("Line Plot")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.show()
```

---

## Common Plot Types

### 1. Line Plot

```python
plt.plot([1, 2, 3], [4, 5, 6])
plt.show()
```

### 2. Bar Chart

```python
categories = ['A', 'B', 'C']
values = [5, 7, 3]

plt.bar(categories, values)
plt.title("Bar Chart")
plt.show()
```

### 3. Scatter Plot

```python
plt.scatter([1, 2, 3], [4, 1, 9])
plt.title("Scatter Plot")
plt.show()
```

### 4. Pie Chart

```python
slices = [40, 30, 20, 10]
labels = ['Python', 'Java', 'C++', 'Ruby']

plt.pie(slices, labels=labels, autopct='%1.1f%%')
plt.title("Language Popularity")
plt.show()
```

---

## Customizing Your Plots

### Titles and Labels

```python
plt.title("Main Title")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
```

### Grid and Legends

```python
plt.grid(True)
plt.legend(['Data 1'])
```

### Colors and Styles

```python
plt.plot(x, y, color='red', linestyle='--', marker='o')
```

---

## Subplots

```python
plt.subplot(1, 2, 1)
plt.plot([1, 2], [3, 4])
plt.title("First Plot")

plt.subplot(1, 2, 2)
plt.plot([1, 2], [5, 2])
plt.title("Second Plot")

plt.tight_layout()
plt.show()
```

---

## Save the Plot

```python
plt.savefig("plot.png")
```

---

## Integration with Pandas

```python
import pandas as pd

data = pd.DataFrame({
    'x': [1, 2, 3],
    'y': [10, 20, 15]
})

data.plot(x='x', y='y', kind='line')
plt.show()
```

---

## Tips

- Use `%matplotlib inline` in Jupyter Notebooks
- Use `plt.style.use('ggplot')` for pre-set themes
- Use `tight_layout()` to fix overlapping elements

---

## Summary

- **Highly Customizable**: Colors, styles, fonts
- **Versatile**: Works with NumPy, Pandas, SciPy
- **Good for Exploratory Analysis & Presentation**

---

> “A good plot is worth a thousand lines of raw data.”