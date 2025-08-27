## 三角函数例题II - 正弦的半角公式

### 题目：

化简 $\left(\dfrac{1}{\tan \frac{\alpha}{2}} - \tan \frac{\alpha}{2}\right) \cdot \left(1 + \tan \alpha \cdot \tan \frac{\alpha}{2}\right)$。

### 准备工作：

$\tan \frac{\alpha}{2} = \dfrac{\sin \frac{\alpha}{2}}{\cos \frac{\alpha}{2}} \times \dfrac{2 \cos \frac{\alpha}{2}}{2 \cos \frac{\alpha}{2}} = \dfrac{\sin \alpha}{2 \cos^2 \frac{\alpha}{2}} = \dfrac{\sin \alpha}{2 \dfrac{\left(1 + \cos \alpha\right)}{2}} = \dfrac{\sin \alpha}{1 + \cos \alpha} = \dfrac{1 - \cos \alpha}{\sin \alpha}$

### 解题步骤

$
\text{原式} = \left(\dfrac{1+\cos \alpha}{\sin \alpha} - \dfrac{1-\cos \alpha}{\sin \alpha}\right) \left(1 + \tan \alpha \cdot \tan \frac{\alpha}{2}\right)
$

$
= \dfrac{2\cos \alpha}{\sin \alpha} \left(1 + \tan \alpha \cdot \tan \frac{\alpha}{2}\right)
$

$
= \dfrac{2}{\tan \alpha} \left(1 + \tan \alpha \cdot \tan \frac{\alpha}{2}\right), \text{又有} \tan(\alpha - \beta) = \dfrac{\tan \alpha - \tan \beta}{1 + \tan \alpha \tan \beta}
$

$
= \dfrac{2}{\tan \alpha} \cdot \dfrac{\tan \alpha - \tan \frac{\alpha}{2}}{\tan \frac{\alpha}{2}}
$

$
= \dfrac{2}{\tan \frac{\alpha}{2}} - \dfrac{2}{\tan \alpha}, \text{利用} \tan \frac{\alpha}{2} = \dfrac{\sin \alpha}{1 + \cos \alpha}
$

$
= \dfrac{2(1 + \cos \alpha)}{\sin \alpha} - \dfrac{2\cos \alpha}{\sin \alpha} = \dfrac{2}{\sin \alpha}
$