
# 📊 DATA VISUALIZATION CHEAT SHEET (Python)

---

## 1️⃣ Core Libraries & Imports

```python
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd
import numpy as np
```

Optional (styling & stats):

```python
from matplotlib.ticker import FuncFormatter
from scipy import stats
```

---

## 2️⃣ Matplotlib – Base Visualization Library

### ▶ Line Plot

```python
plt.plot(x, y)
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Line Plot")
plt.show()
```

Multiple lines:

```python
plt.plot(x1, y1, label="Line 1")
plt.plot(x2, y2, label="Line 2")
plt.legend()
```

---

### ▶ Bar Chart

```python
plt.bar(categories, values)
plt.title("Bar Chart")
plt.show()
```

Horizontal:

```python
plt.barh(categories, values)
```

---

### ▶ Histogram

```python
plt.hist(data, bins=10)
plt.title("Histogram")
plt.show()
```

Normalized:

```python
plt.hist(data, bins=10, density=True)
```

---

### ▶ Scatter Plot

```python
plt.scatter(x, y)
plt.title("Scatter Plot")
plt.show()
```

With size:

```python
plt.scatter(x, y, s=50)
```

---

### ▶ Pie Chart

```python
plt.pie(values, labels=labels, autopct='%1.1f%%')
plt.title("Pie Chart")
plt.show()
```

---

### ▶ Box Plot

```python
plt.boxplot(data)
plt.title("Box Plot")
plt.show()
```

---

### ▶ Subplots

```python
plt.subplot(1, 2, 1)
plt.plot(x, y)

plt.subplot(1, 2, 2)
plt.bar(x, y)

plt.show()
```

---

## 3️⃣ Seaborn – Statistical Visualization

### ▶ Set Theme

```python
sns.set_theme(style="darkgrid")
```

---

### ▶ Line Plot

```python
sns.lineplot(x=x, y=y)
```

---

### ▶ Bar Plot

```python
sns.barplot(x="category", y="value", data=df)
```

---

### ▶ Count Plot (VERY IMPORTANT)

```python
sns.countplot(x="gender", data=df)
```

---

### ▶ Histogram

```python
sns.histplot(data, bins=10)
```

With KDE:

```python
sns.histplot(data, kde=True)
```

---

### ▶ Box Plot

```python
sns.boxplot(x="category", y="value", data=df)
```

---

### ▶ Violin Plot

```python
sns.violinplot(x="category", y="value", data=df)
```

---

### ▶ Scatter Plot

```python
sns.scatterplot(x="x", y="y", data=df)
```

With hue:

```python
sns.scatterplot(x="x", y="y", hue="category", data=df)
```

---

### ▶ Pair Plot (Placement Favorite ⭐)

```python
sns.pairplot(df)
```

---

### ▶ Heatmap (Correlation)

```python
corr = df.corr()
sns.heatmap(corr, annot=True, cmap="coolwarm")
```

---

## 4️⃣ Pandas Built-in Plotting

### ▶ Line Plot

```python
df.plot()
```

---

### ▶ Bar Plot

```python
df.plot(kind="bar")
```

---

### ▶ Histogram

```python
df['column'].plot(kind="hist")
```

---

### ▶ Box Plot

```python
df.boxplot()
```

---

### ▶ Scatter

```python
df.plot(kind="scatter", x="col1", y="col2")
```

---

## 5️⃣ Common Chart → Use Case Mapping (VERY IMPORTANT)

| Chart Type | Use Case               |
| ---------- | ---------------------- |
| Line       | Trend over time        |
| Bar        | Category comparison    |
| Histogram  | Data distribution      |
| Box        | Outliers & spread      |
| Scatter    | Relationship           |
| Heatmap    | Correlation            |
| Pie        | Proportion             |
| Violin     | Distribution + density |

---

## 6️⃣ Customization Cheats

### ▶ Figure Size

```python
plt.figure(figsize=(8, 5))
```

---

### ▶ Grid

```python
plt.grid(True)
```

---

### ▶ Rotate Labels

```python
plt.xticks(rotation=45)
```

---

### ▶ Save Figure

```python
plt.savefig("plot.png")
```

---

## 7️⃣ Quick Practical Template (Exam-Ready)

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv("data.csv")

sns.set_theme(style="whitegrid")
sns.boxplot(x="Category", y="Value", data=df)

plt.title("Category vs Value")
plt.show()
```

---

## 8️⃣ Common Viva Questions (Expect These)

✔ Difference between **matplotlib & seaborn**
✔ When to use **histogram vs boxplot**
✔ What does **hue** do in seaborn
✔ What does **KDE** represent
✔ How to visualize **outliers**

