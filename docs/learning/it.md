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
