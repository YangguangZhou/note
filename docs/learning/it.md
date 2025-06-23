---
level: secret
---

# 信息技术

## Matplotlib 常用图表类型

本文档介绍了 Matplotlib 库中四种常见的图表类型：线图(plot)、散点图(scatter)、柱状图(bar)和水平柱状图(barh)。

### 1. 线图 (plot)

线图用于绘制连续的线条图表，常用于展示随时间变化的趋势或连续数据的变化。其特点是数据点之间用线段连接，形成连续曲线。

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 10, 100)
y = np.sin(x)
    
plt.figure(figsize=(8, 6))
plt.plot(x, y, 'b-', linewidth=2)
plt.title('线图 (Line Plot)')
plt.xlabel('X 轴')
plt.ylabel('Y 轴')
plt.grid(True)
plt.show()
```

![线图示例](https://private-us-east-1.manuscdn.com/sessionFile/rRuTnFWvPRg0shnMgewuiG/sandbox/ReBAfYPehhY63JwGWKQsre-images_1748394494077_na1fn_L2hvbWUvdWJ1bnR1L21hdHBsb3RsaWJfZXhhbXBsZXMvaW1hZ2VzL2xpbmVfcGxvdA.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvclJ1VG5GV3ZQUmcwc2huTWdld3VpRy9zYW5kYm94L1JlQkFmWVBlaGhZNjNKd0dXS1FzcmUtaW1hZ2VzXzE3NDgzOTQ0OTQwNzdfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwyMWhkSEJzYjNSc2FXSmZaWGhoYlhCc1pYTXZhVzFoWjJWekwyeHBibVZmY0d4dmRBLnBuZyIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTc2NzIyNTYwMH19fV19&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=Z0cZvi3fahG1~WeAKWcJyouAEW2ULdtlIDkCIKSI9D1lhFA10dcLwg0wnzuhnG8zZnqT2zNqnIubACMSqEd40fgF-TQMP7mNQMIjNcm8u0h8kAg-4JYzJYFjQuz1WijjAHjyojLTmOKICmVfXYhbht-dvAqlDHL~K6QcoTiSatoZOTIpnhYotB0OUTi0wEIOLrXNq82Zbz-aMcI7ezMFyOBgvMJIBdEX9BS~tOktQoN7EL~jHixfN3jClIny5G~eqTPTCNAglKiYJcz6AEdm5IihizsgObngMZsULo3-OXx6Wq~FkDEzwXi4iSJTzYq-Te0rcpIS8fvnv~I3aYapZg__)

### 2. 散点图 (scatter)

散点图用于绘制分散的点，常用于展示两个变量之间的关系或分布。其特点是每个数据点独立显示，可以通过颜色、大小表示额外维度的信息。

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.random.rand(50)
y = np.random.rand(50)
colors = np.random.rand(50)
sizes = 1000 * np.random.rand(50)
    
plt.figure(figsize=(8, 6))
plt.scatter(x, y, c=colors, s=sizes, alpha=0.7)
plt.title('散点图 (Scatter Plot)')
plt.xlabel('X 轴')
plt.ylabel('Y 轴')
plt.colorbar(label='颜色值')
plt.grid(True)
plt.show()
```

![散点图示例](https://private-us-east-1.manuscdn.com/sessionFile/rRuTnFWvPRg0shnMgewuiG/sandbox/ReBAfYPehhY63JwGWKQsre-images_1748394494077_na1fn_L2hvbWUvdWJ1bnR1L21hdHBsb3RsaWJfZXhhbXBsZXMvaW1hZ2VzL3NjYXR0ZXJfcGxvdA.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvclJ1VG5GV3ZQUmcwc2huTWdld3VpRy9zYW5kYm94L1JlQkFmWVBlaGhZNjNKd0dXS1FzcmUtaW1hZ2VzXzE3NDgzOTQ0OTQwNzdfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwyMWhkSEJzYjNSc2FXSmZaWGhoYlhCc1pYTXZhVzFoWjJWekwzTmpZWFIwWlhKZmNHeHZkQS5wbmciLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3NjcyMjU2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=gN-cQ-hsQhK-ndcnpXQk00b6Kc7NuQBS4fR4YEd81fb6z-O18sDQpB3CgcWOiX9GQzLc5E2x5OzhUV6uFDRyqdMOrRfNTiJ7ehzd5QCxsFb3b4~WSoJBMvnL~dksNX2~i-8LoAOiqn1uB2CcAYEBNhkZHIDOJ8THv2jEej-5b20loyPjCCuiSE7vthsvYcgZGCuZjdsZB85URswo1UYWIc-0f5P9fnHJHDCVNkQQuQNobEOB2M6LAtmRf6Ve-EC0Nq0rBSAwvBbkm7xj9huv7lzl609bVnagspShc~0V0HQMzhKRu-uZFKYKqp8k~SY3XERpTuyhyHyAoZBOdFHN2w__)

### 3. 柱状图 (bar)

柱状图用于绘制垂直的柱状图，常用于比较不同类别之间的数值大小。其特点是垂直排列的矩形条，高度表示数值大小。

```python
import matplotlib.pyplot as plt

categories = ['类别A', '类别B', '类别C', '类别D', '类别E']
values = [25, 40, 30, 55, 15]
    
plt.figure(figsize=(8, 6))
plt.bar(categories, values, color='skyblue', edgecolor='navy')
plt.title('柱状图 (Bar Plot)')
plt.xlabel('类别')
plt.ylabel('数值')
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.show()
```

![柱状图示例](https://private-us-east-1.manuscdn.com/sessionFile/rRuTnFWvPRg0shnMgewuiG/sandbox/ReBAfYPehhY63JwGWKQsre-images_1748394494077_na1fn_L2hvbWUvdWJ1bnR1L21hdHBsb3RsaWJfZXhhbXBsZXMvaW1hZ2VzL2Jhcl9wbG90.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvclJ1VG5GV3ZQUmcwc2huTWdld3VpRy9zYW5kYm94L1JlQkFmWVBlaGhZNjNKd0dXS1FzcmUtaW1hZ2VzXzE3NDgzOTQ0OTQwNzdfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwyMWhkSEJzYjNSc2FXSmZaWGhoYlhCc1pYTXZhVzFoWjJWekwySmhjbDl3Ykc5MC5wbmciLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3NjcyMjU2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=rhBGN2SkeEizj-PEKkk9uihdycL1ko1nPpm~MiX8AeNOL3ejzvlRSKaNPqbQGT~e5swxDT5rjXCEmH3a1P6uAgmRmvV~fBKwtFBrDb1lCHRYjL684QPcBVWFfWPjXmhYRvphctX0Ke6bt3PYpD0rDoBp6Y5ZN2nOmBsglj~LI2Xsd5dXhzGq1vnr6H3et7df4Rleig5heCXeKxQnKIBwwzMOZUbMQzwnAD3idr~wrlfIXfgBwbiPucWHO6W46RIzd1k2HAb-kaZNvxwPH2OXlFRD5fy5c2MjWrzFONSjj1i7AwAa7DDAhkfcO5SWReIm98RDOVZGRmq-cjZ4VOSG8w__)

### 4. 水平柱状图 (barh)

水平柱状图用于绘制水平的柱状图，与bar功能相似，但柱条水平排列。其特点是水平排列的矩形条，长度表示数值大小。当类别名称较长时特别有用。

```python
import matplotlib.pyplot as plt

categories = ['类别A', '类别B', '类别C', '类别D', '类别E']
values = [25, 40, 30, 55, 15]
    
plt.figure(figsize=(8, 6))
plt.barh(categories, values, color='lightgreen', edgecolor='darkgreen')
plt.title('水平柱状图 (Horizontal Bar Plot)')
plt.xlabel('数值')
plt.ylabel('类别')
plt.grid(axis='x', linestyle='--', alpha=0.7)
plt.show()
```

![水平柱状图示例](https://private-us-east-1.manuscdn.com/sessionFile/rRuTnFWvPRg0shnMgewuiG/sandbox/ReBAfYPehhY63JwGWKQsre-images_1748394494077_na1fn_L2hvbWUvdWJ1bnR1L21hdHBsb3RsaWJfZXhhbXBsZXMvaW1hZ2VzL2JhcmhfcGxvdA.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvclJ1VG5GV3ZQUmcwc2huTWdld3VpRy9zYW5kYm94L1JlQkFmWVBlaGhZNjNKd0dXS1FzcmUtaW1hZ2VzXzE3NDgzOTQ0OTQwNzdfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwyMWhkSEJzYjNSc2FXSmZaWGhoYlhCc1pYTXZhVzFoWjJWekwySmhjbWhmY0d4dmRBLnBuZyIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTc2NzIyNTYwMH19fV19&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=jLSFol9XK0-JG81RDOp28AtCGVG97myGGST85AID5UPVr~kMiZ1uMy6CCOTseDzPOKx-vKF9tUnc6P81iT-XwayEcNhNxRj5loCKKKzlkuI3dh3fXy-65ao05R4DIa~8He0AxoA4lQDwvUmCDa61xsOqkpgWAWK3HcFMdMeApJD-Y0MsaKl1OjVM~eYAMUwmAQxdOnHNmWhGtjW2MPMq3Ns1MOwbeH9xHradq4F7Kop6-7DAwZW7Tc-B2HkGmPomJdH1uFLe5zT3Ow6mASyCNyVUg1lvg9KmBBIFFTqbFbbGM~ZAM5OEsyZY2iSL4~KXJlTrbqBm9EZBLOz53JSKvQ__)

### 总结

这四种图表类型是数据可视化中最常用的基础图表，可以根据您的数据特点和展示需求灵活选择使用：

- **线图(plot)**: 适合展示连续变化的数据和趋势
- **散点图(scatter)**: 适合展示数据分布和变量间关系
- **柱状图(bar)**: 适合比较不同类别间的数值大小
- **水平柱状图(barh)**: 适合展示类别名称较长的数据比较

## Python Pandas 基础用法

Pandas 是 Python 中一个开源的、功能强大的数据分析和处理库。它提供了两种核心数据结构：`Series` 和 `DataFrame`，使得处理表格化数据变得非常高效和简单。

### 1\. 核心数据结构

首先，你需要导入 pandas 库，通常我们将其简写为 `pd`。

```python
import pandas as pd
import numpy as np
```

#### a. Series (系列)

`Series` 是一个一维的、带标签的数组，可以存储任何数据类型（整数、字符串、浮点数、Python 对象等）。它由数据和与之关联的标签（即 **索引**）组成。

**代码示例：**

```python
# 从一个列表创建一个 Series
s = pd.Series([1, 3, 5, np.nan, 6, 8])

print(s)
```

**结果：**

```
0    1.0
1    3.0
2    5.0
3    NaN
4    6.0
5    8.0
dtype: float64
```

#### b. DataFrame (数据帧)

`DataFrame` 是一个二维的、带标签的数据结构，可以看作是一个表格。它有行索引和列索引，并且每列可以有不同的数据类型。你可以把它想象成一个 Excel 电子表格或一个 SQL 表。

**代码示例：**

```python
# 通过一个字典来创建一个 DataFrame
data = {
    '姓名': ['张三', '李四', '王五', '赵六'],
    '年龄': [28, 34, 29, 42],
    '城市': ['北京', '上海', '广州', '深圳'],
    '工资': [15000, 25000, 20000, 30000]
}
df = pd.DataFrame(data)

print(df)
```

**结果：**

```
   姓名  年龄  城市     工资
0  张三  28  北京  15000
1  李四  34  上海  25000
2  王五  29  广州  20000
3  赵六  42  深圳  30000
```

### 2\. 查看数据

当数据量很大时，查看数据的基本信息和摘要非常重要。

```python
# 查看前 5 行数据 (默认 n=5)
print("--- df.head() ---")
print(df.head())

# 查看后 2 行数据
print("\n--- df.tail(2) ---")
print(df.tail(2))

# 查看 DataFrame 的简要信息（索引、列、非空值、内存使用等）
print("\n--- df.info() ---")
df.info()

# 获取数值列的描述性统计信息
print("\n--- df.describe() ---")
print(df.describe())
```

**结果：**

```
--- df.head() ---
   姓名  年龄  城市     工资
0  张三  28  北京  15000
1  李四  34  上海  25000
2  王五  29  广州  20000
3  赵六  42  深圳  30000

--- df.tail(2) ---
   姓名  年龄  城市     工资
2  王五  29  广州  20000
3  赵六  42  深圳  30000

--- df.info() ---
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 4 entries, 0 to 3
Data columns (total 4 columns):
 #   Column  Non-Null Count  Dtype 
---  ------  --------------  ----- 
 0   姓名      4 non-null      object
 1   年龄      4 non-null      int64 
 2   城市      4 non-null      object
 3   工资      4 non-null      int64 
dtypes: int64(2), object(2)
memory usage: 256.0+ bytes

--- df.describe() ---
             年龄           工资
count   4.000000      4.00000
mean   33.250000  22500.00000
std     5.909031   6454.97224
min    28.000000  15000.00000
25%    28.750000  18750.00000
50%    31.500000  22500.00000
75%    36.000000  26250.00000
max    42.000000  30000.00000
```

-----

### 3\. 数据选择

Pandas 提供了多种灵活的方式来选择数据的子集。

#### a. 选择列

```python
# 选择'姓名'列
print(df['姓名'])
```

**结果：**

```
0    张三
1    李四
2    王五
3    赵六
Name: 姓名, dtype: object
```

### b. 通过标签选择行 (`.loc`)

`loc` 是基于标签（索引名）进行选择的。

```python
# 选择索引为 1 的行
print(df.loc[1])
```

**结果：**

```
姓名        李四
年龄        34
城市        上海
工资     25000
Name: 1, dtype: object
```

#### c. 通过位置选择行 (`.iloc`)

`iloc` 是基于整数位置（从 0 开始）进行选择的。

```python
# 选择第 3 行 (位置索引为 2)
print(df.iloc[2])
```

**结果：**

```
姓名        王五
年龄        29
城市        广州
工资     20000
Name: 2, dtype: object
```

#### d. 条件选择

你可以像过滤数组一样对 DataFrame 进行过滤。

```python
# 选择年龄大于 30 的所有行
print(df[df['年龄'] > 30])
```

**结果：**

```
   姓名  年龄  城市     工资
1  李四  34  上海  25000
3  赵六  42  深圳  30000
```

-----

### 4\. 基本操作

#### a. 添加新列

```python
# 假设我们要添加一个新列'司龄'
df['司龄(年)'] = [5, 10, 3, 12]
print(df)
```

**结果：**

```
   姓名  年龄  城市     工资  司龄(年)
0  张三  28  北京  15000       5
1  李四  34  上海  25000      10
2  王五  29  广州  20000       3
3  赵六  42  深圳  30000      12
```

#### b. 删除列

```python
# 删除'司龄(年)'列
df_after_drop = df.drop(columns=['司龄(年)'])
print(df_after_drop)
```

**结果：**

```
   姓名  年龄  城市     工资
0  张三  28  北京  15000
1  李四  34  上海  25000
2  王五  29  广州  20000
3  赵六  42  深圳  30000
```

### 5\. 常用函数与操作

Pandas 提供了大量内置函数用于数据计算和分析。

#### a. 求和 (`.sum()`)

可以对整个 DataFrame 或单个列进行求和。

```python
# 对所有数值列求和
print("--- 对所有数值列求和 ---")
print(df.sum())

# 只对'工资'列求和
print("\n--- 对'工资'列求和 ---")
print(df['工资'].sum())
```

**结果：**

```
--- 对所有数值列求和 ---
姓名         张三李四王五赵六
年龄              133
城市       北京上海广州深圳
工资            90000
司龄(年)           30
dtype: object

--- 对'工资'列求和 ---
90000
```

*注意：`sum()` 在字符串列上会进行拼接操作。*

#### b. 平均值 (`.mean()`)

计算数值列的平均值。

```python
# 计算'年龄'和'工资'的平均值
print(df[['年龄', '工资']].mean())
```

**结果：**

```
年龄        33.25
工资     22500.00
dtype: float64
```

#### c. 计数 (`.value_counts()`)

统计某一列中各个唯一值出现的次数。

```python
# 假设我们在DataFrame中增加一行，让'北京'出现两次
df_new = pd.concat([df, pd.DataFrame([{'姓名': '孙七', '年龄': 25, '城市': '北京', '工资': 12000, '司龄(年)': 1}])], ignore_index=True)

# 统计'城市'列中每个城市的出现次数
print(df_new['城市'].value_counts())
```

**结果：**

```
北京    2
上海    1
广州    1
深圳    1
Name: 城市, dtype: int64
```

#### d. 排序 (`.sort_values()`)

可以根据一列或多列的值对 DataFrame 进行排序。

```python
# 根据'年龄'升序排序
print(df.sort_values(by='年龄'))

print("\n--- 分割线 --- \n")

# 根据'工资'降序排序
print(df.sort_values(by='工资', ascending=False))
```

**结果：**

```
   姓名  年龄  城市     工资  司龄(年)
0  张三  28  北京  15000       5
2  王五  29  广州  20000       3
1  李四  34  上海  25000      10
3  赵六  42  深圳  30000      12

--- 分割线 --- 

   姓名  年龄  城市     工资  司龄(年)
3  赵六  42  深圳  30000      12
1  李四  34  上海  25000      10
2  王五  29  广州  20000       3
0  张三  28  北京  15000       5
```