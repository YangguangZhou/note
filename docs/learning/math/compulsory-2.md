# 必修二

## 平面向量

### 向量夹角的余弦值

设 \(\vec{a}=(x_1,y_1)\) , \(\vec{b}=(x_2,y_2)\) ，则有： \(\cos \theta = \frac{\vec{a} \cdot \vec{b}}{|\vec{a}||\vec{b}|}\)。
坐标表示：\(\cos \theta = \frac{x_1 x_2 + y_1 y_2}{\sqrt{x_1^2 + y_1^2} \sqrt{x_2^2 + y_2^2}}\)

### 向量的投影

向量 \(\vec{a}\) 在向量 \(\vec{b}\) 上的投影向量为： \( |\vec{a}| \cdot |\vec{b}| \cdot \cos \theta \cdot \frac{\vec{b}}{|\vec{b}|} =  \frac{\left(\vec{a} \cdot \vec{b}\right) \cdot\vec{b}}{|\vec{b}|^2}\)

### 向量平行和垂直的坐标表示

- 向量 \(\vec{a}\) 和 \(\vec{b}\) 平行，当且仅当： \(\vec{a} \times \vec{b} = 0\)。
  坐标表示为： \(x_1 y_2 - y_1 x_2 = 0\)

- 向量 \(\vec{a}\) 和 \(\vec{b}\) 垂直，当且仅当： \(\vec{a} \cdot \vec{b} = 0\)。
  坐标表示为： \(x_1 x_2 + y_1 y_2 = 0\)

### 极化恒等式

对于任意两个向量 \(\vec{a}\) 和 \(\vec{b}\)，有： \(\vec{a} \cdot \vec{b} = (\frac{\vec{a} + \vec{b} }{2})^2 - (\frac{\vec{a} - \vec{b} }{2})^2\)

即两向量数量积等于中线向量的平方减三角形底边一半的平方

### 中线长公式

在三角形 \(ABC\) 中，若 \(D\) 是 \(BC\) 的中点，则有： \( AD^2 = \frac{1}{2}AB^2 + \frac{1}{2}AC^2 - \frac{1}{4}BC^2 \)
 
### 三角形四心的性质

- **重心（G）**：重心是三角形三条中线的交点，且是中线的三等分点
  \(\vec{GA} + \vec{GB} + \vec{GC} = \vec{0}\)

- **垂心（H）**：垂心是三角形三条高的交点
  \(\vec{HA} \cdot \vec{HB} = \vec{HA} \cdot \vec{HC} = \vec{HB} \cdot \vec{HC}\)

- **外心（O）**：外心是三角形三边垂直平分线的交点，且是外接圆的圆心
  \(|\vec{OA}| = |\vec{OB}| = |\vec{OC}|\)

- **内心（I）**：内心是三角形三条角平分线的交点，且是内切圆的圆心
  \(a \cdot \vec{IA} + b \cdot \vec{IB} + c \cdot \vec{IC} = \vec{0}\)

## 立体几何

### 斜二测画法

\( S' = \frac{\sqrt{2}}{4} S \)

\( S = 2 \sqrt{2} S' \)

其中 \(S\) 是原面积，\(S'\) 是斜二测画法画出图形的面积

### 平面

1. **基本事实1** 过不在一条直线上的三个点，有且只有一个平面。
2. **基本事实3** 如果两个不重合的平面有一个公共点，那么它们有且只有一条过该点的公共直线。
3. **推论1** 经过一条直线和这条直线外一点，有且只有一个平面。
4. **推论2** 经过两条相交直线，有且只有一个平面。
5. **推论3** 经过两条平行直线，有且只有一个平面。

### 直线与直线平行

1. **基本事实4** 平行于同一条直线的两条直线平行。
2. **定理** 如果空间中两个角的两条边分别对应平行，那么这两个角相等或互补。

### 直线与平面平行

1. **定理** 如果平面外一条直线与此平面内的一条直线平行，那么该直线与此平面平行。
2. **定理** 一条直线与一个平面平行，如果过该直线的平面与此平面相交，那么该直线与交线平行。

### 平面与平面平行

1. **定理** 如果一个平面内的两条相交直线与另一个平面平行，那么这两个平面平行。
2. **定理** 两个平面平行，如果另一个平面与这两个平面相交，那么两条交线平行。

### 直线与平面垂直

1. **定理** 垂直于同一个平面的两条直线平行。
2. **定理** 如果一条直线与一个平面内的两条相交直线垂直，那么该直线与此平面垂直。

### 平面与平面垂直

1. **定理** 如果一个平面过另一个平面的垂线，那么这两个平面垂直。
2. **定理** 两个平面垂直，如果一个平面内有一直线垂直于这两个平面的交线，那么这条直线与另一个平面垂直。

### 表面积与体积

#### 棱台、圆台、圆锥

\(V_{棱台} = \frac{1}{3} h (S_1 + S_2 + \sqrt{S_1 S_2})\)

\(V_{圆台} = \frac{1}{3} \pi h (r^2 + r r_1 + r_1^2)\)

\(S_{圆台} = \pi (r_1^2 + r^2 + r_1 l + r l)\)

\(V_{圆锥} = \frac{1}{3} \pi r^2 h\)

\(S_{圆锥} = \pi r (r + l)\)

#### 表面积与体积关系

\(V=\frac{1}{3}S_表 r_外\)

类似地， \(S=\frac{1}{2}C r_外\)

### 正四面体

正四面体的高：\(h = \frac{\sqrt{6}}{3} a\)

正四面体的外接球半径：\(R = \frac{\sqrt{6}}{4} a\)

正四面体的内切球半径：\(r = \frac{\sqrt{6}}{12} a\)

正四面体的体积：\(V = \frac{\sqrt{2}}{12} a^3\)

### 二面角

\(\cos\theta = \frac{S_{\text{射}}}{S_{\text{原}}}\)

### 外接球

\(R^2 = r_{底}^2 + \frac{h}{2}^2\)

如果有一个四面体，它的对棱相等，那么 \(R^2 = \frac{x^2 + y^2 + z^2}{8}\)，其中 \(x\)、\(y\)、\(z\) 是三组对棱

如果补出长方体补体，那么 \(R^2 = \frac{a^2 + b^2 + c^2}{4}\)，其中 \(a\)、\(b\)、\(c\) 是长方体的长、宽、高，即可解出 \(x\)、\(y\)、\(z\)

## 统计与概率

### 方差公式

\(S^2 = \frac{1}{n} \sum_{i=1}^{n} (x_i - \bar{x})^2 = \frac{1}{n} \sum_{i=1}^{n} x_i^2 - \bar{x}^2\)

### 变换后的平均数和方差

设 \(x\) 的平均数为 \(\bar{x}\)，方差为 \(S^2\)

则 \(y=ax+b\) 的平均数为 \(\bar{y}=a\bar{x}+b\)，方差为 \(a^2S^2\)