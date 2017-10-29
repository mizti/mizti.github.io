---
layout: default
title: 正規分布のモーメント母関数の導出
---

# 正規分布のモーメント母関数の導出

モーメント母関数の一般形は

$$M_x(t) = E[e^{tX}]$$

と表される（これが定義）。これをまず  

$$
E[X] = \int xp(x) dx
$$

用いて展開する（確率分布を用いた期待値の表現）。  

$$
\begin{eqnarray*}
&=& \int_{-\infty}^{\infty} e^{tx} \frac{1} {\sqrt{2\pi}\sigma}e^{-\frac{(x-\mu)^2}{2\sigma^2}}dx
\end{eqnarray*}
$$

$e^{tx}$を$ e^{-\frac{(x-\mu)^2}{2\sigma^2}}$ と合わせる  

$$
\begin{eqnarray*}
&=& \int_{-\infty}^{\infty} e^{tx} \frac{1} {\sqrt{2\pi}\sigma}e^{tx {-\frac{(x-\mu)^2}{2\sigma^2}}}dx
\end{eqnarray*}
$$

ここで、指数部に着目する。  

$$
\begin{eqnarray*}
tx {-\frac{(x-\mu)^2}{2\sigma^2}} &=& \frac{ -x^2 + 2\mu x - \mu ^2 + 2t\sigma^2 x }{2\sigma^2} (展開して通分)\\
&=& \frac{ -x^2 + 2(\mu +t\sigma^2)x - \mu ^2 }{2\sigma^2} (xの2次方程式に)\\
\end{eqnarray*}
$$

ここで、$\mu + t\sigma ^2$ を仮に$h$と置くと、  

$$
\begin{eqnarray*}
&=& \frac{ -x^2 + 2hx - \mu ^2 }{2\sigma^2} (hを置き換えた)\\
&=& \frac{ -(x^2 -2hx) - \mu ^2}{2\sigma^2} \\
&=& \frac{ -((x-h)^2 - h^2) - \mu ^2}{2\sigma^2} \\
&=& \frac{ -(x-h)^2 + h^2 - \mu ^2}{2\sigma^2} \\
&=& \frac{ -(x-h)^2 + (\mu + t \sigma^2)^2 - \mu ^2}{2\sigma^2}  (後ろのhのみ展開)\\
&=& \frac{ -(x-h)^2 + 2\mu t \sigma^2 + t^2 \sigma^4 }{2\sigma^2} \\
&=& \frac{ -(x-h)^2 } {2\sigma^2}+ \mu t  + \frac{t^2 \sigma^2}{2}  (約分) \\
&=& -\frac{ (x-h)2 } {2\sigma^2}+ \mu t  + \frac{t^2 \sigma^2}{2}  (約分) \\
\end{eqnarray*}
$$

と指数部を変形することができた。よって、最初の式に戻ると  

$$
\begin{eqnarray*}
E[e^{tX}] &=& \int_{-\infty}^{\infty} \frac{1} {\sqrt{2\pi}\sigma}e^{ -\frac{ (x-h)^2 } {2\sigma^2} + \mu t + \frac{t^2 \sigma^2}{2}  }dx \\
 &=& e^{ \mu t + \frac{t^2 \sigma^2}{2}  } \int_{-\infty}^{\infty} \frac{1} {\sqrt{2\pi}\sigma}e^{ -\frac{ (x-h)^2 } {2\sigma^2}   }dx
\end{eqnarray*}
$$

ここで、積分の中を見ると平均$h = \mu + t\sigma ^2$、分散$\sigma^2$な正規分布$\mathcal{N}(h, \sigma^2)$となっていることが分かる。  

正規分布は確率分布であり、全範囲で積分すれば$1$である
（∵全事象の起きる確率は1である）ため、結局、正規分布においては  

$$
\begin{eqnarray*}
Mt(x) = E[e^{tX}] &=& e^{ \mu t + \frac{t^2 \sigma^2}{2}  } 
\end{eqnarray*}
$$

が成立することが分かる。
