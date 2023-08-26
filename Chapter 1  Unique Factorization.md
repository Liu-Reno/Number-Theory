# Content

[TOC]

# Chapter 1 : Unique Factorization

$\text{The notion of prime number is fundamental in number theory. The first part of this chapter is devoted to proving that every integer  can be written as a product}$

$\text{ of primes in an essentially unique way.}$

$\text{After that, we shall prove an analogous theorem in the ring of polynomials over a field.}$

$\text{On a more abstract plane, the general idea of unique factorization is treated for principal ideal domains.}$

$\text{Finally, returning from the abstract to the concrete, the general theory is applied tv two special rings that will be important later in the book.}$



## $\S 1\quad \Z$的唯一因数分解

作为第一近似,数论可以被定义为对于自然数$1,2,3,\cdots,L$的研究.$\text{Kronecker}$曾经说过(泛指数学),上帝创造了自然数,其余的都是人类的工作.尽管自然数在某种意义上构成了最基本的数学体系,但对于自然数性质的研究给一代又一代的数学家带来了具有无穷魅力的问题.

对于两个自然数$a,b$若存在一个自然数$c$使得$b= ac$则说$a$整除$b$.若$a$整除$b$,我们使用符号$a\mid b$来表示.举个例子$2\mid 8,3\mid 15$但是$6\nmid 21$.若我们给定一个数,我们很容易把它一遍又一遍的分解,直到无法再分解.举个例子$180 = 18 \times 10 = 2 \times 9 \times 2 \times 5 = 2\times 3 \times 3 \times 2 \times 5$.这些不能被进一步分解的数称为素数$(\text{primes})$.更精确的说,若一个数$p$只能被$1$和$p$整除,我们就说它是素数.素数非常重要,因为每个数字都可以写为素数的乘积.此外,素数之所以引起人们的极大兴趣,是因为素数的许多问题很容易表述但是很难证明.事实上,许多关于素数的老问题至今无法得到解决.

排在最前边的几个素数是$2,3,5,7,11,13,17,19,23,29,31,37,41,43,\cdots$.有人可能会问素数是否是无穷多个的.回答是肯定的.$\text{Euclid}$在距今$2000$多年前给出了一个优雅的证明.我们将在第二章给出他和其他几个人的证明.令$\pi(x)$为在$1$到$x$之间的素数个数.$\pi(x)$有什么有趣的性质呢?几位数学家通过试验发现,当$x$较大时,函数$\pi(x)$近似等于$\frac{x}{\ln x}$.这个论断被称为素数定理,在$19$世纪末由$\text{J. Hadamard}$证明,并且由$\text{Ch-J. de la Vall\'{e} Poussin}$.更准确的说,他们证明了
$$
\lim_{x \to \infty}\frac{\pi(x)}{x/\ln x} = 1
$$
即使从一个很小的素数列表中,人们也可以注意到它们具有成对出现的趋势,例如$3$和$5$,$5$和$7$,$11$和$13$,$17$和$19$.是否存在无穷的素数对?这是至今无法回答的问题.



另一个著名的未解之谜是$\text{Goldbach}(\text{C.G.Goldbach})$猜想.每个偶数都可以写为两个素数之和吗?$\text{Goldbach}$通过实验得出这个猜想.如今,电子计算机可以使用非常大的数字进行实验.$\text{Goldbach}$猜想的反例从未被发现过.$\text{I.M. Vinogradov}$和$\text{L.Schnirelmann}$在校对方面取得了很大的进展.$1937$年$\text{Vinogradov}$证明了每一个足够大的数都是三个奇素数之和.

在本书中,将不会深入研究素数分布或关于它们"可加性"的问题.相反,我们关注的是素数如何进入数字的乘法结构.这些主要的定理可以追溯到$\text{Euclid}$年代.它就是唯一分解定理$(\text{unique factorization})$.这个定理有时也被称为算术基本定理$(\text{fundamental theorem of arithmetic})$,这是当之无愧的.某种程度上,我们将要讨论的几乎所有结果都取决于它.该定理指出,任何一个数字都可以以唯一的方式分解为质数的乘积.下面将解释唯一性的含义.

以数字$180$为例.我们知道$180 = 2\times 2\times 3\times 3 \times 5 = 2^2\times 3^2 \times 5$.在这种情况下,唯一性指的是能够整除$180$的素数只有$2,3,5$.其指数$2,2,1$是唯一由$180$所确定的.

$\Z$表示整数环,即集合$0,\pm 1,\pm 2, \pm 3 ,\cdots$,加法与乘法定义为最常见的加法与乘法.用$\Z$来操作要比使用正整数方便得多.整除的概念可以毫不费力的扩张到$\Z$上.若$p$为一个正素数,则$-p$也是一个素数.我们不将$1,-1$考虑为素数即使它们确实符合定义.这只是一个有用的约定.注意到,$1.-1$是唯二拥有整除所有数这一性质的整数.它们被称为$\Z$的单位.注意到每一个非零数都可以整除$0$.依照惯例,$0$不作为被除数.

除法有一些简单的性质,我们将简单列出.

1. $a\mid a,a \neq 0$
2. 若$a\mid b$且$b \mid a$则$a = \pm b$.
3. 若$a\mid b$且$b \mid c$则$a \mid c$
4. 若$a\mid b$且$a \mid c$则$a\mid b+c$.

令$n \in \Z$且$p$为一个素数.则若$n$非零,就存在一个非负整数$a$使得$p^a \mid n$且$p^{a+1}\nmid n$($a$可以等于$0$).很容易看出若$p$和$n$都是正的,那么$p$的幂会不断增大,直至超过$n$.其他的情况也很容易被归结到这种结果上.数字$a$称为$p$的$n$阶并使用$\text{ord}_p n$表示.粗略的说,$\text{ord}_p n$是$n$能被$p$所整除的次数.若$n = 0$我们设置$\text{ord}_p n = \infty$注意到$\text{ord}_p n = 0$当且仅当$p \nmid n$.

 引理 $1$ 每一个非零整数都可以写为素数的乘积.

[证明]

假设整数使其不能写为素数的乘积

我们取$N$为这样的整数中的最小正整数(由于正整数集有下界,因此若上述假设成立,必然存在一个最小的符合上述特征的正整数).则显然其不为一个素数,所以必然存在一个$m$使其不为素数且可以整除$N$因此得到$N = mn$其中$1<m,n<N$然而对于$m,n$都有其小于$N$,因此其可以写为素数的乘积,即$N$也可以写为素数的乘积,这与$N$是最小的不能写成素数的乘积的正整数相矛盾.

也可以使用数学归纳法进行更精确的证明,我们只需要证明对于正整数的情况成立即可.

首先对于$2$有$2$为素数自然可以写为素数的乘积,接下来假设$2<N$,然后对于任意的$2\leq m<N$均可以写为素数的乘积,对于$N$,若$N$为素数,则自然可以写为素数的乘积,若$N$不为素数,则存在$m$使得$N = mn$其中$1<m,n<N$因此可以证明$N$可以写为素数的乘积.$\square$



不难发现我们可以写为$n = p_1^{a_1}p_2^{a_2}\cdots p_m^{a_m}$的形式.其中$p_i$是素数且$a_i$是非负整数.我们将使用下述记号
$$
n = (-1)^{\varepsilon(n)}\prod_p p^{a(p)}
$$


其中$\varepsilon(n) = 0,1$取决于$n$是否是一个正数,可以理解为一个$\text{sgn}$函数.指数$a(p)$是非负整数,当然除了有限个素数以外都有$a(p) = 0$.

我们现在就可以证明核心的定理了.

定理 $1$ 所有非负整数$n$都存在一个指数由$n$唯一确定的因数分解.
$$
n = (-1)^{\varepsilon(n)}\prod_p p^{a(p)}
$$
事实上,我们有$a(p) = \text{ord}_p n$.

这个定理的证明没有看上去那么简单.我们将在确定了一些初步结果之后对其进行证明.

引理 $2$ 若$a,b \in \Z$且$b>0$,则存在$q,r\in \Z$使得$a = qb+r$且$0\leq r<b$.

[证明]

考虑所有$a- xb,x \in \Z$形式的整数.这个集合至少包含一个正整数.令$r = a - qb$为这个集合中的最小正整数.我们断言$0 \leq r <b$,若不成立,则$r = a - qb \geq b$即$0<a - (q+1)b \leq r$这与$r$是$a - xb$中最小的正整数相矛盾.$\Box$



定义: 若$a_1,a_2,\cdots,a_n \in \Z$,我们定义$(a_1,a_2,\cdots,a_n)$为所有形如$a_1x_1+a_2x_2+\cdots+a_nx_n$其中$x_1,x_2,\cdots,x_n \in \Z$的整数所构成的集合.令$A = (a_1,a_2,\cdots,a_n)$.注意到$A$中任意两个元素的和与差仍然在$A$中(即$A$对于加法构成群).且对于任意的$a \in A,r\in \Z$有$ra \in A$,于是得到$rA \subset A$因此$A$是$\Z$的一个理想.



引理$3$ 若$a,b \in \Z$则有一个$d \in \Z$使得$(a,b) = (d)$

[证明]

我们假设$a,b$不全为$0$.于是在$(a,b)$中必然存在正元素.令$d$为$(a,b)$中最小的正元素.显然有$(d)\subset (a,b)$接下来我们需要证明反向包含也是成立的.

对于任意的$c \in (a,b)$,根据引理$2$可以得到存在$q,r$使得$c = qd + r$.且无论是$c$还是$d$都在$(a,b)$中,也就是说$r = c - qd$也属于$(a,b)$.由于$0\leq r<d$而$d$是$(a,b)$中最小的正元素,于是得到$r =0$因此$d \mid c$即$c \in (d)$.$\square$



定义 : 对于$a,b \in \Z$.若有一个整数$d$使得$d$同时整除$a$和$b$且对于其他所有$a$和$b$的公因子$c$都有$c\mid d$则$d$称为$a$和$b$的最大公因子$(\text{greatest common divisor})$.注意到,若存在$c$也是$a$和$b$的最大公因子,则$c \mid d$且$d \mid c$即$c = \pm d$.因此,两个数的最大公因子,若存在,则由符号函数$\text{sign}$所决定.



举个例子,我们可以检验$14$是$42$和$196$的最大公因子.下面的引理将保证最大公因子的存在性,但是不会给出计算它的方法.在$\text{Exercise}$中,我们将概述一种行之有效的计算方法,称为$\text{Euclid}$算法.



引理$4$ 若$a,b \in \Z$且$(a,b) = (d)$则$d$是$a$和$b$的最大公因子.

[证明]

由于$a,b\in (a,b) = (d)$因此可以得到$d$确实是$a,b$的公因子.对于$a,b$的某个公因子$c$,有$c$可以整除任意$ax+by$形式的整数,其中$x,y \in \Z$,因此得到$c \mid d$.$\Box$



定义 : 我们说整数$a$和$b$是互素的若其最大公因子只有$\pm 1$即单位.



虽然我们定义$(a,b)$是一个集合,但是由于$(a,b) = (d)$且$d$是一个最大公因子,因此使用$(a,b)$表示$a$和$b$的最大公因子是相当标准的.使用$(a,b)$表示两种含义不会太混乱.因此$a,b$互素当且仅当$(a,b) = 1$.



命题$1.1.1$ 假设$a\mid bc$且$(a,b) = 1$则$a \mid c$.

[证明]

因为$(a,b) = 1$因此存在$r,s \in \Z$使得$ra+sb = 1$因此$rac + sbc = c$,由于$a\mid bc$因此存在$e$使得$ea = bc$于是得到$rac+ sea = c$即$(rc+se)a = c$因此$a\mid c$.$\square$



当$(a,b)\neq 1$时,命题是错误的.举个例子$6 \mid 24$但是$6 \nmid 3$且$6 \nmid 8$.



推论$1$ 若$p$是一个素数且$p \mid bc$则要么有$p \mid b$要么有$p \mid c$.

[证明]

由于$p$的因子只有$\pm 1$和$\pm p$因此$(p,b) = 1$或$p$,若$(p,b) = p$则$p \mid b$,若$(p,b) = 1$则由于$p \mid bc$得到$p \mid c$.$\square$



我们可以用一种稍微不同的形式来表述这个推论,这种形式通常是有用的:若$p$是一个素数且$p \nmid b,p \nmid c$则$p \nmid bc$.



推论$2$ 若$p$是一个素数且$a,b \in \Z$则$\text{ord}_p ab = \text{ord}_p a + \text{ord}_p b$.

[证明]

令$\alpha = \text{ord}_p a$,$\beta = \text{ord}_p b$于是得到$a = p^\alpha c$,$b = p^\beta d$其中$p \nmid c$且$p \nmid d$因此得到$ab = p^{\alpha + \beta}cd$由于$p \nmid c$且$p \nmid d$于是有$p \nmid cd$因此$\text{ord}_p ab = \alpha + \beta = \text{ord}_p a+ \text{ord}_p b$.$\square$



现在,我们来证明定理$1$.

回顾等式
$$
n = (-1)^{\varepsilon(n)}\prod_p p^{a(p)}
$$
对于两侧同时作用一个函数$\text{ord}_q$得到
$$
\text{ord}_q n = \varepsilon(n)\text{ord}_q(-1) +\sum_p a(p)\text{ord}_qp
$$
$p \neq q$时由于$\text{ord}_q (-1) = \text{ord}_q p = 0$因此得到$\text{ord}_q n = 0$.

而$p = q$时有$\text{ord}_q n = a(q)$.这就是我们想要证明的.

需要强调的是,证明的关键步骤是推论$1$也就是说若$p \mid ab$则$p \mid a$或$p \mid b$.证明中的所有难点都集中在这个事实上.

> 这是因为若$q \mid n$则有$q \mid (-1)^{\varepsilon(n)}$或$q \mid \prod_p p^{a(p)}$
>
> 若$q\mid (-1)$则$q^{\varepsilon(n)} \mid (-1)^{\varepsilon(n)}$若$q \mid p$则$q^{a(p)} \mid p^{a(p)}$,再根据推论$2$将乘法转化为加法得到
> $$
> \text{ord}_qn = \varepsilon(n)\text{ord}_q(-1) +\sum_p a(p)\text{ord}_qp
> $$



## $\S2\quad k[x]$上的唯一因式分解

唯一分解定理可以在比$\S 1$更一般的情况下表述和证明.在本节中,我们将考虑系数在域$\mathbb{k}$中的多项式环$k[x]$.在$\S 3$中我们将考虑主理想域.事实证明,这些情况的分析将对于整数的研究有益.

若$f,g \in k[x]$,若存在$h\in k[x]$使得$g = fh$则称$f$整除$g$.

若使用$\text{deg } f$来表示$f$的度(即最高次非零项的次数),我们有$\text{deg }fg = \text{deg }f+\text{deg }g$.同理,当且仅当$f$为一个非零常数时有$\text{deg }f = 0$.这也说明$f \mid g$且$g \mid f$当且仅当$g = cf$其中$c$是一个非零常数.它还可以得出,可以整除所有其他多项式的唯一多项式是一个非零常数.这些非零常数就是$k[x]$的单位.若$q \mid p$可以推出$q$是一个常数或$q$是$p$的常数倍,那么常系数多项式$p$是不可约的$(\text{irreducible})$.不可约多项式是素数的类似物.



引理$1$ 每个非常数的多项式都可以写为若干个不可约多项式的乘积.

[证明]

通过对于度进行归纳来证明引理.

不难发现当多项式的度为$1$时多项式是不可约的(根据$\text{deg }fg = \text{deg }f+ \text{deg }g$得到若$\text{deg }fg = 1$且其可约,则$f$和$g$必然一个的度为$1$一个的度为$0$,假设$f$的度为$1$则有$g$为非零常数,即$fg$是不可约的).

现在假设我们已经对于所有的度小于$n$的多项式证明了上述引理,则考虑$\text{deg }f = n$若$f$为不可约多项式,则$f$自然可以写为自身与$1$的乘积,也就是说可以写为不可约多项式的乘积.若$f$可约则存在$f = gh$使得$1\leq \text{deg }g,\text{deg }h < n$因此根据前文假设可以得知$g$和$h$都可以写为若干个不可约多项式的乘积,也就是说$f$可以写为不可约多项式的乘积.$\square$



很自然地,可以引出首一多项式$(\text{monic polynomial})$的定义.对于多项式$f$,若其第一个(非零)系数为$1$则称其为一个首一多项式.举个例子,$x^2 + x-3$以及$x^3 - x^2 + 3x+17$都是首一的,但是$2x^3 - 5$以及$3x^4+2x^2-1$就不是首一的.每一个非零多项式都是某个首一多项式的常数倍.

令$p$为一个首一不可约多项式.我们定义$\text{ord}_p f$为一个满足$p^a \mid f$且$p^{a+1}\nmid f$的整数.由于$p^{a}$将越来越大,因此这样的整数$a$必然存在.注意到$\text{ord}_p f  = 0$当且仅当$p \nmid f$.



定理$2$ 令$f \in k[x]$与是我们可以得到
$$
f = c\prod_p p^{a(p)}
$$
其中乘积为所有的不可约多项式,且$c$为常数.常数$c$和指数$a(p)$由$f$唯一确定.事实上,$a(p) = \text{ord}_p f$.

这种乘积的存在性可以直接从引理$1$推导出来.和先前一样,唯一性的证明较为困难,我们将先推导出一些数学工具来辅助证明

引理 $2$ 令$f,g \in k[x]$若$g \neq 0$则存在多项式$h,r \in k[x]$使得$f = hg + r$其中$r$要么为$0$要么$\text{deg } r < \text{deg } g$.

[证明]

若$g \mid f$则$f = hg$即$r = 0$.

若$g \nmid f$则令$r$为$f - lg$其中$l \in k[x]$的多项式中度数最小的多项式.我们断言$\text{deg } r < \text{deg }g$否则设$r$的第一项为$ax^d$而$g$的第一项为$bx^m$.于是得到$r - ab^{-1}x^{d-m}g = f - (h+ab^{-1}x^{d-m}g)$其度数比$\text{deg }r$小,造成矛盾.$\square$

> 构建$ab^{-1}x^{d-m}g$的原因在于其第一项为$ax^d$,可以保证$r - ab^{-1}x^{d-m}g$的度数比$r$小.



定义 若$f_1,f_2,\cdots,f_n \in k[x]$则$(f_1,f_2,\cdots,f_n)$是所有形如$f_1h_1+f_2h_2+\cdots+f_nh_n$的多项式构成的集合其中$h_1,h_2,\cdots,h_n \in k[x]$.



使用环理论语言来说$(f_1,f_2,\cdots,f_n)$无非是由$f_1,f_2,\cdots,f_n$生成的理想.



引理$3$ 给定$f,g \in k[x]$存在一个$d \in k[x]$使得$(f,g) = (d)$

[证明]

令$d$为$(f,g)$中具有最小度的多项式.必然有$(d) \subset (f,g)$并且我们打算证明反向的包含也是成立的.

令$c \in (f,g)$则$\text{deg }c \geq \text{deg }d$.若$d \nmid c$则根据引理$2$可知存在$h,r \in k[x]$使得$c = hd + r$,其中$\text{deg }r < \text{deg }d$由于$(f,g)$是理想

因此$r = c-hd \in (f,g)$而$\text{deg }r < \text{deg }d$

这与$d$是$(f,g)$中具有最小度的多项式相矛盾.

因此$r$必然为$0$也就是说对于任意的$c \in (f,g)$都有$c \in (d)$.$\square$



定义 令$f,g \in k[x]$,若有$d$同时作为$f$和$g$的公因子且对于$f$和$g$的其他公因子$c$都有$c \mid d$则$d$为$f$和$g$的最大公因子.



注意到两个多项式的最大公因子之间相差常数倍.若我们要求它是首一的,则它就是唯一确定的,我们一般特指其为最大公因子.



引理$4$ 令$f,g \in k[x]$通过引理$3$可以得到有一个$d \in k[x]$使得$(f,g) = (d)$.$d$是$f$和$g$的最大公因子.

[证明]

因为$f \in (d)$且$g \in (d)$因此$d$是$f$和$g$的公因子,接下来对于任意的$c$也为$f$和$g$的公因子,有$d = h_1f+h_2g$其中$h_1,h_2 \in k[x]$于是有$c \mid d$因此$d$是最大公因子.$\square$



定义: 两个多项式$f$和$g$的最大公因子为常数时,称$(f,g)$是互素的,有$(f,g) = (1)$



命题$1.2.1$ 若$f$和$g$是互素的,则$f \mid gh$可以推出$f \mid h$.

[证明]

若$f$和$g$是互素的,我们有$(f,g) = (1)$因此存在两个多项式$l,r$使得$1 = lf + rg$因此$lfh + rgh = h$由于$f \mid gh$因此得到$f \mid h$.$\square$.



推论$1$ 若$p$是不可约多项式且$p \mid fg$则$p \mid f$或$p \mid g$.

[证明]

因为$p$是不可约多项式,因此对于任意的$f \in k[x]$都有$p \mid f$或者$(p,f) = (1)$.若$p\mid f$则得到推论成立,若$(p,f) = (1)$则根据前文命题得到$p \mid g$.$\square$



推论$2$ 若$p$是一个首一不可约多项式且$f,g\in k[x]$就得到$\text{ord}_p fg = \text{ord}_p f+ \text{ord}_p g$.

[证明]

令$\alpha = \text{ord}_p f$且$\beta = \text{ord}_p g$则$f = p^{\alpha}c$,$g = p^\beta d,c,d \in k[x]$且$(p,c) = (p,d) = (1)$于是$p \nmid cd$.因此$fg = p^{\alpha + \beta}cd$得到$\text{ord}_p fg = \text{ord}_p f+ \text{ord}_p g$.$\square$



依照$\S 1$中的证明方式,我们在
$$
f = c\prod_pp^{a(p)}
$$
等式两侧都应用函数$\text{ord}_q$得到
$$
\text{ord}_q f = \text{ord}_q c +\sum_p a(p)\text{ord}_q p 
$$
仿照$\S 1$中的讨论得到$q \neq p$时,$\text{ord}_q f = 0$而$q = p$时有$\text{ord}_q f = a(p)$.



## $\S 3 \quad $主理想域上的唯一因式分解

读者不会没有注意到$\S 1$和$\S2$的证明方法存在巨大性的相似.在本节中,我们将证明一个抽象定理,它将前面的结果作为一个特例从而包含在内.

在本节中,$R$表示一个整环.



定义$1$ 对于$R$若存在一个函数$\lambda$将$R$中的非零元映射到集合$\{0,1,2,3,\cdots\}$上使得对于$a,b \in R$且$b \neq 0$存在$c,d \in R$且具有特性:$a = cb + d$其中$d$要么为$0$要么有$\lambda(d)<\lambda(b)$.则称$R$为一个欧几里得整环$(\text{Euclidean domain})$.



环$\Z$与$k[x]$都是欧几里得整环.在$\Z$上我们可以令绝对值为函数$\lambda$;在环$k[x]$上可以将多项式的度视为$\lambda$来达成目的.



命题$1.3.1$ 若$R$是一个欧几里得整环且$I \subset R$为一个理想,则存在一个元素$a \in R$使得$I = Ra = \{ra : r \in R\}$.

[证明]

考虑非负整数$\{\lambda(b) : b \in I,b \neq 0\}$所构成的集合.由于每个非负整数所构成的集合均存在一个最小元,此处为一个$a \in I , a \neq 0$且$\lambda (a)\leq \lambda(b)$对于所有的$b \in I ,b \neq 0$成立.

我们断言$I = Ra$.由于$I$是一个理想,且$a \in I$,显然有$Ra \subset I$,取$b \in I$可以得到存在$c,d \in R$使得$b = ac + d$其中$d$要么为$0$要么有$\lambda(d)<\lambda(a)$.由于$I$是一个理想,于是可以得到$b - ca \in I$即$d \in I$若有$d \neq 0$则$d$与$\lambda(a) = \inf \{\lambda(b): b \in I ,b \neq 0\}$矛盾.

因此得到$I \subset Ra$.$\square$



对于元素$a_1,a_2,\cdots,a_n \in R$,定义$(a_1,a_2,\cdots,a_n) = Ra_1+Ra_2+\cdots+Ra_n = \{\sum_{i = 1}^n r_ia_i : r_i \in R\}$.$(a_1,a_2,\cdots,a_n)$是一个理想.若一个理想$I$等于$(a_1,a_2,\cdots,a_n)$其中$a_i \in I$则说$I$是有限生成的$(\text{finitely generated})$.若$I = (a)$对于某个$a \in I$成立,我们就说$I$是一个主理想.



定义$2$ 若每一个$R$中的理想都是主理想,则$R$为一个主理想环($\text{principal ideal domian (PID)})$.



命题$1.3.1$断言每个欧几里得整环都是一个$\text{PID}$.虽然我们很难提供一个真实例子,但是这种说法反过来是错误的.



本节剩下的讨论是关于$\text{PID}$的.欧几里得整环的概念是非常有用的,在实践中,人们可以通过先确定一个环时欧几里得整环而后来证明环是$\text{PID}$的.我们将在$\S 4$中给出两个更具体的例子.



我们引入更多的术语.

若$a,b \in R$且$b \neq 0$,若对于某个$c \in R$有$a = bc$我们称,$b$整除$a$.记为$b\mid a$.

一个元素$u \in R$整除$1$则称$u$为单位.

两个元素$a,b\in R$若对于某个单位$u$有$a = bu$则称$a$和$b$是关联的$(\text{associates})$.

对于一个元素$p \in R$若对于$a \mid p$都有$a$是一个单位或者与$p$关联则称$p$是不可约的.

若一个非单位元$p \in R$,有$p \mid ab$推出$p\mid a$或$p \mid b$则$p$称为一个素元.



不可约元和素元的定义是新的,但是一般来说,这两个概念并不是一致的.正如我们所见,在$\Z$和$k[x]$中它们是一致的,我们将很快证明在所有的$\text{PID}$中它们都一致.



一些我们讨论的概念可以翻译为理想的语言

$a \mid b$当且仅当$(b) \subset (a)$.

> 由于$a\mid b$因此存在$c$使得$b= ac$即$b \in Ra$即$(b) \subset (a)$

$u$是$R$的单位当且仅当$R= (u)$.

> 若$u$是$R$的单位,由于$u \mid 1$因此$(1)\subset (u)$,此外由于$(1) = R$因此得到$R \subset (u) \subset R$因此$(u) = R$

$a$和$b$是关联的当且仅当$(a) = (b)$.

> 若$a = bu$则$b \mid a$,得到$(a)\subset (b)$,且$(a) = (bu) = buR$
>
> 由于$(u) = R$因此得到$R$中存在元素$u'$使得$uu' = 1$因此得到$b = buu' \in (bu) =(a)$
>
> 因此$(b)\subset (a)$即$(b) = (a)$

$p$是一个素元当且仅当$ab \in (p)\Rightarrow a\in (p) \lor b \in (p)$.

> 由于$p \mid ab \Rightarrow p \mid a \lor p \mid b$
>
> 因此得到若$ab \in (p)$则$p \mid ab$,即$p \mid a \lor p \mid b$
>
> 因此自然可以得到$a \in (p)\lor b \in (p)$



定义 若$a,b \in R$且$d \in R$,$d$称为$a,b$之间的最大公因子$(\text{greatest common divisor(gcd)}$在不引起矛盾的时候使用$\text{gcd})$若

$(\text{a})$ $d \mid a$且$d \mid b$

$(\text{b})$ $d' \mid a$且$d' \mid b$则$d' \mid d$.

不难发现若$d$和$d'$均为$a$与$b$的$\text{gcd}$,则$d$与$d'$关联.

一般环中两个元素的$\text{gcd}$不一定存在.然而

命题$1.3.2$ 令$R$为一个$\text{PID}$且$a,b \in R$.则$a$与$b$有一个最大公因子$d$且$(a,b) = (d)$

[证明]

由于$R$是一个$\text{PID}$因此$R$中的所有理想均为主理想,也就是说必然存在一个$d\in R$使得$(a,b) = (d)$.因为$(a)\subset (d)$且$(b)\subset (d)$我们可以得到$d \mid a$且$d \mid b$.因此$d$是一个$a,b$的公因子.接下来证明$d$是$\text{gcd}$.

若有$d' \mid a$且$d' \mid b$则有$(a)\subset (d')$且$(b)\subset (d')$因此得到$(d)= (a,b)\subset (d')$即$d' \mid d$因此根据定义得到$d$确实是一个$\text{gcd}$.$\square$



对于两个元素$a,b$若它们的公因子是单位$u$,则$a$和$b$互素.

推论$1$ 若$R$是一个$\text{PID}$且$a,b \in R$是互素的,则$(a,b) = R$

[证明]

由于$(a,b) = (u) = R$直接得到结果$\square$



推论$2$ 若$R$是一个$\text{PID}$且$p \in R$是不可约的,则$p$是一个素元.

[证明]

假设$p \mid ab$且$p \nmid a$.因此有$(ab)\subset (p)$但是$a \notin (p)$.于是由于$p$是不可约的,有$a$与$p$互素.因此$(a,p) = R$

从而有$(ab,pb) = (b)$.因为$p \mid ab$因此$ab \in (p)$且$pb \in (p)$于是得到$(ab,pb)\subset (p)$因此得到$(b)\subset (p)$即$p \mid b$即$p$是一个素元.$\square$



从现在起$R$将会是一个$\text{PID}$且我们将交替的使用素元和不可约元来表述.

我们打算证明$R$中每一个非零元均可写为不可约元素的乘积.证明分为两步.第一步证明若$a \in R$且$a \neq 0$则存在一个不可约元整除$a$,紧接着我们就可以将$a$写为不可约元的乘积.



引理 $1$ 令$(a_1)\subset (a_2)\subset (a_3)\subset \cdots$为一条不断上升的理想链.则存在一个整数$k$使得$(a_k) = (a_{k+l})$其中$l  =0,1,2,\cdots$换句话说,链条将在有限步内断裂.

[证明]

令$I= \bigcup_{i = 1}^\infty (a_i)$则显然对于任意的$k \in \N$有$(a_k)\subset I$

不难发现$I$是一个理想(对于任意的$a \in I$都存在一个$k$使得$a \in (a_k)$因此有$aR \subset (a_k)$因此$aR \subset I$,且$I$显然是一个加法子群)

但是由于$R$是一个$\text{PID}$因此得知$I = (a)$对于某个$a \in R$成立.

因此存在$k$使得$a \in (a_k)$,即$I = (a)\subset (a_k)\subset (a_{k+1})\subset \cdots \subset I$.$\square$



命题$1.3.3$ 每一个$R$中的非零非单位元都可以写为不可约元的乘积.

[证明]

令$a \in R$且$a \neq 0$且$a$不是单位.

我们首先要证明$a$可以被一个不可约元素整除.若$a$是不可约元,则自然成立.

否则$a$可约,即存在$a_1,b_1$使得$a =a_1b_1$其中$a_1$和$b_1$均不是单位.

若$a_1$不可约,则我们就证明了命题,若$a_1$可约,则有$a_1 = a_2 b_2$其中$a_2,b_2$均不为单位.

若$a_2$不可约,则证明命题,若$a_2$可约则继续得到$a_3$

由于它们之间都具有整除关系,因此

$(a)\subset (a_1)\subset (a_2)\subset \cdots$最终得到存在某个$k$使得$(a_k) = (a_{k + l})$因此得知$a_k$为不可约元(不可约元的定义)

接下来再证明$a$可以写为不可约元的乘积.若$a$是不可约的,则证毕

若$a$可约,则根据前文推导可知存在$p_1$使得$p_1 \mid a$且$p_1$是不可约元.

那么有$a = p_1c_1$若$c_1$是单位元,则证毕.

若$c_1$不是单位元且可约,则存在$p_2 \mid c_1$使得$a = p_1 p_2 c_2$.

不难发现$(a)\subset (c_1)\subset (c_2)\subset \cdots$根据引理$1$可知总是存在一个$c_k$使得$c_k$是单位,由于$p_kc_k$是不可约的,因此$a = p_1 p_2 \cdots p_k c_k$,即$a$可以写为不可约元的乘积.$\square$



现在我们打算像在$\S 1$和$\S 2$一样定义一个$\text{ord}$函数.



引理$2$ 令$p$为一个素元且$a \neq 0$.则存在一个整数$n$使得$p^n \mid a$且$p^{n+1}\nmid a$

[证明]

假设不存在这样一个$n$,那么对于任意的$m >0$都有$p^m \mid a$也就是说存在$b_m$使得$a = p^m b_m$则有$pb_{m+1} = b_m$因此得到$b_{m+1}\mid b_m$即$(b_m)\subset (b_{m+1})$

那么我们可以得知$(b_1)\subset (b_2)\subset (b_3)\subset \cdots$

根据引理$1$得知这个链条将会断裂.因此必然存在一个$b_m$使得$a = p^mb_m$且$(b_m) = (b_{m+1})$

由于$p$是一个素元,因此$(pb_m)\neq (b_m)$因此造成矛盾.$\square$



由于$n$只由$p$和$a$决定,因此可以令$n = \text{ord}_p a$.



引理$3$ 若$a,b \in R$且$a,b \neq 0$则$\text{ord}_p ab = \text{ord}_p a + \text{ord}_p b$

[证明]

令$\alpha = \text{ord}_p a$且$\beta = \text{ord}_p b$则有$a = p^{\alpha}c$且$b = p^\beta d$且有$p \nmid c$且$p \nmid d$.,

由于$p$是一个素元,因此$p \nmid cd$

$ab = p^{\alpha+\beta}cd$因此有$\text{ord}_p ab = \text{ord}_p a +\text{ord}_p b$.$\square$



现在我们就可以表述并证明这一节的主要定理了.

令$S$为$R$的素元所构成的集合,且具有以下两种特性:

$(\text{a})$ $R$中每一个素元均与$S$中某一个素元相关联.

$(\text{b})$ $S$中任意两个素元都是不相关联的.

为了得到这样一个集合,从每一类关联素元某种选择一个素元(即代表元).这样的选择显然具有很大的随意性.在$\Z$和$k[x]$中有一种比较自然的方式供我们选择.在$\Z$中我们将正素数的集合作为$S$,在$k[x]$中我们将首一不可约多项式构成的集合记为$S$.一般来说,没有哦简单的方法来做出选择,这偶尔会导致复杂的情况(见$\text{Chapter 9}$)



定理$3$ 令$R$为一个$\text{PID}$且$S$为素元所构成的满足前文所述条件的集合,则若$a\in R$且$a \neq 0$则我们可以写成
$$
a = u \prod_p  p^{e(p)}
$$
其中$u$是单位且有$p \in S$.单位$u$和$e(p)$完全由$a$所决定.事实上,$e(p) = \text{ord}_p a$.

[证明]

存在性前文已经证明.

照例引入$\text{ord}_q$函数且$q \in S$

根据引理$3$可以得到
$$
\text{ord}_qa = \text{ord}_q u + \sum_p e(p)\text{ord}_q p
$$
显然有$\text{ord}_q u = 0$.

接下来由于$S$中的素元两两不相关联,因此若$q \neq p$则有$\text{ord}_q p = 0$若$q = p$则$\text{ord}_q p = 1$

因此得到$\text{ord}_q a = e(q)$$\square$

