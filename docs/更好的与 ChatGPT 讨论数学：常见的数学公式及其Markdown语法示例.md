<img alt="picture 0" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/abd24e1c01cb0fc467286484187eb915f5606482c13afcf331b446d9c12cb9f7.jpg" width="600" />  

# 更好的与 ChatGPT 讨论数学：常见的数学公式及其Markdown语法示例
> 日期：2024年5月28日

本文的行内 latex 语法展示，离不开 [Equation Render](https://latex.codecogs.com) 的技术支持。

在与ChatGPT聊天的过程中，为了让GPT能看懂我们的数学公式，我们可以利用Markdown中的 Latex 语法和GPT进行聊天。

在Markdown中嵌入LaTeX数学公式，可以使用美元符号`$`或双美元符号`$$`来包围公式。以下是一些常见的数学公式及其Markdown语法示例：

### 行内公式
行内公式使用单个美元符号`$`包围。

```这是一个行内公式 $a^2 + b^2 = c^2$。```

效果：这是一个行内公式 <img src = "https://latex.codecogs.com/svg.image?&space;a^2&plus;b^2=c^2">

### 独立公式
独立公式使用双美元符号`$$`包围。
```
$$
E = mc^2
$$
```
效果：

$$
E = mc^2
$$

### 分数

```
行内分数：$ \frac{a}{b} $

独立分数：

$$
\frac{a}{b}
$$
```

效果：

行内分数：
<img src="https://latex.codecogs.com/svg.image?\frac{a}{b}">

独立分数：
$$
\frac{a}{b}
$$

### 上标和下标
```
上标：$ a^2 $

下标：$ a_i $
```
效果：

上标：<img src = "https://latex.codecogs.com/svg.image?a^2">

下标：<img src = "https://latex.codecogs.com/svg.image?a_i">

### 根号
```
行内根号：$ \sqrt{a} $

独立根号：
$$
\sqrt{a}
$$
```

效果：

行内根号：<img src = "https://latex.codecogs.com/svg.image?\sqrt{a}">

独立根号：
$$
\sqrt{a}
$$

### 矩阵
```
$$
\begin{bmatrix}
    a & b \\
    c & d
\end{bmatrix}
$$
```
效果：
$$
\begin{bmatrix}
    a & b \\
    c & d
\end{bmatrix}
$$

### 求和和积分
```
求和：$ \sum_{i=1}^n i $
积分：
$$
\int_{a}^{b} x^2 \, dx
$$
```
效果：

求和：
<img src = "https://latex.codecogs.com/svg.image?\sum_{i=1}^n i">

积分：
$$
\int_{a}^{b} x^2 \, dx
$$

### 带括号的表达式
```
行内表达式：$ (a + b) $

独立表达式：
$$
(a + b)
$$
```
效果：
行内表达式：<img src = "https://latex.codecogs.com/svg.image?\(a+b)">

独立表达式：
$$
(a + b)
$$

### 方程组
```
$$
\begin{cases}
    x + y = 1 \\
    x - y = 2
\end{cases}
$$
```
效果：
$$
\begin{cases}
    x + y = 1 \\
    x - y = 2
\end{cases}
$$

### 极限
```行内极限：$ \lim_{x \to \infty} f(x) $

独立极限：
$$
\lim_{x \to \infty} f(x)
$$
```
效果：

行内极限：<img src = "https://latex.codecogs.com/svg.image?\lim_{x \to \infty} f(x)">

独立极限：
$$
\lim_{x \to \infty} f(x)
$$

这些是Markdown中常见的LaTeX数学公式语法示例。可以在支持LaTeX的Markdown编辑器（如Jupyter Notebook、Typora、GitHub Markdown等）中试用这些语法。
