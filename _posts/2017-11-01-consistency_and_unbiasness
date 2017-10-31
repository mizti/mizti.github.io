---
layout: default
title: 一致推定量と不偏推定量
---

# 一致推定量と不偏推定量

何らかの確率分布からいくつかのサンプルを抽出した際に、そのサンプルから推定される推定量（例えば平均とか分散とか）が全体の確率分布の同じパラメータと「同じもの」になるかどうかは統計を考える上で重要である。

「一致推定量」と「不偏推定量」はともにサンプルから計算した推定量が真のパラメータと"同じ"かどうかを判定するための二つの異なる性質である。

以下、$\hat{\theta}$ をサンプルから推定した推定量、$\theta$ を確率分布全体の真のパラメータとする。

|＼           | 不偏推定量(Unbiased Estimator)   | 一致推定量 (Consistent Estimator)|
|:-----------|:------------|:------------|
|意味|期待値としては対象のパラメータと一致する推定量|サンプル数nが増えると対象のパラメータに収束する推定量|
|定義|$E[\hat{\theta}]- \theta=0$ もしくは $E[\hat{\theta} - \theta]=0$|$\lim_{n \to \infty} \hat{\theta} \to \theta$|

また、それぞれの性質を

* 不偏性: Unbiasedness
* 一致性: Consistency

という。

#### 標本に対する不偏分散の導出

ある独立な $n$ 個の独立なサンプル(=標本) $X_i = X_1, X_2, ... ,X_n$ を確率分布 $F$ から取得した場合に、まず $\bar{X}$ を標本平均

$$
\bar{X} = \frac{1}{n}\sum_{i=1}^{n}X_i
$$

とする。

このサンプルの分散（標本分散）$V_s$ は分散の定義から

$$
V_s = \frac{1}{n}\sum_{i=1}^n(X-\bar{X})^2
$$

と表される。しかしこの標本分散は確率分布 $F$ の分散 $V_F$ に対する不偏分散とはなっていない。以下にそれを示す。
もし $V_s$ が $V_F$ の不偏推定量であれば、 $E[V_s] - V_F $ が0になるはずである。

ここで、

$$
\begin{eqnarray*}
E[V_s]  &=& E\Big[\frac{1}{n}\sum_{i=1}^n(X_i-\bar{X})^2\Big] \\ 
&=& E\Big[   \frac{1}{n}\sum_{i=1}^n   ((X_i-\mu) -(\bar{X}-\mu))^2   \Big] \\ 
&=& E\Big[   \frac{1}{n}\sum_{i=1}^n   ((X_i-\mu)^2 -2(X_i-\mu)(\bar{X}-\mu)  +(\bar{X}-\mu)^2)   \Big]  \\ 
&=&  \frac{1}{n}\sum_{i=1}^n   E\Big[(X_i-\mu)^2\Big] -\frac{2}{n}  \sum_{i=1}^n  E\Big[(X_i-\mu)(\bar{X}-\mu) \Big] + \frac{1}{n}  \sum_{i=1}^nE\Big[(\bar{X}-\mu)^2 \Big] (期待値Eの線形性から)\\
&=&  \frac{1}{n}\sum_{i=1}^n   E\Big[(X_i-\mu)^2\Big] -\frac{2}{n} (\bar{X}-\mu) \sum_{i=1}^n  E\Big[(X_i-\mu) \Big] + E\Big[(\bar{X}-\mu)^2 \Big]  (iを持たない項目を\sum からくくりだし)\\ 
&=&  \frac{1}{n}\sum_{i=1}^n   E\Big[(X_i-\mu)^2\Big] -{2} (\bar{X}-\mu)   E\Big[(\bar{X}-\mu) \Big] + E\Big[(\bar{X}-\mu)^2 \Big]  (\bar{X}の定義)\\ 
&=&  \frac{1}{n}\sum_{i=1}^n   E\Big[(X_i-\mu)^2\Big]-E\Big[(\bar{X}-\mu)^2 \Big]  \\ 
\end{eqnarray*} 
$$

ところで、 $V_F = \sigma^2$ の定義は $E\big[(X_i - \mu)^2\big]$ であることから、

$$
\begin{eqnarray*}
E[V_s]  &=& \frac{1}{n}\sum^n_{i=1} \sigma^2 -E\Big[(\bar{X}-\mu)^2 \Big] \\
&=& \sigma^2 -E\Big[(\bar{X}-\mu)^2 \Big] 
\end{eqnarray*} 
$$

であり、結局、 $E[V_s]$ は $V_F$ より $E\Big[(\bar{X}-\mu)^2 \Big] $ だけ小さいことが分かる。つまり $E[V_s] - V_F $ は $0$ にならず $V_s$ は $V_F$ の不偏推定量 **ではない** ことがわかる。    
（つまり、標本から頑張って素直に計算した分散は真の分散と一致しない）  
    
ところで、上記の差分の $E\Big[(\bar{X}-\mu)^2 \Big] $ について、 $\bar{X}$ の定義から


$$
\begin{eqnarray*}
E\Big[(\bar{X}-\mu)^2 \Big]  &=& \frac{1}{n} \sum^{n}_{i=1}E\Big[(X_i-\mu)^2\Big] \\
&=& \frac{1}{n} \sigma ^2 = \frac{1}{n} V_F
\end{eqnarray*} 
$$

であることがわかる。

つまり、$V_s$ の期待値は $V_F$ よりも $\frac{1}{n} V_F $ だけ大きく、

$$
E[V_s] = \sigma^2 - \frac{1}{n}\sigma^2 = \frac{n-1}{n}\sigma^2
$$

であり、$V_s$ を $\frac{n}{n-1}$ 倍した $V_u$ を置くと、

$$
E[V_u] = \sigma ^2
$$

となるため、 $V_u$ は $V_F$ の不偏推定量であると言える。
(また、この $V_u$ を不偏分散(Unbiased Variance)という)  
  
定義より、

$$
\begin{eqnarray*}
V_u = \frac{n}{n-1}V_s &=& \frac{n}{n-1}\frac{1}{n}\sum^{n}_{i=1}(X_i - \bar{X})^2\\
&=&\frac{1}{n-1}\sum^{n}_{i=1}(X_i - \bar{X})^2
\end{eqnarray*}
$$

が不偏分散の一般形となる。

#### 不偏分散が一致推定量であること

一致推定量の定義は$\lim_{n \to \infty} \hat{\theta} \to \theta$であることから、不偏分散が（真の）分散の一致推定量であることを言うためには

$$\lim_{n \to \infty} V_u \to V_F$$

を言えば良い。  
  
が、これはなかなか大変。

まず、不偏分散の性質として、
 $(n-1)V_u / \sigma^2$ が自由度 $n-1$ のカイ二乗分布に従うことが知られている。

すなわち

$$
(n-1)V_u / \sigma^2 = \frac{1}{2^{\frac{n-1}{2}}\Gamma(\frac{n-1}{2})}x^{\frac{n-1}{2}-1}e^{-{\frac{x}{2}}}
$$

であり、なおかつ、カイ二乗分散に従う変数の分散は、 $2k$ ( $k$ は自由度)となることから、

$ Var[(n-1)V_u / \sigma^2 ] = 2(n-1)$

が言える。分散の変換公式から $V_u$ 以外の数を $Var$ から出すと、

$$
\begin{eqnarray*}
Var[(n-1)V_u / \sigma^2 ] &=& 2(n-1)\\
(n-1)^2Var[V_u / \sigma^2] &=& 2(n-1)\\
Var[V_u / \sigma^2 ] &=& \frac{2}{(n-1)}\\
Var[V_u] &=& \frac{2\sigma^4}{(n-1)}
\end{eqnarray*}
$$

が得られる。

ここでチェビシェフの不等式を用いる。
チェビシェフの不等式とは、確率分布と標準偏差( $\sigma$ )の間に**常に**成り立つ関係を示した式である。

$$
P(|X-\mu| \geq k\sigma) \leq \frac{1}{k^2}
$$

もしくは

$$
P(|X-\mu| \geq k) \leq \frac{\sigma^2}{k^2}
$$

更にXのみで表すと

$$
P(|X-E[X]| \geq k) \leq \frac{Var[X]}{k^2}
$$

と表される。

この式は
  * 平均から 2標準偏差以上離れた値は全体の $1/4$ を超えない
  * 一般にk標準偏差以上離れた値は全体の $1/k^2$ を超えない

ことを示している。
この $X$ に $V_u$ を代入し、

$$
P(|V_u - E[V_u]| > k) \leq \frac{Var[V_u]}{k^2}
$$

$E[V_u] = \sigma^2$であることに注意すると、

$$
P(|V_u - \sigma^2| > k) \leq \frac{Var[V_u]}{k^2}
$$

が得られる。先程求めた $Var[V_u]$ を右辺に代入すると、

$$
P(|V_u - \sigma^2| > k) \leq \frac{2\sigma^4}{(n-1)k^2} \to 0　(n \to \infty)
$$

つまり、nが十分に大きいとき、  $P(|V_u - \sigma^2| > k) $  が0に収束することが示された。
これは逆に言えば任意の $k$ について
 $P(|V_u - \sigma^2| \leq k) $ が1に収束することを示しており、

kは任意の正の値なので、 結局、 $n \to \infty $のとき、 $V_u$ と $\sigma^2$ の差はは必ずどんなに小さい値kよりも必ず小さくなる、と言うことができ、 $V_u$ は $\sigma^2$ と一致することから $V_u$ は $\sigma^2$ の一致推定量であると言うことができる。

