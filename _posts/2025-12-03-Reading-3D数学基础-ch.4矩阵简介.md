---
layout: post
title: "Reading: 3D数学基础 ch. 4 矩阵简介"
date: 2025-12-03
---

### 矩阵维度和表示方法

r行c列的矩阵(Matrix)，称为是r x c矩阵。具有相同行数与列数的矩阵称为方形矩阵(Square Matrix)，方阵的对角元素(Diagonal Elements)是行和列索引相同的元素，其他的元素是非对角元素(Non-Diagonal Elements)。

如果一个矩阵中所有的非对角元素都为0，则该矩阵为对角矩阵(Diagonal Matrix)。有一类特殊的对角矩阵是单位矩阵(Identity Matrix)。维度为n的单位矩阵，表示I<sub>n</sub>，是n x n的矩阵，其对角线上的值为1，其他元素均为0。当矩阵的行或列为1时，1 x n矩阵称为行矢量(Row Vector)，n x 1矩阵称为列矢量(Column Vector)。

给定r x c的矩阵M，M的转置(Transpose)表示为M<sup>T</sup>，是c x r矩阵，其中列由M的行构成，M<sub>ij</sub>=M<sup>T</sup><sub>ji</sub>，这实际上是以对角进行翻转的矩阵。

### 矩阵相乘

矩阵M可以与标量k相乘，得到与M相同维度的矩阵。M = [m1, m2, m3]; kM = k[m1, m2, m3] = [km1, km2, km3]。

在某些情况下，可以将两个矩阵相乘，一个**r x n**的矩阵A可以乘一个**n x c**的矩阵B，结果是一个**r x c**的矩阵。矩阵的乘法计算方式为，一个r x n的矩阵A乘n x c的矩阵B，得到r x n的矩阵C，C中的每个元素c<sub>ij</sub>等于$\sum_{k=1}^n{a_{ik}}{b_{kj}}，比如c<sub>24</sub>等于A 2行和B 4列中元素的点积(a<sub>21</sub>b<sub>14</sub> + a<sub>22</sub>b<sub>42</sub>+...+a<sub>2k</sub>b<sub>k4</sub>)。

将任何一个矩阵M乘一个方形矩阵S将得到与M大小相同的矩阵(前提是允许相乘)，如果S是单位矩阵I，结果是原始矩阵M：MI = IM = M。

矩阵乘法是不可交换的，一般来说AB != BA，但矩阵乘法是可以结合的，(AB)C = A(BC)。(AB)<sup>T</sup> = B<sup>T</sup>A<sup>T</sup>，这可以拓展到2个以上的矩阵。

矢量与矩阵相乘时，行矢量在左侧，列矢量在右侧。

### 矩阵的几何解释

一般来说，方形矩阵可以描述任何线性变换(Linear Transformation)。包括：旋转(Rotation)，比例缩放(Scale)，正交投影(Orthographic Projection)，反射(Reflection)，错切(Shearing)。

---

<small>3D Math Primer for Graphics and Game Development, 2nd Edition</small>
<small>by Fletcher Dunn, Ian Parberry</small>
<small>Nov 2011</small>
<small>ISBN: 9781439869819</small>
