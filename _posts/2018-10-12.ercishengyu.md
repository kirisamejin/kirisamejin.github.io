---
title: 二次剩余
teaser:
category:
tags: [数论]
---

###二次剩余

> ##### p是一个奇质数且a不被p整除那么同余方程组$x^2\equiv a(mod p)$要么无解要么有两个非同余解
proof. 如果$x_0$是一个解，那么有$(-x_0)^2\equiv (x_0)^2\equiv a$,$-x_0$是一个解。（因为$(-x_0)\equiv (x_0) \rightarrow p\mid 2x_0 $矛盾）
如果有另外一个解$x_1$$(x_0)^2\equiv (x_1)^2 \rightarrow (x_0-x_1)(x_0+x_1)\equiv 0 \to p\mid (x_0-x_1) \| p\mid (x_0+x_1) \to x_0\equiv x_1 \| x_0 \equiv -x_1$ 因此只有两个非同余解

>#####p是一个奇质数，在$1,2,...,p-1$中恰好有$\frac{(p-1)}{2}$个二次剩余和$\frac{(p-1)}{2}$个非二次剩余
>proof. 因为每个a（$x^2\equiv a(mod p)$）要么对应2个数要么对应0个数，而又有1，2，p-1这些数的平方，所以这些平方有(p-1)/2个不同的值，这些值为二次剩余，剩下的(p-1)/2为非二次剩余简化

[//]: # (This may be the most platform independent comment)

[comment]: # (p是一个质数，r是p的原根。如果a不被p整除，如果$ind_ra$是偶数，那么a是p的二次剩余；否则，a是p的非二次剩余)

> $$\bigl( \frac ap \bigr) =
\begin{cases}
1,  & \mbox{if }a\mbox{ is quadratic residues} \\
-1, & \mbox{if }a\mbox{ is not quadratic residues}
\end{cases}
$$
> 若a不被p整除 $$\bigl( \frac ap \bigr) = a^{\frac {p-1}2}$$
proof. 如果是二次剩余显然有$(x^2)^{\frac {p-1}2}=a^{\frac {p-1}2}=1$。由于对$ij=a$的每个i一定存在一个j（因为p是质数，$i,j\in 1,...,p-1$），如果是非二次剩余有$i\neq j$，且j唯一，所以有$\frac {p-1}2$对，即$a^{\frac {p-1}2}=(p-1)!=-1$


求 $x^2=n \%p $
设$\omega$是模p非二次剩余$\omega = a^2 - n$设$\sqrt \omega$是虚数单位根=$\sqrt {-1}$
$ 则n=a^2-\omega=(a-\sqrt\omega)(a+\sqrt\omega) (\because \omega^{\frac p2}=\omega^{\frac 12}\cdot -1)$
$=(a+\sqrt\omega)^p(a+\sqrt\omega)=(a+\sqrt\omega)^{\frac {p+1}2 \cdot 2}=x^2$
其实直接看这个就完事了[这里](https://blog.csdn.net/qq_33229466/article/details/79125057)
引用一下
> 然后x取相反数也是一个解。这时可能有人会问，我们得到的解会在𝔽p2域上的，但是我们要求的是𝔽p域的解，也就是说我们所谓的“虚部”ω系数是否可能不为0。
> 其实我们不需要担心这个问题，由拉格朗日定理，我们知道在任意一个模p(p∈ℙ)的数域里面，任意一个多项式f(x)最多有deg(f(x))个根（f(x)≡0(modp)的解称为f(x)在𝔽p下的根），deg表示多项式的度数，即最大指数。由于𝔽p2是对𝔽p域的扩充，𝔽p域的两根一定在𝔽p2内也有效，并且我们知道x2−n在数域𝔽p2下的根有两个（x1,x2），那么x1,x2一定也是𝔽p域下的根，也就是“虚部”系数为0。

[这个讲的也很好](https://blog.csdn.net/ZLTJohn/article/details/80289470)


[有代码实现的博客](https://blog.csdn.net/kele52he/article/details/78897187)

练习：bzoj5104
