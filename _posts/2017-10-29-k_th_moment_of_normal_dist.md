---
layout: default
title: 正規分布の標本平均のk次モーメント一般解の導出
---

# 正規分布の標本平均のk次モーメント一般解の導出

ある確率分布の標本平均$\bar{X}$について、この平均は$\mu$、分散は$\frac{\sigma^2}{n}$ である(事前知識)。    

このとき、$\bar{X}$の、平均周りのk次モーメントを求める。  
$\bar{X} - \mu$は平均0、分散 $\frac{\sigma^2}{n}$の正規分布となる。    

ここで、$\frac{\sigma^2}{n}$を$\sigma \prime ^2$と置くとすると、正規分布のモーメント関数の一般形  

$$
\begin{eqnarray*}
M(t)  &=& e^{ \mu t + \frac{\sigma^2 t^2}{2}  } 
\end{eqnarray*}
$$

から$N(0, \sigma \prime ^2)$ のモーメント母関数$M(t)$は、  

$$
M(t) =  e^{\frac{\sigma \prime^2 t^2}{2}}
$$

となる。ところで、$e^x$は下記のようにマクローリン展開できることが知られており、  

$$
\begin{eqnarray*}
e^x &=& 1 + \frac{1}{1!}x + \frac{1}{2!}x^2  + \frac{1}{3!}x^3 ...\\
&=& \sum^{\infty}_{m=0} \frac{1}{m!}\Big( x^m \Big)
\end{eqnarray*}
$$

ここで$x=\frac{\sigma \prime^2 t^2}{2}$ と見なせば、  

$$
\begin{eqnarray*}
M(t) &=&  \sum^{\infty}_{m=0} \frac{1}{m!}\Big(  \frac{\sigma \prime^2 t^2}{2} \Big)^m\\
&=& \sum^{\infty}_{m=0} \frac{1}{m!} \Big( \frac{\sigma \prime ^2}{2} \Big)^m t^{2m}
\end{eqnarray*}
$$

と書ける。これを展開すると、  

$$
\begin{eqnarray*}
M(t) &=& \frac{1}{0!}\Big(\frac{\sigma \prime ^2}{2}\Big)^0 t^0 
             + \frac{1}{1!}\Big(\frac{\sigma \prime ^2}{2}\Big)^1 t^2 
             +  \frac{1}{2!}\Big(\frac{\sigma \prime ^2}{2}\Big)^2 t^4
             +  ... 
\end{eqnarray*}
$$

という形で、tについて偶数回微分したときにのみ定数項が現れる式形であることがわかる。  

微分後に$t=0$を代入することを考えれば、  
  1. 微分回数が奇数の時、k次モーメントは0
を言うことができる。  

微分回数が偶数回($2m$)回のときに定数項に現れるのは、$\frac{2m!}{m!}\Big(\frac{\sigma \prime ^2}{2}\Big)^m$ であり、これがすなわち  

$$
\begin{eqnarray*}
M^{(2m)}(0) &=& \frac{2m!}{m!}\Big(\frac{\sigma \prime ^2}{2}\Big)^m\\
&=&  \frac{2m!}{m!}\Big(\frac{\sigma ^2}{2n}\Big)^m
\end{eqnarray*}
$$

である。  
ここまででも一般形になっているのだが、ガンマ関数を用いて表してみる。  
一般に、$n!$は  

$$
n! = \Gamma(n+1)
$$

と表すことができ、これを用いると、$m! = \Gamma(m+1)$ 、$2m! = \Gamma(2m+1)$より  

$$
\begin{eqnarray*}
M^{(2m)}(0) &=& \frac{\Gamma(2m+1)}{\Gamma(m+1)}\Big(\frac{\sigma ^2}{2n}\Big)^m\\
\end{eqnarray*}
$$

と表すことができる。
