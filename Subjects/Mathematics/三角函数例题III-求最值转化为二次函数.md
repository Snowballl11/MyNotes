## 三角函数例题三 - 求最值转化为二次函数

### 题目:

已知函数 $f(x) = \sin x + \cos x + 2\sin x \cos x + 2$，则（ ）
- A. $f(x)$ 的最大值为 3，最小值为 1
- B. $f(x)$ 的最大值为 3，最小值为 $-1$
- C. $f(x)$ 的最大值为 $3+\sqrt{2}$，最小值为 $\frac{3}{4}$
- D. $f(x)$ 的最大值为 $3+\sqrt{2}$，最小值为 $3-\sqrt{2}$

### 解题步骤：

令 $\sin x + \cos x = t$，$t \in [-\sqrt{2}, \sqrt{2}]$，注意 $t$ 的取值范围。

$\therefore 2 \sin x \cos x = t^2 - 1$

关键是留意到公式 $(\sin x + \cos x)^2 = 1 + 2 \sin x \cos x$

$f(x) = t^2 + t - 1 + 2 = t^2 + t  + 1 = (t + \frac{1}{2})^2 + \frac{3}{4}$

$f_{\max}(x) = \left(\frac{1 + 2 \sqrt{2}}{2}\right)^2 + \frac{3}{4} = \frac{12 + 4 \sqrt{2}}{4} = 3 + \sqrt{2}$

$f_{\min}(x) = \frac{3}{4}$