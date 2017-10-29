---
layout: default
title: 標本平均の分散について
---
# 標本平均の分散について

※ github pagesへの試験投稿

ある(特に正規分布であるとか限定はせず)確率分布$D$ の
標本平均$\bar{X}$、つまり独立なサンプル$X_i = X_1, X_2, ... X_n$の平均

$$\bar{X} = \dfrac{1}{n}\sum_i^n X_i$$

について、その標本平均自体の分散$V[\bar{X}]$は、下記のように求められる。

$$
\begin{eqnarray*}
V[\bar{X}] &=& V\Big[\dfrac{X_1 + X_2 + ... + X_n}{n}\Big]\\
&=&\Big(\dfrac{1}{n}\Big)^2\Big(V[X_1] + VaV_2] + ... + V[V]\Big)\\
&=&\dfrac{n\sigma^2}{n^2}\\
&=&\dfrac{\sigma^2}{n}\\
\end{eqnarray*}
$$

ここで、1式から2式への変換には
1. $V(aX + b) = a^2 V(X)$
と
2. $V(X_1+X_2)=X(X_1) + X(X_2)$ (ただし$X_1$と$X_2$は独立)

という性質を用いている。

---
$V[\bar{X}] = \dfrac{\sigma^2}{n}$は、サンプル数nが大きくなるほど$\bar{X}$の分散が小さくなり、確率分布$D$の真の平均$\mu$に収束していくことを示している。
