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

Pandas 是 Python 中一个开源、免费的、功能强大的数据分析和处理库。它提供了两种核心数据结构：`Series` 和 `DataFrame`，使得处理和分析结构化数据（如CSV文件、Excel表格、SQL数据库查询结果等）变得非常高效和简单。

### 1\. 核心数据结构

首先，你需要导入 pandas 库，通常我们将其简写为 `pd`。

```python
import pandas as pd
import numpy as np
```

#### a. Series (系列)

`Series` 是一个**带标签的一维数组**，可以存储任何数据类型（整数、字符串、浮点数、Python 对象等）。它由两部分组成：

  * **数据 (values)**: 一组数据。
  * **索引 (index)**: 与数据相关联的标签，用于查找和识别数据。

如果你不指定索引，Pandas 会自动创建一个从 0 开始的整数索引。

**代码示例：**

```python
# 从列表创建一个 Series (自动生成索引)
s = pd.Series([1, 3, 5, np.nan, 6, 8])
print("--- 自动索引的 Series ---")
print(s)

# 查看 Series 的索引
print("\n--- Series 的索引 ---")
print(s.index)

# 查看 Series 的数据
print("\n--- Series 的数据 ---")
print(s.values)
```

**结果：**

```
--- 自动索引的 Series ---
0    1.0
1    3.0
2    5.0
3    NaN
4    6.0
5    8.0
dtype: float64

--- Series 的索引 ---
RangeIndex(start=0, stop=6, step=1)

--- Series 的数据 ---
[ 1.  3.  5. nan  6.  8.]
```

- 这里的 `dtype: float64` 表示 Series 中存储的数据类型是64位浮点数。因为原始数据中包含 `np.nan` (Not a Number)，整数被自动转换为了浮点数。
- 这里的 `RangeIndex(start=0, stop=6, step=1)` 是程序自动生成的索引，表示索引从 0 开始，到 4 **之前**结束（即到 3 结束），步长为 1

#### b. DataFrame (数据帧)

`DataFrame` 是一个**带标签的二维数据结构**，可以看作是一个电子表格或 SQL 表。它是 Pandas 中最常用的数据结构。其主要特点：

  * 由多个共享相同**行索引**的列组成。
  * 每列可以有不同的数据类型。
  * 同时拥有**行索引 (index)** 和**列索引 (columns)**。

**代码示例：**

```python
# 通过字典创建 DataFrame
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

### 2\. 查看与检查数据

对于大型数据集，首先需要快速了解其概况。

```python
# 查看 DataFrame 的维度 (行数, 列数)
print("--- df.shape ---")
print(df.shape)

# 查看行索引
print("\n--- df.index ---")
print(df.index)

# 查看列名
print("\n--- df.columns ---")
print(df.columns)

# 查看前 5 行数据 (默认 n=5)
print("\n--- df.head() ---")
print(df.head())

# 查看后 2 行数据
print("\n--- df.tail(2) ---")
print(df.tail(2))

# 获取数值列的描述性统计信息
# count: 非空值数量, mean: 平均值, std: 标准差
# min: 最小值, 25%/50%/75%: 四分位数, max: 最大值
print("\n--- df.describe() ---")
print(df.describe())

# 查看 DataFrame 的简要信息
# 包括索引类型、列信息、非空值数量、数据类型和内存使用
print("\n--- df.info() ---")
df.info()
```

**结果：**

```
--- df.shape ---
(4, 4)

--- df.index ---
RangeIndex(start=0, stop=4, step=1)

--- df.columns ---
Index(['姓名', '年龄', '城市', '工资'], dtype='object')

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
memory usage: 272.0+ bytes
```

### 3\. 数据选择与切片

Pandas 提供了多种强大的方式来选择数据的子集。

#### a. 选择列

```python
# 选择'姓名'列，返回一个 Series
print(df['姓名'])

# 选择'姓名'和'城市'两列，返回一个 DataFrame
print("\n--- 选择多列 ---")
print(df[['姓名', '城市']])
```

#### b. 通过标签选择 (`.loc`)

`.loc` **基于标签 (label)** 进行选择，包括行标签和列标签。

```python
# 选择行索引为 1 的行
print("--- 选择单行 ---")
print(df.loc[1])

# 选择行索引为 1 和 3 的行
print("\n--- 选择多行 ---")
print(df.loc[[1, 3]])

# 选择行索引为 1 到 3，列为'姓名'到'城市'的区域
print("\n--- 选择行列区域 ---")
print(df.loc[1:3, '姓名':'城市'])
```

#### c. 通过整数位置选择 (`.iloc`)

`.iloc` **基于整数位置 (integer position)** 进行选择，从 0 开始。

```python
# 选择第 3 行 (位置索引为 2)
print("--- 选择单行 ---")
print(df.iloc[2])

# 选择第 2 行到第 4 行之前 (不包括第4行) 的数据
print("\n--- 切片选择行 ---")
print(df.iloc[1:4])

# 选择第 2 行、第 1 列的数据 (年龄)
print("\n--- 选择单个数据 ---")
print(df.iloc[1, 1])
```

#### d. 条件选择

利用布尔条件过滤数据，这是数据分析中最常用的操作之一。

```python
# 选择年龄大于 30 的所有行
print("--- 单一条件 ---")
print(df[df['年龄'] > 30])

# 选择城市为'北京'或'深圳'的行
print("\n--- 多个 or 条件 ---")
print(df[df['城市'].isin(['北京', '深圳'])])

# 选择年龄大于 30 且工资高于 20000 的行
# 注意：多个条件要用 & (与) 或 | (或) 连接，且每个条件要用括号括起来
print("\n--- 多个 and 条件 ---")
print(df[(df['年龄'] > 30) & (df['工资'] > 20000)])
```

### 4\. 修改与操作数据

#### a. 添加新列

```python
# 添加一个新列'司龄(年)'
df['司龄(年)'] = [5, 10, 3, 12]

# 基于现有列计算新列
df['月薪(千元)'] = df['工资'] / 1000
print(df)
```

#### b. 删除列或行 (`.drop()`)

```python
# 删除'月薪(千元)'列
# axis=1 表示操作对象是列
df_after_drop = df.drop(columns=['月薪(千元)'])
print("--- 删除列后 ---")
print(df_after_drop)

# 删除索引为 0 和 2 的行
# axis=0 表示操作对象是行
df_after_drop_rows = df.drop([0, 2], axis=0)
print("\n--- 删除行后 ---")
print(df_after_drop_rows)
```

*注意：`.drop()` 操作默认返回一个新的 DataFrame，原始 `df` 不变。如果想在原始 `df` 上直接修改，可以使用 `inplace=True` 参数。*

### 5\. 常用函数与操作

#### a. 排序 (`.sort_values()`)

```python
# 根据'年龄'升序排序 (默认)
print("--- 按年龄升序 ---")
print(df.sort_values(by='年龄'))

# 根据'工资'降序排序
print("\n--- 按工资降序 ---")
print(df.sort_values(by='工资', ascending=False))
```

#### b. 计数 (`.value_counts()`)

统计某一列中各个唯一值出现的次数，非常适合分类数据。

```python
# 假设我们扩展一下数据
df_new = pd.concat([df, pd.DataFrame([{'姓名': '孙七', '年龄': 25, '城市': '北京', '工资': 12000, '司龄(年)': 1, '月薪(千元)': 12.0}])], ignore_index=True)

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

#### c. 分组聚合 (`.groupby()`)

`groupby` 是 Pandas 最强大的功能之一，它遵循 "分割-应用-合并" (Split-Apply-Combine) 的思想。

```python
# 按'城市'分组，并计算每座城市员工的平均年龄和平均工资
city_stats = df_new.groupby('城市')[['年龄', '工资']].mean()
print(city_stats)
```

**结果：**

```
         年龄      工资
城市                
上海  34.000000  25000.0
广州  29.000000  20000.0
深圳  42.000000  30000.0
北京  26.500000  13500.0
```