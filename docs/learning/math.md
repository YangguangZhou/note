# 数学公式整理

为了更好的阅读和理解，以下公式按类别进行了整理，包括对数的运算法则和三角函数的公式。

## 对数的运算法则

1. 对数乘法法则： \(\log_a(bc) = \log_a b + \log_a c\)
2. 对数除法法则： \(\log_a\frac{b}{c} = \log_a b - \log_a c\)
3. 对数幂法则：   \(\log_a b^c = c \log_a b\)
4. 对数换底法则： \(\log_a b = \frac{\log_c b}{\log_c a}\)

## 三角函数公式

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
    - \(\sin\alpha \pm \sin\beta = 2\sin\frac{1}{2}(\alpha \pm \beta)\cos\frac{1}{2}(\alpha \mp \beta)\)
    - \(\cos\alpha + \cos\beta = 2\cos\frac{1}{2}(\alpha + \beta)\cos\frac{1}{2}(\alpha - \beta)\)
    - \(\cos\alpha - \cos\beta = -2\sin\frac{1}{2}(\alpha + \beta)\sin\frac{1}{2}(\alpha - \beta)\)

### 倍角公式和半角公式
1. 倍角公式
    - \(\sin 2\alpha = 2\sin\alpha\cos\alpha\)
    - \(\cos 2\alpha = \cos^2\alpha - \sin^2\alpha = 2\cos^2\alpha - 1 = 1 - 2\sin^2\alpha\)
    - \(\tan 2\alpha = \frac{2\tan\alpha}{1 - \tan^2\alpha}\)

2. 半角公式
    - \(\sin\frac{\alpha}{2} = \pm\sqrt{\frac{1 - \cos\alpha}{2}}\)
    - \(\cos\frac{\alpha}{2} = \pm\sqrt{\frac{1 + \cos\alpha}{2}}\)
    - \(\tan\frac{\alpha}{2} = \pm\sqrt{\frac{1 - \cos\alpha}{1 + \cos\alpha}} = \frac{1 - \cos\alpha}{\sin\alpha} = \frac{\sin\alpha}{1 + \cos\alpha}\)
