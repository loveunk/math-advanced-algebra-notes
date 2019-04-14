# 丘维声《高等代数》学习笔记

《高等代数》，丘维声，北京大学，视频：共151讲，[B站视频链接](https://www.bilibili.com/video/av39523603)

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [丘维声《高等代数》学习笔记](#丘维声高等代数学习笔记)
	- [前言](#前言)
	- [第一章 线性方程组的解法](#第一章-线性方程组的解法)
		- [1. .1 解线性方程组的矩阵消元法](#1-1-解线性方程组的矩阵消元法)
			- [加减消元法](#加减消元法)
			- [矩阵的初等行变化](#矩阵的初等行变化)
			- [在有理数集内解线性方程组](#在有理数集内解线性方程组)
		- [1.2 线性方程组解的情况及其判别情况](#12-线性方程组解的情况及其判别情况)
		- [1.3 数域](#13-数域)
			- [习题1.3 思路](#习题13-思路)

<!-- /TOC -->

## 前言

> 视频1、2

* n元线性方程组和其解法
* 矩阵的定义（由n元线性方程组的系数得到）
  * 通常由 _A_ 表示
  * 对于线性方程组，可以得到**增广矩阵**
* **高等代数研究对象**：
  * **n元线性方程组**
    * 研究**解的情况的判别**和**解集的结构**
  * **矩阵**
  * **n维向量空间**
  * **线性空间**（由n维向量空间抽象而来）
  * **线性映射**（研究线性空间，就离不开线性映射）
  * **双线性函数**
  * **具有度量的线性空间**
    * 欧几里得空间
    * 酉空间
    * 等等
  * **与度量有关的线性变换**
    * 正交变换
    * 对称变换
    * 酉变换
    * Hermite变换
* **线性代数的主线：**
  * 线性空间
  * 线性映射
* 一元高次方程的求根
  * 一元多项式环
  * 环的概念
  * 域的概念
  * 群的概念
* **数学的思维方式**
  * 观察客观现象
    * 提出研究的问题
    * 抓住主要特征
  * 抽象出概念或建立模型
  * 探索
    * 运用直觉、类比、归纳、联想、推理
  * 猜测（可能的规律）
  * 论证
    * 深入分析
    * 运用定义、公理、已证明的定理进行推理
  * 揭示事物内在规律

## 第一章 线性方程组的解法

### 1. .1 解线性方程组的矩阵消元法

> 视频3、4、5

#### 加减消元法

* 不同方程的乘以系数后和其他方程加减，以消除方程中某个（些）系数
* 如果以矩阵方式来写，把矩阵转换为阶梯型矩阵，即左下角的元素全为0
  * 首先针对矩阵第一列，其次第二列，直到最后一列
* 当主元全是1，其他元素都是0 时，增广矩阵的最后一列即为X的解

#### 矩阵的初等行变化

1. 把一行的倍数加到另外一行
2. 两行互换
3. 一行乘以一个非零系数

**结论**：矩阵的初等行变换得到的解与原方程组同解

作业，习题1.1的1和2

#### 在有理数集内解线性方程组

**有且只有如下三种情况：**

* **无解**：阶梯形方程组无解，从而原方程组无解
  * 视频中的例子是最后一行：_0 x<sub>3</sub>= -2_
* **有无穷多个解**，从而原方程有无穷多个解
  * 视频的例子是最后一行：_0 x<sub>2</sub> = 0_
  * _x<sub>2</sub>_ 是自由未知量（主变量以外的未知量）
  * _x<sub>1</sub>, x<sub>3</sub>_ 是主变量（以主元为系数的未知量）
* **有唯一的解**

当有解的时候，要么有一个解，要么有无穷多个解。

> 从两条直线来考虑这个问题，它们要么相交，要么重叠，要么平行。

**方程组是否有解的总结：**

* 如果线性方程的增广矩阵经过初等变换成阶梯矩阵后
  * 相应的阶梯矩阵方程组如果出现 _0 = d_ （其中 _d_ 是非零数），那么原方程组无解，否则有解。
* 当有解时
  * 若阶梯形矩阵的非零行的数目 _r = n_ （未知量数目），那么方程有唯一解
  * 如 _r < n_，那么方程有无穷多个解。

### 1.2 线性方程组解的情况及其判别情况

> 视频5、6

证明：n元线形方程组的增广矩阵经过初等行变换成阶梯矩阵有 _r_ 个非零行，显然有 _n + 1_ 列。

* 情况1： *"0 = d"*，无解
* 情况2： 不出现*"0 = d"*
  * 由于 _J_ 的第 _r_ 个主元 _b<sub>rt</sub>_ 不能位于第 _n+1_ 列，因此 _t ≤ n_
  * 因为只能位于对角线的右上方，所以有 _t ≥ r_
  * 情况 2.1：_r = n_
    * _J<sub>1</sub>_ 有n个主元，最后一列的 _(C<sub>1</sub>, C<sub>2</sub>, ..., C<sub>n</sub>)_ 是方程唯一解
  * 情况 2.2：_r < n_
    * 有 _n - r_个自由未知量

### 1.3 数域

> 视频7

定义1：复数集的一个非空子集K，如果满足：

（1）*0， 1 ∈ K*

（2）*a，b ∈ K* → *a ± b, ab ∈ K*

（3）*a，b ∈ K*，且 *b ≠ 0 → <sup>a</sup>/<sub>b</sub> ∈ K*

上面 *K* 是一个数域

**数域举例：**

- 有理数域 *Q* （最小的数域）
- 实数域 *R*
- 复数域 *C* （最大的数域）

对于例子：

-  _a<sub>11</sub>x1 + a<sub>12</sub>x<sub>2</sub> = b<sub>1</sub>_
- _a<sub>21</sub>x1 + a<sub>22</sub>x<sub>2</sub> = b<sub>2</sub>_

其增广矩阵转化为阶梯矩阵后可得

<p align="center">
<img src="https://latex.codecogs.com/gif.latex?\begin{pmatrix}&space;a_{11}&space;&&space;a_{12}&space;&&space;b_1\\&space;0&space;&&space;a_{22}&space;-&space;\frac{a_{21}}{a_{11}}a_{12}&space;&&space;b_2&space;-&space;\frac{a_{21}}{a_{11}}b_1&space;\end{pmatrix}" title="\begin{pmatrix} a_{11} & a_{12} & b_1\\ 0 & a_{22} - \frac{a_{21}}{a_{11}}a_{12} & b_2 - \frac{a_{21}}{a_{11}}b_1 \end{pmatrix}" />
</p>

所以需要第二行第二个元素部位*0*，意味着

* _(<sup> a<sub>11</sub>a<sub>22</sub> - a<sub>21</sub>a<sub>12</sub> </sup>/<sub> a<sub>11</sub> </sub>) ≠ 0_，即
* _a<sub>11</sub>a<sub>22</sub> - a<sub>21</sub>a<sub>12</sub> ≠ 0_

表达式_a<sub>11</sub>a<sub>22</sub> - a<sub>21</sub>a<sub>12</sub> ≠ 0_ 用  _|A|_ 来表示，称为**行列式**，这里是**二阶行列式**

#### 习题1.3 思路

1. 令 *Q(i) = {a + bi | a, b ∈ Q}*, 证明 *Q(i)* 是一个数域

证明思路：

* 0 = 0 + 0i ∈ Q(i), 1 = 1 + 0 i ∈ Q(i)
* α = a + bi, β = c + di
  - α ± β = (a ± c) + (b ± d)i ∈ Q(i)
  - αβ = (ac - bd) + (ad + bc)i ∈ Q(i)
  - β ≠ 0，则c、d不全为0，则<img src="https://latex.codecogs.com/gif.latex?\inline&space;\frac{\alpha}{\beta}&space;=&space;\frac{a&plus;bi}{c&plus;di}&space;=&space;\frac{(a&plus;bi)(c-di)}{(c&plus;di)(c-di)}=\frac{ac&plus;bd}{c^2&plus;d^2}&plus;\frac{(bc-ad)}{c^2&plus;d^2}i&space;\in&space;Q(i)" title="\frac{\alpha}{\beta} = \frac{a+bi}{c+di} = \frac{(a+bi)(c-di)}{(c+di)(c-di)}=\frac{ac+bd}{c^2+d^2}+\frac{(bc-ad)}{c^2+d^2}i \in Q(i)" />

2. 令 <img src="https://latex.codecogs.com/gif.latex?F=\{\frac{a_0&plus;a_1e&plus;\cdots&plus;a_ne^n}{b_0&plus;b_1e&plus;\cdots&plus;b_ne^n}" title="F=\{\frac{a_0+a_1e+\cdots+a_ne^n}{b_0+b_1e+\cdots+b_ne^n}" /> n、m为任意非负整数，a<sub>i</sub>，b<sub>i</sub> 数域 Z，0 ≤ i ≤ n, 0 ≤ j ≤ m。证明F是一个数域，其中e是自然对数的底。

证明思路：

* 对于 0、1∈ F的思路同上题目
* 对于F中的两个数 α、β
  * 令<img src="https://latex.codecogs.com/gif.latex?\alpha=\frac{a_0&plus;a_1e&plus;\cdots&plus;a_{n_\alpha}e^{n_\alpha}}{b_0&plus;b_1e&plus;\cdots&plus;b_{n_\alpha}e^n_{n_\alpha}},&space;\beta=\frac{a_0&plus;a_1e&plus;\cdots&plus;a_{n_\beta}e^{n_\beta}}{b_0&plus;b_1e&plus;\cdots&plus;b_{n_\beta}e^n_{n_\beta}}" title="\alpha=\frac{a_0+a_1e+\cdots+a_{n_\alpha}e^{n_\alpha}}{b_0+b_1e+\cdots+b_{n_\alpha}e^n_{n_\alpha}}, \beta=\frac{a_0+a_1e+\cdots+a_{n_\beta}e^{n_\beta}}{b_0+b_1e+\cdots+b_{n_\beta}e^n_{n_\beta}}" />
  * 则 <img src="https://latex.codecogs.com/gif.latex?\alpha\beta=\frac{a_0^2&plus;2a_0a_1e&plus;\cdots&plus;a_{n_\alpha}a_{n_\beta}e^{n_\alpha&plus;n_\beta}}{b_0^2&plus;2b_0b_1e&plus;\cdots&plus;b_{n_\alpha}b_{n_\beta}e^n_{n_\alpha&plus;n_\beta}}" title="\alpha\beta=\frac{a_0^2+2a_0a_1e+\cdots+a_{n_\alpha}a_{n_\beta}e^{n_\alpha+n_\beta}}{b_0^2+2b_0b_1e+\cdots+b_{n_\alpha}b_{n_\beta}e^n_{n_\alpha+n_\beta}}" />，所以 αβ ∈ F
  * 同样的思路 α ± β ∈ F，<sup>α</sup>/<sub>β</sub> ∈ F


[回到顶部](#丘维声高等代数学习笔记)
