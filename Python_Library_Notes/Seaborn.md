# Seaborn – Statistical Data Visualization Library

> Build beautiful and informative statistical graphics with ease.

---

## What is Seaborn?

Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.

---

## Getting Started

```bash
pip install seaborn
```

```python
import seaborn as sns
import matplotlib.pyplot as plt
```

---

## Built-in Datasets

```python
tips = sns.load_dataset("tips")
iris = sns.load_dataset("iris")
```

---

## Basic Plot

```python
sns.lineplot(x="total_bill", y="tip", data=tips)
plt.title("Line Plot with Seaborn")
plt.show()
```

---

## Common Plot Types

### 1. Histogram (Distplot)

```python
sns.histplot(tips["total_bill"], kde=True)
plt.title("Histogram with KDE")
plt.show()
```

### 2. Box Plot

```python
sns.boxplot(x="day", y="total_bill", data=tips)
plt.title("Box Plot")
plt.show()
```

### 3. Violin Plot

```python
sns.violinplot(x="day", y="total_bill", data=tips)
plt.title("Violin Plot")
plt.show()
```

### 4. Count Plot

```python
sns.countplot(x="day", data=tips)
plt.title("Count Plot")
plt.show()
```

### 5. Scatter Plot

```python
sns.scatterplot(x="total_bill", y="tip", data=tips, hue="sex")
plt.title("Scatter Plot")
plt.show()
```

### 6. Pair Plot

```python
sns.pairplot(iris, hue="species")
plt.suptitle("Pair Plot")
plt.show()
```

---

## Heatmap

```python
corr = tips.corr()
sns.heatmap(corr, annot=True, cmap="coolwarm")
plt.title("Correlation Heatmap")
plt.show()
```

---

## Customization

### Style

```python
sns.set_style("whitegrid")  # options: white, dark, whitegrid, darkgrid, ticks
```

### Color Palette

```python
sns.set_palette("pastel")
```

### Titles and Labels

```python
plt.title("Plot Title")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
```

---

## Save the Plot

```python
plt.savefig("seaborn_plot.png")
```

---

## Summary

- **Easy to Use**: Clean API built on top of Matplotlib
- **Statistical Focus**: Best for visualizing complex relationships
- **Great Aesthetics**: Beautiful default themes and color palettes

---

> “Seaborn makes your data talk in colors, lines, and patterns.”