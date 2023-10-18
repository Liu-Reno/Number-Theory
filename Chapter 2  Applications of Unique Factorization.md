# Chapter 2 : Applications of Unique Factorization

$\text{The importance of the notion of prime number should be evident from the results of Chater 1.}$

$\text{In this chapter we shall give several proofs of the fact that there are infinitely many primes in }\Z$.$\text{We shall also consider the analogous question for the ring }$$k[x].$

$\text{The theorem of unique prime decomposition is sometimes referred to as the fundamental theorem of arithmetic. We shall begin to demonstrate its usefulness}$ $\text{by using it to investigate the properties of some natural number-theoretic functions.}$



## $\S1\quad \Z$上具有无穷多个素数

定理$1(\text{Euclid})$ 在环$\Z$上有无穷多个素数.

[证明]

让我们考虑所有正素数.以增长关系将它们标记为$p_1,p_2,\cdots$因此有$p_1 = 2,p_2 = 3,p_3 = 5$等.

令$N = (p_1p_2\cdots p_n)+1$.不难发现$N$比$1$大且不能被任意的$p_i$所整除,$i = 1,2,\cdots,n$.另一方面,由于$N$是实数,根据唯一分解定理可以得知$N$必然能被某个素数$p$所整除,且$p$必然要大于$p_n$.

我们就证明了给定任何正素数,总是存在一个比它大的素数,由此可见,素数的集合是无限集$\square$



$k[x]$上的类似定理是具有无穷多个单元的,首一不可约多项式.若$\mathbb{k}$是无穷的,这就是显而易见的,因为$x - a, a \in \mathbb{k}$就有无穷多个,且其不可约.若$\mathbb{k}$是有限的,这个证明方式就鞭长莫及了,但是$\text{Euclid}$的证明可以轻松地推广到这种情况上.我们将其留到习题.

回想一下,在一个整环中两个元素若仅通过乘以一个单位而不同,则它们被称为是关联的.我们现在知道$\Z$和$k[x]$上都有无穷多个不关联素元.考虑一个由关联素元所构成的环是有意义的,它本质上只有一个素数.

令$p \in \Z$为一个素数并且令$\Z_p$为由全体有理数$a/b,p \nmid b$所构成的集合.很容易通过命题$1.1.1$的推论$1$下的注释(若$p\nmid a$且$p \nmid b$则$p\nmid ab$)来得到$\Z_p$确实是一个环(对于加减法,由于$a/b+c/d$有$p\nmid b$且$p\nmid d$于是有$p \nmid bd$因此得到$(ad\pm bc)/bd \in \Z_p$,由此可以推出乘法封闭性).若$a/b \in \Z_p$是一个单位则有$a/b \mid 1$即存在$c/d \in \Z_p$使得$a/b \cdot c/d = 1$得到$ac = db$由于$p \nmid b$且$p \nmid d$得到$p \nmid a$.反过来,任意有理数$a/b$是$\Z_p$上的单位则有$p \nmid a$且$p \nmid b$.若$a/b \in \Z_p$记$a = p^l a'$其中$p\nmid a'$.则$a/b = p^la'/b$.因此$\Z_p$中每个元素都是$p$的幂乘以一个单位.由此很容易看出$\Z_p$中仅有的素数均为$pc/d$的形式,其中$c/d$是一个单位.因此$\Z_p$中的所有素数都是相关联的.



### $\text{\large{E}\small{XERCISE}}$

若$a/b \in \Z_p$不是一个单位,证明$a/b + 1$是一个单位.这一现象说明了$\text{Euclid}$的证明在整环中为何普遍失效.



 由于$a/b$不是一个单位,因此有$p \mid a$.由于$p \nmid b$因此有$p \nmid (a+b)$,因此$a/b+1$是一个单位,因此$\Z_p$中有无穷多个单位,也就催生出无穷多个素元.







## $\S 2\quad$若干数论函数

在本章的剩余部分,我们将给出唯一分解定理的一些应用.

一个整数$a \in \Z$若不能被任何大于$1$的整数平方整除,则说它是无平方因子的$(\text{square-free})$



命题$2.2.1$ 若$n \in \Z$,$n$可以写为$n = ab^2$的形式,其中$a,b \in \Z$且$a$是无平方因子的.

[证明]

令$n = p_1^{a_1}p_2^{a_2}\cdots p_l^{a_l}$我们可以对于$a_i$做关于$2$的带余除法,得到$a_i = 2b_i +r_i$得到$r_i = 0$或$1$,这取决于$a_i$是否能够被$2$整除.

令$a = p_1^{r_1}p_2^{r_2}\cdots p_l^{r_l}$以及$b = p_1^{b_1}p_2^{b_2}\cdots p_l^{b_l}$得到$n = ab^2$且$a$显然是无平方因子的.$\square$



这个引理可以用来给出$\Z$具有无穷多个素数的另一种证明.假设不是无穷多个,令$p_1,p_2,\cdots,p_n$为全体正素数所构成的清单.考虑一个小于等于$N$的正整数集合.若$n \leq N$则$n = ab^2$,其中$a$无平方因子,因此$a$等于$p_1^{\varepsilon_1}p_2^{\varepsilon_2}\cdots p_l^{\varepsilon_l}$其中$\varepsilon_i = 0,1$所合成的$2^l$个数中的某一个.注意到$b \leq \sqrt{N}$.因此至多有$2^l\sqrt{N}$个元素满足要求,即$N\leq 2^l\sqrt{N}$即$\sqrt{N}\leq 2^l$发现当$N$足够大时有这是不成立的,造成矛盾.

> 也就是说由于全体正素数共有$l$个,因此$b$与$a$的组合至多有$2^l \times \sqrt N$种,由于$ab^2$表示所有的$n\leq N$因此必然有$N \leq 2^l \sqrt{N}$

可以给出一个类似的证明,证明$k[x]$中存在无穷多个不可约首一多项式,其中$\mathbb{k}$是一个有限域



在整数上有很多自然定义的函数.比如说,给定一个正整数$n$令$v(n)$为$n$的正因子数且$\sigma(n)$作为$n$的所有正因子之和.举个例子$v(3) = 2$,$v(6) = 4$以及$v(12) = 6$.$\sigma(3) = 4$,$\sigma(6) = 12$,$\sigma(12) = 28$.利用唯一因式分解,可以得到相当简单地求解这些函数的公式.



命题$2.2.2$ 若$n$是一个正整数,令$n = p_1^{a_1}p_2^{a_2}\cdots p_l^{a_l}$为其素数分解.则

$(\text{a})$ $v(n) = (a_1+1)(a_2+1)\cdots(a_l+1)$

$(\text{b})$ $\sigma(n) = \frac{p_1^{a_1+1}-1}{p_1-1}\frac{p_2^{a_2+1}-1}{p_2-1}\cdots\frac{p_l^{a_l+1}-1}{p_l-1}$

[证明]

不难发现,$m \mid n$当且仅当$m = p_1^{b_1}p_2^{b_2}\cdots p_l^{b_l}$其中$0 \leq b_i \leq a_i$因此得到对于每一个$i$,$b_i$都有$a_i + 1$种选择.

因此$v(n) = (a_1+1)(a_2+1)\cdots (a_l+1)$



对于$(\text{b})$得知$\sigma(n) = \sum_{(b_1,b_2,\cdots,b_l)}p_1^{b_1}p_2^{b_2}\cdots p_l^{b_l}$.因此得到$\sigma(n) = (\sum_{b_1 = 0}^{a_1}p_1^{b_1})(\sum_{b_2 = 0}^{a_2}p_2^{b_2})\cdots (\sum_{b_l = 0}^{a_l}p_l^{b_l})$.利用等比数列求和公式就得到了$\sigma(n)$.$\square$



关于函数$\sigma(n)$有一个有趣但是未解决的问题.若$\sigma(n) = 2n$则$n$称为是完全的.举个例子$6$和$28$是完全的.一般地,若$2^{m+1}-1$是一个素数,则$n = 2^m(2^{m+1}-1)$是完全的,因为$\sigma(2^m(2^{m+1}-1)) = (2^{m+1}-1)\frac{(2^{m+1}-1)^2-1}{2^{m+1}-2} = (2^{m+1}-1)\frac{2^{2(m+1)}-2^{m+2}}{2(2^m-1)} = (2^{m+1}-1)\frac{2^{m+2}(2^m-1)}{2(2^{m-1})} = 2^{m+1}(2^{m+1}-1) = 2(2^m(2^{m+1}-1))$.这个事实在$\text{Euclid}$时期就已经存在.$\text{L.Euler}$证明了任何偶完全数都为这个形式.因此偶完全数的问题就简化为寻找$2^{m+1}-1$形式的素数问题.这样的素数称为$\text{Mersenne}$素数.涉及完全数的两个突出问题是:是否有无穷多个完全数?是否有奇数完全数?

这个问题在乘法上是显然的.若整数$n$的正因子乘积为$n^2$则这个数称为乘法完备数.这样一个数不可能为素数或者素数的平方.因此存在一个真因子$d$使得$d \neq n/d$.因子$1,d,n/d,d$的乘积就是$n^2$.因此,若$n$恰好有两个固有因数.这样的数只有素数的立方数或两个不同素数的乘积.例如,$27$和$10$是乘法完全数.

我们现在介绍一个非常重要的数论函数,$\text{M}\ddot{\text{o}}\text{bius}$函数$\mu$.对于$n \in \Z^+$有$\mu(1) = 1$且$n$有平方因子时$\mu(n) = 0$.有$\mu(p_1p_2\cdots p_l)= (-1)^l$其中$p_i$是互异的正素数.



命题$2.2.3$ 若$n>1$,$\sum_{d \mid n}\mu(d) = 0$

[证明]

对于$n$使用唯一因式分解得到$n= p_1^{a_1}p_2^{a_2}\cdots p_l^{a_l}$考虑$d \mid n$,若$d$有平方因子时有$\mu(d) = 0$.由于$d$可以写为$ab^2$的形式,而当$b \neq 1$时有$\mu(d) = 0$且对于$a$有$a = p_1^{\varepsilon_1}p_2^{\varepsilon_2}\cdots p_l^{\varepsilon_l}$其中$\varepsilon_i = 0$或$1$.

因此得到$\sum_{d\mid n}\mu(d)$可以转化为$\sum_{a \mid n}\mu(a)$其中$a$如前文所述,根据$0,1$选择的不同共有$2^l$种组合.

因此得到
$$
\sum_{d \mid n}\mu(d) = 1+(-1)l+(-1)^2{l \choose 2} + (-1)^3{l \choose 3}+\cdots + (-1)^l = (1-1)^l = 0
$$
$\square$

当$\text{M}\ddot{\text{o}}\text{bius}$函数与$\text{Dirichlet}$乘积联系起来时,其意义就能被清楚地理解.

令$f,g$为$\Z^+$上的复值函数.$f$与$g$的$\text{Dirichlet}$乘积被定义为公式$f \circ g(n) = \sum f(d_1)g(d_2)$其中求和对象是所有满足$d_1d_2 = n$的正整数有序偶$(d_1,d_2)$.这个乘积是满足结合律的,我们可以通过$f\circ (g \circ h)(n)$来检验,$f \circ (g \circ h) = f \circ (\sum g(d_2)h(d_3)) = \sum f(d_1)(\sum g(d_2)h(d_3)) = \sum (f(d_1)g(d_2))h(d_3) = (\sum f(d_1)g(d_2)) \sum h(d_3) = (f \circ g)\circ h(n)$.其中有$(d_1,d_2,d_3)$满足$d_1d_2d_3 = n$.



定义函数$\mathbb{I}$为$\mathbb{I}(1) = 1$且对于$n >1$有$\mathbb{I}(n) = 0$.则$\sum f(d_1)\mathbb{I}(d_2) = f \circ \mathbb{I} = \mathbb{I}\circ f = \sum \mathbb{I}(d_1)f(d_2) = f$其中$d_1d_2 = n$.

定义$I$为$I(n) = 1$对于所有的$n  \in \Z^+$成立.$f \circ I(n) = I \circ f(n) = \sum_{d \mid n}f(d)$.



引理 $I \circ \mu = \mu \circ I = \mathbb{I}$.

[证明]

$I\circ \mu (1) = I(1)\mu(1) = \mu(1)I(1) = 1 = \mathbb{I}(1)$.

$I \circ \mu(n) = \sum_{d\mid n} \mu(d) = \mu\circ I (n) = 0 = \mathbb{I}(n)$

$\square$



定理$2$ $(\text{M}\ddot{\text{o}}\text{bius Inversion Theorem})$ 令$F(n) = \sum_{d \mid n}f(d)$则$f(n) = \sum_{d \mid n}\mu(d)F(n/d)$

[证明]

不难发现$F = f \circ I$因此$F(n/d) = f \circ I(n/d) = I \circ f(n/d)$

因此得到
$$
f(n) = \mu \circ F(n) =  \mu \circ I \circ f(n) =\mathbb{I}\circ f(n) = f(n)
$$
$\square$



> 我们考虑正整数上的复值函数.注意到只要函数在$\text{Abel}$群中取值,定理$2$就成立.证明方式一字不差.

若将$\text{Abel}$群中的加法群结构写为乘法结构,则定理表现为如下形式:若$F(n) = \prod_{d \mid n}f(d)$则$f(n) = \prod_{d \mid n} F(n/d)^{\mu(d)}$.

$\text{M}\ddot{\text{o}}\text{bius}$反演定理有很多种作用.我们将用它来得到另一个数论函数的公式,$\text{Euler } \phi$函数.$\phi(n)$定义为$1$到$n$之间与$n$互素的整数个数.举个例子$\phi(1) = 1,\phi(5) =4$,$\phi(6) = 2$以及当$p$为素数时有$\phi(p) = p-1$.



命题$2.2.4$ $\sum_{d \mid n} \phi(d) = n$

[证明]

考虑$n$个有理数$1/n,2/n,\cdots,(n-1)/n,n/n$将其化为最简形式,那么每个数均表示为互素数的商.其分母必然是$n$的因数.

若$d\mid n$则总是存在$\phi(d)$个数的最简形式的分母为$d$.(若$(m,d) = 1$由于$d \mid n$因此$\frac{n}{d}$是整数,因此$\frac{m \times \frac{n}{d}}{n}$为$n$个有理数中的一个,其最简形式为$\frac{m}{d}$,若$(m,d) = c\neq 1$则有$m = cm'$且$d = cd'$即$\frac{m}{d} = \frac{cm'}{cd'} = \frac{m'}{d'}$) 

于是有$\sum_{d \mid n}\phi(d) = n$$\square$



命题$2.25$ 若$n = p_1^{a_1}p_2^{a_2}\cdots p_l^{a_l}$则
$$
\phi(n)= n(1- \frac{1}{p_1})(1- \frac{1}{p_2})\cdots(1- \frac{1}{p_l})
$$
[证明]

由于$\sum_{d\mid n}\phi(d) = n$因此我们可以对于$n$使用$\text{M}\ddot{\text{o}}\text{bius}$反演定理,即令$F(n) = \sum_{d \mid n}\phi(n)$得到$\phi(n) = \sum_{d \mid n}\mu(d) F(n/d) = \sum_{d \mid n} \mu(d)(n/d) = \sum_{d \mid n} n (\mu(d)/d)$.

接下来延续命题$2.2.3$中的证明得到当$d = p_1^{\varepsilon_1}p_2^{\varepsilon_2}\cdots p_l^{\varepsilon_l}$,$\varepsilon_i = 0,1$时$\mu(d)\neq 0$.

因此得到
$$
\phi(n) = n(\sum_{p_i}\frac{1}{p_i}+(-1)\sum_{i \neq j}\frac{1}{p_ip_j}+(-1)^2\sum_{i \neq j \neq k}\frac{1}{p_ip_jp_k}+\cdots + (-1)^l\frac{1}{\prod_{i = 1}^lp_i}) = n(1-\frac{1}{p_1})(1-\frac{1}{p_2})\cdots(1-\frac{1}{p_l})
$$
$\square$



稍后,我们将对于这个公式进行一个更为深刻的证明.我们还将使用$\text{M}\ddot{\text{o}}\text{bius}$来确定$k[x]$中固定次数的单不可约多项式的个数,其中$\mathbb{k}$是一个有限域.



## $\S 3 \quad\sum 1/p$发散

我们从证明$\Z$中有无穷多个素数开始本章,最后,我们将证明一个更强的命题,这个证明将引用无穷级数理论中的一些基本事实.



定理$3$ $\sum 1/p$是发散的,这里的和是$\Z$中所有的正素数之和.

[证明]

令$p_1,p_2,\cdots,p_{l(n)}$为所有小于$n$的素数且定义$\lambda(n) = \prod_{i = 1}^{l(n)}(1-1/p_i)^{-1}$.因为$(1-1/p_i)^{-1} = \sum_{a_i = 1}^\infty 1/p^{a_i}$我们可以发现
$$
\lambda(n) = \sum(p_1^{a_1}p_2^{a_2}\cdots p_l^{a_{l}})^{-1}
$$
这个求和的对象是所有的非负整数构成的$l-$元组$(a_1,a_2,\cdots,a_l)$.

特别地,我们发现$1+1/2+1/3+\cdots+1/n < \lambda(n)$(根据唯一因式分解得到对于$i$有$i = p_1^{a'_1}p_2^{a'_2}\cdots p_l^{a'_l}$因此得知$1/i = 1/p_1^{a'_1}p_2^{a'_2}\cdots p_l^{a'_l}$,而$1\to n$最多只占用$n$个$l-$元组,而$\lambda(n)$的求和对象为无穷多个$l-$元组)

因此由于调和级数发散可知$\lambda(n)$在$n \to \infty$时趋于无穷,这也就给出了一个证明,即存在无穷多个素数.

接下来,考虑$\log \lambda(n)$我们有
$$
\log \lambda(n) &=& -\sum_{ i =1}^l \log(1-1/p_i) = \sum_{i = 1}^l \sum_{m = 1}^\infty 1/(mp_i^m)\\
&=& p_1^{-1}+p_2^{-1}+\cdots+p_l^{-1}+\sum_{i=1}^l\sum_{m = 2}^\infty 1/(mp_i^m)
$$
接下来我们证明$\sum_{i = 1}^l \sum_{m = 2}^\infty 1/(mp_i^m)$是收敛的.

由于$\sum_{m = 2}^\infty 1/(mp_i^m)\leq \sum_{m = 2}^\infty p_i^{-m}\leq p_{i}^{-2}(1-p_i^{-1})^{-1}\leq 2p_i^{-2}$.

因此有$\log \lambda (n)<p_1^{-1}+p_2^{-1}+\cdots+p_l^{-1}+ 2\sum_{i = 1}^l p_i^{-2}<p_1^{-1}+p_2^{-1}+\cdots+p_l^{-1}+ 2\sum_{n = 1}^\infty n^{-2}$由于$\sum_{n = 1}^\infty n^{-2}$是收敛的,因此有$2\sum_{i = 1}^\infty p_i^{-2}$是收敛的.若$\sum1/p$是收敛的,则存在一个常数$M$使得$\log \lambda(n)<M$即$\lambda(n) < e^M$,这与$n \to \infty$时$\lambda(n)\to \infty$矛盾.$\square$



对于环$k[x]$也可以类比定理$3$的证明过程进行构造,其中$\mathbb{k}$是一个有$q$个元素的有限域.正素数$p$的作用被首一不可约多项式$p(x)$所代替.一元多项式$f(x)$的"大小"由数值$q^{\text{deg } f(x)}$给出.

其原因在于对于正整数$n$,(接下来涉及到序数理论)$n$可以表示所有小于$n$的非负整数的个数,即$\{0,1,\cdots,n-1\}$.类似地,$q^{\text{deg}f(x)}$表示度数小于$\text{deg }f(x)$的多项式个数.很容易发现.任何符合前文约束的多项式都可以写为$a_0x^m+a_1x^{m-1}+\cdots+a_{m-1}x+a_m$的形式,其中$m = \text{deg } f(x) -1$且有$a_i \in \mathbb{k}$.因此$a_i$有$q$种选择,而且每个$a_i$的选择是相互独立的.因此有$q^{m+1} = q^{\text{deg }f(x)}$个这样的多项式.



定理$4$ $\sum q^{-\text{deg }p(x)}$发散,其中求和对象$p(x)$为$k[x]$中所有首一不可约多项式.

[证明]

我们先证明$\sum q^{-\text{deg} f(x)}$是发散的以及$\sum q^{-2\text{deg }f(x)}$是收敛的,其中求和的$f(x)$是$k[x]$中所有多项式,这些结果都来自于$k[x]$中$n$度的首一多项式有$q^n$个这一事实.

考虑$\sum_{\text{deg } f(x)\leq n} q^{-\text{deg }f(x)}$得到其和等于$\sum_{m = 0}^{n}q^m q^{-m} = n+1$.因此得到$\sum q^{-\text{deg }f(x)}$是发散的.类似地,有$\sum_{\text{deg }f(x)\leq n} q^{-2\text{deg }f(x)} =\sum_{m = 1}^n q^mq^{-2m} = (1-1/q)^{-1}$.因此得到$\sum q^{-2\text{deg }f(x)}$是收敛的.

接下来的证明过程与定理$3$的证明过程大同小异

考虑阶数小于$n$的所有首一不可约多项式$p(x)$将其记为$p_1,p_2,\cdots,p_{l(n)}$.

记$\lambda(n)  = \prod_{i = 1}^{l(n)}(1-q^{-\text{deg }p_i(x)})^{-1}$由于$(1-q^{-\text{deg }p_i(x)})^{-1} = \sum q^{-a_i \text{deg }p_i(x)}$

因而得知$\lambda(n) = \sum q^{-(a_1\text{deg }p_1(x)+ a_2\text{deg }p_2(x)+\cdots +a_{l(n)}\text{deg }p_{l(n)}(x))}$

其求和对象$(a_1,a_2,\cdots,a_l)$为一个$l$元组取遍所有非负整数.

因此得知$\sum q^{-\text{deg }f(x)}< \lambda(n)$.因此$\lambda(n) \to \infty (n \to \infty)$

考虑$\log \lambda(n)$得到
$$
\log \lambda(n) &=& \sum_{i = 1}^{l(n)}\log (1-q^{-\text{deg }p_i(x)})^{-1} = \sum_{i = 1}^{l(n)}\sum_{m = 1}^\infty (m q^{m\text{deg }p_i(x)})^{-1}\\
&=& \sum_{i = 1}^{l(n)}q^{-\text{deg }p_i(x)} + \sum_{i = 1}^{l(n)}\sum_{m = 2}^\infty(m q^{m\text{deg }p_i(x)})^{-1}
$$
由于$\sum_{m = 2}^\infty (mq^{m\text{deg }p_i (x)})^{-1}< \sum_{m = 2}^\infty q^{-m \text{deg }p_i(x)}= (1- q^{-\text{deg }p_i(x)})^{-1} q^{-2 \text{deg }p_i (x)}< 2q^{-2\text{deg }p_i(x)}$

因此
$$
\log \lambda (n) < \sum_{i = 1}^{l(n)}q^{-\text{deg }p_i (x)}+ 2\sum_{i = 1}^{l(n)}q^{-2\text{deg }p_i(x)}
$$
由前文得到$\sum q^{-2\text{deg }p_i(x)}$收敛.且$\lambda(n) \to \infty (n \to \infty)$因此$\log \lambda (n) \to \infty (n \to \infty)$得到$\sum q^{-\text{deg }p_i(x)}$是发散的

$\square$



## $\S 4 \quad \pi(x)$的进一步讨论

在$\text{Chapter }1$中我们曾介绍$\pi(x)$为$1< p\leq  x$的素数$p$的个数.在足够大的$x$下研究$\pi(x)$涉及到解析方面的知识.我们将在本节中证明几个结果,这些结果需要一些分析中的结论.事实上,这里只用到了对数函数最简单的性质.

我们从$\text{Euclid}$的论证(定理$1$)的以下结论开始,其给出了$\pi (x)$的一个弱下界,我们将使用$\log x$表示以自然对数为底数的$x$的对数.



命题$2.4.1$ $\pi(x)\geq \log(\log x)$,$x \geq 2$

[证明]

令$p_n$为第$n$个素数.由于任意可以整除$p_1p_2\cdots p_n+1$的素数均与$p_1,p_2,\cdots,p_n$互异.这就说明了$p_{n + 1}\leq p_1p_2\cdots p_n+1$.现在,$p_1<2^{(2^1)}$,$p_2<2^{(2^2)}$以及$p_n < 2^{(2^n)}$.

> $p_n < 2^{2^n}$处实际上使用了一个数学归纳法,但是文中并未明确指出,此处是先假设$p_n <2^{(2^n)}$再证明$p_{n+1}<2^{(2^{n+1})}$

则$p_{n+1}\leq2^{(2^1)}2^{(2^2)}\cdots 2^{(2^n)}+1 = 2^{\sum_{i = 1}^n 2^i}=2^{2^{n+1}-2}+1<2^{(2^{n+1})}$这就说明了$\pi(2^{2^{n+1}})\geq n$.对于$x>2$选择一个整数$n$使得$e^{(e^{n-1})}<x<e^{e^n}$.若$n>2$则$e^{n-1}>2^n$

即
$$
\pi(x)>\pi(e^{e^{n-1}})\geq \pi(e^{2^n})\geq \pi(2^{2^n})\geq n
$$
这也就证明了$x > e^e$的情况,对于$x\leq e^e$时不等式是显然的.$\square$



命题$2.2.1$后一段的方法(即将$n<N$的所有素数写为$ab^2$的形式进行拼凑)可以证明$\pi(x) \to \infty$,这也可以用来改进上面的命题.若$n$是一个正整数,令$\gamma(n)$表示可以整除$n$的素数所构成的集合.



命题$2.4.2$ $\pi(x) \geq (\log x)/2$,$\log$的底数为$2$

[证明]

对于任意由素数所构成的集合$S$定义$f_S(x)$表示满足$1\leq n \leq x$且$\gamma(n)\subset S$的整数$n$的个数.假设$S$是一个包含$t$个元素的有限集.

将$n$写为$n = m^2s$的形式,其中$s$无平方因子,我们可以发现$m \leq \sqrt{x}$且$s$至多有$2^t$种选择(素数个数对应于$S$中的元素个数).因此可以推出$f_S(x)\leq 2^t \sqrt{x}$.

令$\pi(x) = m$则$p_{m+1}>x$若$S = \{p_1,p_2,\cdots,p_m\}$则$f_S(x) = x$这就推出
$$
x \leq 2^m \sqrt{x} =2^{\pi(x)}\sqrt{x}
$$
因此得到了$\sqrt{x}\leq 2^{\pi(x)}$即$\frac{1}{2}\log x \leq \pi(x)$.$\square$



有一个非常有意思的发现就是上述方法同样可以用来给定理$2$提供一个额外的证明.若$\sum 1/p_n$收敛则存在一个$n$使得$\sum_{j > n}1/p_j < \frac{1}{2}$.若$S = \{p_1,\cdots,p_n\}$则$x - f_S(x)$为$\gamma(m)\nsubseteq S$且$m\leq x$的整数$m$的个数.也就是说,存在一个素数$p_j$,$j>n$使得$p_j \mid m$.对于这样的素数其$[x/p_j]$倍不会超过$x$,因此

> 也就是说对于$p_j<x$有$[x/p_j]$个$m$满足条件,但是显然会有重复的$m$,即存在$m$使得$p_i \mid m$且$p_j \mid m$其中$i,j>n$且$i \

$$
x - f_S(x) \leq 	\sum_{j>n}\left[\frac{x}{p_j}\right] \leq \sum_{j >n}\frac{x}{p_j}<\frac{x}{2}
$$
因此有$f_S(x)\geq \frac{x}{2}$.另一方面$f_S(x)\leq 2^n \sqrt{x}$即$2^n \geq \sqrt{x}/2$.

这对于$n$固定且$x$足够大时不等式是不成立的.因此$\sum 1/p_n$不是收敛的.



一个与$\pi(x)$密切相关的函数定义为$\theta(x) = \sum_{p \leq x} \log p$,其求和对象为所有不超过$x$的素数$p$.我们将使用$\theta(x)$对于$\pi(x)$求一个上界.令$\theta(1) = 0$



命题$2.4.3$ $\theta(x)<(4\log 2)x$

[证明]

考虑二项式系数
$$
{2n \choose n} = \frac{(n+1)\cdots 2n}{n!}
$$
显然有这个整数可以被$n<p<2n$的所有素数$p$所整除(这是因为$1$到$n$中没有能够整除$p$的数,但是${2n \choose n}$是一个整数,若$p \nmid {2n\choose n}$则$\frac{(n+1)\cdots (p-1)(p+1)\cdots(2n)}{n!}$是一个以$p$为分母的既约分数,也就说明$p$是$n!$的因子,由于$p$是素数,根据$\text{Chapter 1}\S 1$的推论$1$得到存在某个$i \in \{1,2,\cdots,n\}$使得$p \mid i$这显然不成立,因此$p\mid {2n\choose n}$).此外,由于
$$
(1+1)^{2n} = \sum_{i = 1}^{2n}{2n \choose i} , 2^{2n}>{2n \choose n}
$$
因此
$$
2^{2n}>{2n \choose n}>\prod_{p>n}^{p<2n} p
$$
因此有
$$
2n\log2>\sum_{p>n}^{p<2n}\log p = \theta(2n) - \theta(n)
$$
取$n = 1,2,4,8,\cdots,2^{m-1}$得到
$$
\theta(2^m)<(\log2)(2^{m+1}-2)<(\log2)(2^{m+1})
$$
于是若$2^{m-1}<x<2^{m}$有$\theta(x)<\theta(2^{m})<(\log 2)(2^{m+1}) = (4\log2)2^{m-1} <(4\log2)x$.$\square$



推论$1$ 存在一个正整数$c_1$使得$\pi(x)<c_1\frac{x}{\log x}$对于$x \geq 2$成立.

[证明]
$$
\theta(x)&\geq& \sum_{p>\sqrt{x}}^{p\leq x}\log p \\
&\geq& (\log \sqrt{x})(\pi(x) - \pi(\sqrt{x}))\\
&\geq& (\log \sqrt{x})\pi(x) - \sqrt{x}\log\sqrt{x}
$$
其中$\sum_{p > \sqrt{x}}^{p \leq x} \log p\geq (\log\sqrt{x})(\pi(x) - \pi(\sqrt{x}))$这一步本质上是一个放缩,对于$\sum_{p \geq \sqrt{x}}^{p \leq x}\log p$中的每一项都有$\log p >\log {\sqrt{x}}$.而且统共有$\pi(x) - \pi(\sqrt{x})$项.故可以放缩.

因此得到
$$
\pi(x)\leq \frac{2\theta(x)}{\log x} + \sqrt{x}
$$
结合命题$2.4.3$有
$$
\pi(x)\leq \frac{2\times (4\log 2)x}{\log x} +\sqrt x = \frac{8x\log2}{\log x}+\sqrt{x}
$$
注意到$\sqrt{x}< \frac{2x}{\log x}$即$\log x < 2\sqrt{x}$对于$x \geq 2$成立(此处可以构造函数$f(x) = \log x - 2\sqrt{x}$进行求导得到$f'(x) = \frac{1}{x} - \frac{1}{\sqrt{x}}$在$x>1$时单调递减$f(1) <0$且根据前文设$\log x$为分母得知$x$不能取$1$因此得到$\log x <2\sqrt{x}$对于$x \geq 2$成立)$\square$



推论$2$ $x \to \infty$时$\frac{\pi(x)}{x}\to 0$.

[证明]

由于$\frac{\log_2 x}{2}<\pi(x) <c_1 \frac{x}{\log x}$因此得到$\frac{\log_2 x}{2x}<\frac{\pi(x)}{x}<c_1 \frac{1}{\log x}$由于$\frac{\log_2 x}{2x}\to 0,\frac{c_1}{\log x}(x \to \infty)$因此得知$x \to \infty , \frac{\pi(x)}{x}\to 0$$\square$



 从下边开始我们将检验二项式系数${2n \choose n}$来给$\pi(x)$定界.首先
$$
{2n \choose n} = \left(\frac{n+1}{1}\right)\left(\frac{n+2}{2}\right)\cdots \left(\frac{n+n}{n}\right) \geq 2^n
$$
另一方面,根据本章结尾的$\text{Exercise 6}$我们有
$$
\text{ord}_p {2n \choose n} = \text{ord}_p \frac{(2n)!}{(n!)^2} = \sum_{j = 1}^{t_p} \left(\left[\frac{2n}{p^j}\right] - 2\left[\frac{n}{p^j}\right]\right)
$$
其中$t_p$是使得$p^{t_p}<2n$的最大$t_p$.因此有$t_p = [\log 2n / \log p]$.不难发现$[2x] - 2[x]$要么为$1$要么为$0$.因此有
$$
\text{ord}_p {2n \choose n}\leq \frac{\log 2n}{\log p}
$$

## $\text{\large{E}\small{XERCISES}}$

1. 若$\mathbb{k}$是一个有限域则$k[x]$中有无穷多个不可约多项式

   

   设$|\mathbb{k}| = q$ .

   假设$k[x]$只有有限个不可约多项式,将其记为$p_1,p_2,\cdots,p_{l}$

   对于任意的首一多项式$f(x) \in k[x]$考虑唯一因式分解得到$f = c_1\prod p^{a(p)}$

   因此$f$可以写为$ab^2$的形式,其中$a = p_1^{a_1}p_2^{a_2}\cdots p_l^{a_l}$其中$a_i = 0$或$1$取决于$2$能否整除$\text{ord}_{p_i} f$.

   因此得到$a$共有$2^l$种组合.

   由于显然有$b^2 < f$因此$b$有$q^{[\frac{1}{2}\text{deg }f]}$种组合

   得知

   $q^{\text{deg }f} < 2^l q^{\frac{1}{2}\text{deg }f}$因此得到$q^{\frac{1}{2}\text{deg }f}< 2^l$.

   这对于$\text{deg }f$足够大时是不成立的.

   

2. 令$p_1,p_2,\cdots,p_t \in \Z$且均为素数,考虑所有形如$r = a/b$其中$\text{ord}_{p_i}a \geq \text{ord}_{p_i}b$($i = 1,2,\cdots, t$)的所有有理数构成的集合$S$.证明这个集合构成一个环且$p_1,p_2,\cdots,p_t$是环上唯一的素数.

   

   考虑$r_1=a/b,r_2  =c/d \in S$有$r_1 + r_2 = (ad+bc)/(bd)$得到$\text{ord}_{p_i}(ad+bc) \geq \max (\text{ord}_{p_i}ad,\text{ord}_{p_i}bc)$

   由于$\text{ord}_{p_i} ad = \text{ord}_{p_i}a + \text{ord}_{p_i}d$且有$\text{ord}_{p_i}a\geq \text{ord}_{p_i}b$因此有$\text{ord}_{p_i}(ad+bc)\geq \text{ord}_{p_i}bd$因此$r_1 + r_2 \in S$同理得到$r_1 - r_2 \in S$

   $r_1r_2 = ac/bd$根据前文推导得知$r_1r_2\in S$

   因此$S$构成环.

   对于$p_i$由于$\text{ord}_{p_i}a \geq \text{ord}_{p_i}b$因此不存在$a/b$使得$a/b \mid p_i$.

   因此$p_i$是素元.

   若还存在其他的素元$c/d$由于$\text{ord}_{p_i}c \geq \text{ord}_{p_i}d$因此得到$c/d$对于所有的$p_i$都有$\text{ord}_{p_i}c = \text{ord}_{p_i} d = 0$因此$c$和$d$必然由$\Z$中的其它素数构成.

    因此我们可以将其它可能存在的素元转化为素数以及素数的倒数的形式.

   比如$p$和$1/p$

   但是由于$1/p \times p^2 = p$且$1/p, p^2 \in S$因此有$1/p \mid p$得到$p$不是素元

   同理得到$1/p$也不是素元

   因此$p_1,p_2,\cdots,p_t$是环上唯一的素元.

   

3. 使用$\phi(n)$的公式给出具有无穷多个素数的证明.

   

   假设只有有限多个素数,将其记为$p_1,p_2,\cdots,p_l$

   根据命题$2.25$得到若$n = p_1p_2\cdots p_l$则有
   $$
   \phi(n)= n(1- \frac{1}{p_1})(1- \frac{1}{p_2})\cdots(1- \frac{1}{p_l})
   $$
   因此得到$\phi(n) = n \frac{(p_1 - 1)(p_2 - 1)\cdots (p_l -1)}{p_1p_2\cdots p_l} = (p_1 - 1)(p_2 - 1)\cdots (p_l - 1)$.

   由于只有有限多个素数,因此$\phi(n) = 1$

   但是显然有$(p_1 - 1)(p_2 - 1)\cdots (p_l - 1)\neq 1$

   因此得到素数应当有无穷多个.

   

4. 若$a$是一个非零整数,则对于$n>m$证明$(a^{2^m}+1,a^{2^n}+1) = 1$或$2$取决于$a$是奇数还是偶数

   

   首先证明$(a^{2^m}+1,a^{2^n}+1)$只能为$1$或者是$2$.

   假设存在奇素数$p \mid a^{2^m}+1$则考虑$n>m$.

   有$a^{2^n}-1 = (a^{2^{n-1}}+1)(a^{2^{n-2}}+1)\cdots (a^{2^{m}}+1)(a^{2^{m}}-1)$

   因此得到$p \mid a^{2^n}-1$

   若有$p \mid a^{2^n}+1$

   则由于$a^{2^n}+1 - (a^{2^n}-1) = 2$即$(a^{2^n}+1,a^{2^n}-1)\leq 2$得到$2 \mid p$与$p$是一个奇素数矛盾.

   因此不存在奇素数$p$使得$p \mid a^{2^m}+1$且$p \mid a^{2^n}+1$因此得到$(a^{2^m}+1,a^{2^n}+1)$只有可能为$1$或$2$

   若$a$为一个奇数则$a^{2^i}+1$均为偶数($i$为正整数),即$(a^{2^m}+1,a^{2^n}+1) = 2$.

   若$a$为一个偶数则$a^{2^i}+1$均为奇数,即$2 \nmid a^{2^i}+1$因此有$(a^{2^m}+1,a^{2^n}+1) = 1$

   因此得知$(a^{2^m}+1,a^{2^n}+1) = 1$或$2$取决于$a$是奇数还是偶数

   

5. 使用4的结果证明素数时无穷多个的

   

   假设只有$t$个素数

   取$a = 2$得到对于任意的$n \neq m$都有$(a^{2^m}+1,a^{2^n}+1) = 1$因此考虑其唯一因式分解得知它们没有共同的素因子

   由于$n$可以取遍所有正整数

   因此得到素数是由无穷多个的

   

6. 对于有理数$r$定义函数$[r]$为向下取整函数,证明$\text{ord}_{p} n! = [n/p]+[n/p^2]+\cdots $ 

   

   $\text{ord}_{p} n! = \text{ord}_p 1+\text{ord}_p 2+ \cdots +\text{ord}_p n$

   由于$[n/p] \times p$是小于$n$的最大的$p$的倍数,因此对于小于$n$的整数中有$[n/p]$个整数$i$的$\text{ord}_p i \geq 1$

   同理得到有$[n/p^2]$个$i$的$\text{ord}_p i \geq 2$.那么对于$\text{ord}_p i = 2$有$\text{ord}_p i \geq 1$因此得知$i$被$[n/p]$中计算过一次,因此我们只需要再计算一次即可.-

   因此得知$\text{ord}_p n! = [n/p]+[n/p^2]+\cdots$

   

7. 

