# 数学

## 基本不等式

\(
\begin{cases}
a^2 + b^2 \geq 2ab \\
\frac{(a+b)^2}{4} \geq ab \\
a+b \geq 2\sqrt{ab}
\end{cases}
\)

### “调几算方”

调和平均数 \(\geq\) 几何平均数 \(\geq\) 算术平均数 \(\geq\) 平方根平均数

\( \frac{2}{\frac{1}{a}+\frac{1}{b}} \leq \sqrt{ab} \leq \frac{a+b}{2} \leq \sqrt{\frac{a^2+b^2}{2}} \)

## 对数的运算法则

1. 对数乘法法则： \(\log_a(bc) = \log_a b + \log_a c\)
2. 对数除法法则： \(\log_a\frac{b}{c} = \log_a b - \log_a c\)
3. 对数幂法则：   \(\log_a b^c = c \log_a b\)
4. 对数换底法则： \(\log_a b = \frac{\log_c b}{\log_c a}\)

### 推论：

1. \(\log_a \frac{1}{M} = -\log_a M\)
2. \(\log_a \sqrt[p]{M^n} = \frac{n}{p}\log_a M\)
3. \(\log_a b = \frac{1}{\log_b a}\)
4. \(a^{\log_b c} = c^{\log_b a}\)

## 三角函数

\(\sin^2\alpha+\cos^2\alpha=1\)

### 基础公式

1. \(\sin(\theta + 2k\pi) = \sin \theta\)
2. \(\cos(\theta + 2k\pi) = \cos \theta\)
3. \(\tan(\theta + k\pi) = \tan \theta\)

其中，\(k \in \mathbb{Z}\)

### 三角函数诱导公式

1. 第一组:
    - \(\sin(\pi - \theta) = \sin \theta\)
    - \(\cos(\pi - \theta) = -\cos \theta\)
    - \(\tan(\pi - \theta) = -\tan \theta\)

2. 第二组:
    - \(\sin(\pi + \theta) = -\sin \theta\)
    - \(\cos(\pi + \theta) = -\cos \theta\)
    - \(\tan(\pi + \theta) = \tan \theta\)

3. 第三组:
    - \(\sin(2\pi - \theta) = -\sin \theta\)
    - \(\cos(2\pi - \theta) = \cos \theta\)
    - \(\tan(2\pi - \theta) = -\tan \theta\)

4. 第四组:
    - \(\sin(-\theta) = -\sin \theta\)
    - \(\cos(-\theta) = \cos \theta\)
    - \(\tan(-\theta) = -\tan \theta\)

5. 第五组:
    - \(\sin\left(\frac{\pi}{2} - \theta\right) = \cos \theta\)
    - \(\cos\left(\frac{\pi}{2} - \theta\right) = \sin \theta\)
    - \(\tan\left(\frac{\pi}{2} - \theta\right) = \frac{1}{\tan \theta}\)

6. 第六组:
    - \(\sin\left(\frac{\pi}{2} + \theta\right) = \cos \theta\)
    - \(\cos\left(\frac{\pi}{2} + \theta\right) = -\sin \theta\)
    - \(\tan\left(\frac{\pi}{2} + \theta\right) = -\frac{1}{\tan \theta}\)


### 三角函数的性质

#### 基本三角函数

| 函数 | 对称轴 | 对称中心 | 单调递增区间 | 单调递减区间 | 奇偶性 | 零点 |
| --- | --- | --- | --- | --- | --- | --- |
| \( y = \sin x \) | \( x = k\pi + \frac{\pi}{2} \) | \( (k\pi, 0) \) | \( [2k\pi - \frac{\pi}{2}, 2k\pi + \frac{\pi}{2}] \) | \( [2k\pi + \frac{\pi}{2}, 2k\pi + \frac{3\pi}{2}] \) | 奇函数 | \( x = k\pi \) |
| \( y = \cos x \) | \( x = k\pi \) | \( \left(k\pi + \frac{\pi}{2}, 0\right) \) | \( [2k\pi, 2k\pi + \pi] \) | \( [2k\pi + \pi, 2k\pi + 2\pi] \) | 偶函数 | \( x = k\pi + \frac{\pi}{2} \) |
| \( y = \tan x \) | 无 | \( (k\pi, 0) \) | \( \left(k\pi - \frac{\pi}{2}, k\pi + \frac{\pi}{2}\right) \) | 无 | 奇函数 | \( x = k\pi \) |

其中，\( k \in \mathbb{Z} \)

#### 奇偶性

三角函数形如 \( f(x) = A \sin(\omega x + \varphi) \) 的奇偶性：

1. \( f(x) \) 为奇函数 \( \Leftrightarrow \) \( \varphi = k\pi \)
2. \( f(x) \) 为偶函数 \( \Leftrightarrow \) \( \varphi = -\frac{\pi}{2} + k\pi \)

其中，\(k \in \mathbb{Z}\)

#### 周期性

一般地，若函数  \( f(x) \) 的周期为 \(T\)，则函数 \( y = f(\omega x) \) 的周期为 \( \frac{T}{|\omega|} \)

特殊地，函数 \( y = A \sin(\omega x + \varphi) \) 或 \( y = A \cos(\omega x + \varphi) \) 的周期 \( T = \frac{2\pi}{|\omega|} \)，函数 \( y = A \tan(\omega x + \varphi) \) 的周期 \( T = \frac{\pi}{|\omega|} \)

### 和差角公式

1. \(\sin(\alpha \pm \beta) = \sin\alpha\cos\beta \pm \cos\alpha\sin\beta\)
2. \(\cos(\alpha \pm \beta) = \cos\alpha\cos\beta \mp \sin\alpha\sin\beta\)
3. \(\tan(\alpha \pm \beta) = \frac{\tan\alpha \pm \tan\beta}{1 \mp \tan\alpha\tan\beta}\)

### 和差化积与积化和差公式 

1. 两角和（或差）与两角积之间的关系
    - \(\sin\alpha\cos\beta = \frac{1}{2}[\sin(\alpha - \beta)+\sin(\alpha + \beta)]\)
    - \(\cos\alpha\sin\beta = \frac{1}{2}[\sin(\alpha - \beta) - \sin(\alpha + \beta)]\)
    - \(\cos\alpha\cos\beta = \frac{1}{2}[\cos(\alpha - \beta)+\cos(\alpha + \beta)]\)
    - \(\sin\alpha\sin\beta = -\frac{1}{2}[\cos(\alpha - \beta) - \cos(\alpha + \beta)]\)

2. 两角积与两角和（或差）之间的关系
    - \(\sin\alpha \pm \sin\beta = 2\sin\frac{\alpha \pm \beta}{2}\cos\frac{\alpha \mp \beta}{2}\)
    - \(\cos\alpha + \cos\beta = 2\cos\frac{\alpha + \beta}{2}\cos\frac{\alpha - \beta}{2}\)
    - \(\cos\alpha - \cos\beta = -2\sin\frac{\alpha + \beta}{2}\sin\frac{\alpha - \beta}{2}\)

### 倍角公式和半角公式
1. 倍角公式
    - \(\sin 2\alpha = 2\sin\alpha\cos\alpha\)
    - \(\cos 2\alpha = \cos^2\alpha - \sin^2\alpha = 2\cos^2\alpha - 1 = 1 - 2\sin^2\alpha\)
    - \(\tan 2\alpha = \frac{2\tan\alpha}{1 - \tan^2\alpha}\)

2. 半角公式
    - \(\sin\frac{\alpha}{2} = \pm\sqrt{\frac{1 - \cos\alpha}{2}}\)
    - \(\cos\frac{\alpha}{2} = \pm\sqrt{\frac{1 + \cos\alpha}{2}}\)
    - \(\tan\frac{\alpha}{2} = \pm\sqrt{\frac{1 - \cos\alpha}{1 + \cos\alpha}} = \frac{1 - \cos\alpha}{\sin\alpha} = \frac{\sin\alpha}{1 + \cos\alpha}\)

    !!! note "降幂公式"
        - \(\sin^2\alpha = \frac{1 - \cos 2\alpha}{2}\)
        - \(\cos^2\alpha = \frac{1 + \cos 2\alpha}{2}\)
        - \(\tan^2\alpha = \frac{1 - \cos 2\alpha}{1 + \cos 2\alpha}\)

### 万能公式

1. \(\sin2\alpha = \frac{2\tan\alpha}{1+\tan^2\alpha}\)
2. \(\cos2\alpha = \frac{1-\tan^2\alpha}{1+\tan^2\alpha}\)
3. \(\cos^4\alpha+\sin^4\alpha=\cos2\alpha\)
4. \(\cos^4\alpha-\sin^4\alpha=1-\frac{1}{2}\sin^2 2\alpha=\frac{3}{4}+\frac{1}{4}\cos4\alpha\)

### 辅助角公式

\(a\sin\alpha + b\cos\alpha = \sqrt{a^2 + b^2} \sin ( \alpha+\varphi)\)

\(
\begin{cases}
\sin\varphi = \frac{b}{\sqrt{a^2+b^2}} \\
\cos\varphi = \frac{a}{\sqrt{a^2+b^2}} \\
\tan\varphi = \frac{b}{a}
\end{cases}
\)