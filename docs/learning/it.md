---
level: secret
---

# 信息技术

## Matplotlib 常用图表类型

Matplotlib 库中四种常见的图表类型：线图(plot)、散点图(scatter)、柱状图(bar)和水平柱状图(barh)。

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

### 1. 核心数据结构

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

### 2. 查看与检查数据

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

### 3. 数据选择与切片

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

### 4. 修改与操作数据

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

### 5. 常用函数与操作

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

## Python 中 range 的用法

`range()` 是 Python 内置的一个函数，用于生成一个不可变的整数序列。

`range()` 函数有三种主要的用法：

#### 1. `range(stop)`

当只提供一个参数时，`range()` 会生成一个从 `0` 开始，到 `stop - 1` 结束的整数序列。

  * **参数**:
      * `stop`: 序列的结束值（不包含该值）。

**代码示例：**

```python
# 生成从 0 到 4 (5-1) 的整数
for i in range(5):
    print(i, end=' ') # 输出: 0 1 2 3 4
```

#### 2. `range(start, stop)`

当提供两个参数时，`range()` 会生成一个从 `start` 开始，到 `stop - 1` 结束的整数序列。

  * **参数**:
      * `start`: 序列的起始值（包含该值）。
      * `stop`: 序列的结束值（不包含该值）。

**代码示例：**

```python
# 生成从 2 到 6 (7-1) 的整数
for i in range(2, 7):
    print(i, end=' ') # 输出: 2 3 4 5 6
```

#### 3. `range(start, stop, step)`

当提供三个参数时，`range()` 可以控制序列中数字之间的步长。

  * **参数**:
      * `start`: 序列的起始值（包含该值）。
      * `stop`: 序列的结束值（不包含该值）。
      * `step`: 序列中相邻两个数字之间的差值（步长）。它可以是负数，用于生成递减序列。

**代码示例：**

```python
# 生成从 1 到 10，步长为 2 的整数
for i in range(1, 10, 2):
    print(i, end=' ') # 输出: 1 3 5 7 9

print("\n" + "="*20)

# 生成从 10 到 1，步长为 -2 的递减整数
for i in range(10, 0, -2):
    print(i, end=' ') # 输出: 10 8 6 4 2
```

**总结**

  * `range()` 生成的是整数，不支持浮点数。
  * 结束值 `stop` 永远不会被包含在生成的序列中。
  * `step` 的默认值为 `1`。如果 `step` 为 `0`，会引发错误。
  * `range()` 返回的是一个 `range` 对象，它是一个可迭代对象，而不是列表。如果需要列表，可以使用 `list(range(5))` 来转换。

## 图片、视频、音频的大小计算方法

#### 基础：存储单位换算

首先，需要明确计算机存储的基本单位及其换算关系：

  * **位 (bit)**: 数据的最小单位，表示一个 0 或 1。
  * **字节 (Byte)**: 计算机中最常用的基本单位，$1 \text{ Byte} = 8 \text{ bits}$。
  * **千字节 (KB)**: $1 \text{ KB} = 1024 \text{ Bytes}$
  * **兆字节 (MB)**: $1 \text{ MB} = 1024 \text{ KB}$
  * **吉字节 (GB)**: $1 \text{ GB} = 1024 \text{ MB}$

-----

### 1. 图片大小计算（未压缩）

一张未经压缩的位图（BMP）图像，其存储大小由**分辨率**和**色彩深度**决定。

  * **分辨率**: 指图像的宽度和高度的像素点数量，例如 $1920 \times 1080$。
  * **色彩深度 (位深度)**: 指存储每个像素颜色信息所需要的二进制位数。
      * **8 位 (bit)**: 可以表示 $2^8 = 256$ 种颜色（常用于灰度图）。
      * **16 位 (bit)**: 可以表示 $2^{16} = 65536$ 种颜色（高彩色）。
      * **24 位 (bit)**: 可以表示 $2^{24} \approx 1670$ 万种颜色（真彩色），这是最常见的。
      * **32 位 (bit)**: 通常是 24 位真彩色加上 8 位的 Alpha 通道（用于表示透明度）。

**计算公式：**
\(
\text{图片大小(bits)} = \text{图像宽度(像素)} \times \text{图像高度(像素)} \times \text{色彩深度(bits)}
\)
\(
\text{图片大小(Bytes)} = \frac{\text{图片大小(bits)}}{8}
\)

**示例：**
一张分辨率为 $1024 \times 768$、色彩深度为 24 位的 BMP 图像，其大小是多少？

1.  **计算总像素数**: $1024 \times 768 = 786432$ 像素。
2.  **计算总位数**: $786432 \text{ 像素} \times 24 \text{ bits/像素} = 18,874,368 \text{ bits}$。
3.  **换算为字节**: $18,874,368 \text{ bits} / 8 = 2,359,296 \text{ Bytes}$。
4.  **换算为 KB 和 MB**:
      * $2,359,296 \text{ Bytes} / 1024 = 2304 \text{ KB}$。
      * $2304 \text{ KB} / 1024 = 2.25 \text{ MB}$。

### 2. 音频大小计算

一个未经压缩的音频文件，其存储大小由**采样频率**、**采样位数**、**声道数**和**时长**共同决定。

  * **采样频率 (Hz)**: 每秒钟对声音信号进行采集的次数。频率越高，声音的还原度越高。CD 音质通常为 $44100 \text{ Hz}$。
  * **采样位数 (bit)**: 即样本大小，表示每次采样所用的二进制位数。位数越多，声音的动态范围和精度越高。CD 音质通常为 16 位。
  * **声道数**: 录制声音的音轨数量。单声道为 1，立体声为 2。

**计算公式：**
\(
\text{音频大小(bits)} = \text{采样频率(Hz)} \times \text{采样位数(bits)} \times \text{声道数} \times \text{时长(秒)}
\)
\(
\text{音频大小(Bytes)} = \frac{\text{音频大小(bits)}}{8}
\)

**示例：**
一段时长为 1 分钟、采样频率为 $44.1 \text{ kHz}$ (即 $44100 \text{ Hz}$)、采样位数为 16 位、双声道的 WAV 音频，其大小是多少？

1.  **统一单位**: 时长 $1 \text{ 分钟} = 60 \text{ 秒}$。
2.  **计算每秒数据量(bits)**: $44100 \text{ Hz} \times 16 \text{ bits} \times 2 \text{ (声道)} = 1,411,200 \text{ bits/s}$。
3.  **计算总大小(bits)**: $1,411,200 \text{ bits/s} \times 60 \text{ s} = 84,672,000 \text{ bits}$。
4.  **换算为字节**: $84,672,000 \text{ bits} / 8 = 10,584,000 \text{ Bytes}$。
5.  **换算为 MB**: $10,584,000 \text{ Bytes} / 1024 / 1024 \approx 10.1 \text{ MB}$。

### 3. 视频大小计算

视频文件通常是经过压缩的，其大小主要由**码率（比特率）** 和 **时长**决定。视频文件包含视频流和音频流。

  * **码率 (Bitrate)**: 指在单位时间内传输或处理的比特数量，通常用 `kbps`（千比特每秒）或 `Mbps`（兆比特每秒）表示。码率越高，画面和声音的质量越好，文件也越大。

**计算公式：**
\(
\text{文件大小(bits)} = (\text{视频码率(bps)} + \text{音频码率(bps)}) \times \text{时长(秒)}
\)
注意：$1 \text{ kbps} = 1000 \text{ bps}$，而不是 1024。

**示例：**
一部时长为 90 分钟的电影，视频码率为 $2000 \text{ kbps}$，音频码率为 $128 \text{ kbps}$，其大小约是多少？

1.  **统一单位**:
      * 时长: $90 \text{ 分钟} \times 60 \text{ 秒/分钟} = 5400 \text{ 秒}$。
      * 总码率: $2000 \text{ kbps} + 128 \text{ kbps} = 2128 \text{ kbps} = 2,128,000 \text{ bps}$。
2.  **计算总大小(bits)**: $2,128,000 \text{ bps} \times 5400 \text{ s} = 11,491,200,000 \text{ bits}$。
3.  **换算为字节**: $11,491,200,000 \text{ bits} / 8 = 1,436,400,000 \text{ Bytes}$。
4.  **换算为 GB**: $1,436,400,000 \text{ Bytes} / 1024 / 1024 / 1024 \approx 1.34 \text{ GB}$。

## Excel 常用函数用法

### 1. IF 函数

**作用**：根据指定的条件判断，如果条件为真，则返回一个值；如果条件为假，则返回另一个值。

**语法**：`=IF(logical_test, value_if_true, value_if_false)`

  * `logical_test`：要评估的条件（例如 `A1>60`）。
  * `value_if_true`：当条件为真时返回的值。
  * `value_if_false`：当条件为假时返回的值。

**示例**：判断 B2 单元格的成绩是否及格（假设及格线为 60 分）。
`=IF(B2>=60, "及格", "不及格")`
如果 B2 的值是 75，公式将返回 "及格"；如果是 59，则返回 "不及格"。

### 2. SUMIF 函数

**作用**：对满足单个条件的单元格区域进行求和。

**语法**：`=SUMIF(range, criteria, [sum_range])`

  * `range`：要应用条件的单元格区域。
  * `criteria`：用于确定哪些单元格将被求和的条件（可以是数字、文本或表达式，如 `"水果"` 或 `">100"`）。
  * `[sum_range]`：（可选）实际要求和的单元格区域。如果省略，则对 `range` 参数中的单元格求和。

**示例**：计算 A 列中 "水果" 类别的销售总额（销售额在 B 列）。
`=SUMIF(A2:A10, "水果", B2:B10)`
该公式会查找 A2 到 A10 区域中所有值为 "水果" 的单元格，并将 B 列对应行的数值相加。

### 3. COUNT 函数

**作用**：计算包含数字的单元格的数量。

**语法**：`=COUNT(value1, [value2], ...)`

  * `value1`, `value2`, ...：要计算其中数字的单元格或区域。

**示例**：计算 A1 到 A10 区域中包含数字的单元格有多少个。
`=COUNT(A1:A10)`
如果 A1 是数字 5，A2 是文本 "你好"，A3 是数字 10，则结果为 2。它会忽略文本和空白单元格。

### 4. COUNTIF 函数

**作用**：计算区域内符合单个指定条件的单元格的数量。

**语法**：`=COUNTIF(range, criteria)`

  * `range`：要进行计数的单元格区域。
  * `criteria`：定义计数条件的标准（例如 `"是"` 或 `">50"`）。

**示例**：计算 A2 到 A10 区域中，"苹果" 出现了多少次。
`=COUNTIF(A2:A10, "苹果")`

### 5. AVERAGEIF 函数

**作用**：计算区域中满足单个给定条件的所有单元格的平均值。

**语法**：`=AVERAGEIF(range, criteria, [average_range])`

  * `range`：要应用条件的单元格区域。
  * `criteria`：用于确定哪些单元格将被计算平均值的条件。
  * `[average_range]`：（可选）要计算平均值的实际单元格区域。如果省略，则对 `range` 参数中的单元格计算平均值。

**示例**：计算 A 列中 "蔬菜" 类别的平均销售额（销售额在 B 列）。
`=AVERAGEIF(A2:A10, "蔬菜", B2:B10)`
该公式会找到 A 列中所有 "蔬菜" 的条目，并计算 B 列中对应销售额的平均值。