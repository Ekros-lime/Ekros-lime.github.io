---
layout: post
title: "Reading: 3D数学基础 ch. 5 矩阵和线性变换 p1"
date: 2025-12-05
---

### 旋转
**在二维中的旋转**: 在二维中，实际上只能进行一种围绕一个点的旋转，在这里我们进行进一步的范围限制，即围绕原点进行旋转。围绕原点进行的二维旋转仅有一个参数，即角度θ。p(1,0)围绕原点旋转后是p'(cosθ,sinθ)，q(0,1)围绕原点旋转后是q'(-sinθ,cosθ)，即二维旋转矩阵R(θ)=[cosθ,sinθ]\[-sinθ,cosθ]。
**在三维中的旋转**: 在三维中，旋转发生在一个轴上而不是一个点上，根据上一章节的内容，当围绕x轴旋转时，x的坐标不变，即旋转矩阵R<sub>x</sub>(θ)=[1,0,0]\[0,cosθ,sinθ][0,-sinθ,cosθ]，y轴和z轴的旋转矩阵也有相同的原理。
### 缩放
在x，y，z轴方向上独立的缩放k<sub>x</sub>，k<sub>y</sub>，k<sub>z</sub>。可以看作是[1,0,0]\[0,1,0][0,0,1]与对应的k相乘进行的缩放，因此缩放矩阵可以是[k<sub>x</sub>,0,0]\[0,k<sub>y</sub>,0][0,0,k<sub>z</sub>]。

---

<small>3D Math Primer for Graphics and Game Development, 2nd Edition</small>
<small>by Fletcher Dunn, Ian Parberry</small>
<small>Nov 2011</small>
<small>ISBN: 9781439869819</small>
