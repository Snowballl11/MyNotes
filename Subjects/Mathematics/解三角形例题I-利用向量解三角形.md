## 解三角形例题I

### 已知条件

在三角形ABC中：
1. 内角A, B, C的对边分别为a, b, c
2. $b^2 = ac$
3. D在边AC上
4. $BD \sin \angle ABC = a \sin C$
5. $AD = 2DC$

### 求解步骤

1. 利用已知条件，得到向量关系：
   $\overrightarrow{BD} = \frac{2}{3}\overrightarrow{BC} + \frac{1}{3}\overrightarrow{BA}$

2. 整理得到方程：
   $6a^2 - 11ac + 3c^2 = 0$

3. 因式分解：
   $(2a - 3c)(3a - c) = 0$

4. 解得：
   $a = \frac{3}{2}c$ 或 $a = \frac{1}{3}c$

5. 验证哪个解满足三角形边长关系：
   - 当 $a = \frac{3}{2}c$ 时：
     $b^2 = ac = \frac{3}{2}c^2$，即 $b = c\sqrt{\frac{3}{2}}$
     验证三角形不等式：$a + b > c$，$\frac{3}{2}c + c\sqrt{\frac{3}{2}} > c$ 成立
   - 当 $a = \frac{1}{3}c$ 时：
     $b^2 = ac = \frac{1}{3}c^2$，即 $b = \frac{c}{\sqrt{3}}$
     验证三角形不等式：$a + b = \frac{1}{3}c + \frac{c}{\sqrt{3}} \approx 0.91c < c$，不成立

6. 确定正确的边长关系：$a = \frac{3}{2}c$，$b = c\sqrt{\frac{3}{2}}$

7. 使用余弦定理计算 $\cos \angle ABC$：
   $\cos B = \frac{a^2 + c^2 - b^2}{2ac}$

8. 代入已知关系：
   $\cos B = \frac{(\frac{3}{2}c)^2 + c^2 - (\frac{3}{2}c^2)}{2 \cdot \frac{3}{2}c \cdot c} = \frac{\frac{9}{4}c^2 + c^2 - \frac{3}{2}c^2}{3c^2} = \frac{\frac{7}{4}c^2}{3c^2} = \frac{7}{12}$

### 结论

$\cos \angle ABC = \frac{7}{12}$