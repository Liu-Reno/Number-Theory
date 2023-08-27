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



## $\S 4 \quad $环$\Z[i]$与$\Z[\omega]$

作为第三章结果的应用,我们将考虑两个例子,它们在后续的$\text{Chapter}$中是有用的.

令$i = \sqrt{-1}$并且考虑由复数所构成的集合$\Z[i] :=\{a+bi:a,b \in \Z\}$.这个集合对于加减法显然是封闭的.此外,若$a+bi,c+di \in \Z[i]$则$(a+bi)(c+di) = (ac-bd)+(ad+bc)i\in\Z[i]$因此$\Z[i]$对于乘法是封闭的.因此$\Z[i]$可以构成一个环.由于$\Z[i]$包含在复数域(无零因子)中,因此它是一个整环.



命题$1.4.1$ $\Z[i]$是一个欧几里得整环.

[证明]

对于$a+bi \in \Z[i]$定义$\lambda(a+bi) = a^2+b^2$.

令$\alpha = a+bi$,$\gamma = c+di$并且假设$\gamma \neq 0$.$\alpha/\gamma = r+si$其中$r$和$s$均为实数(事实上它们都是有理数).

选择整数$m,n \in \Z$使得$|r - m|\leq \frac{1}{2}$且$|s - n|\leq \frac{1}{2}$.

令$\delta = m+ni$.则$\delta \in \Z[i]$.有$\lambda((\alpha/\gamma)- \delta) = (r-m)^2+(s-n)^2 n\leq \frac{1}{4}+\frac{1}{4} = \frac{1}{2}$.

令$\rho = \alpha - \gamma\delta$则$\rho \in \Z[i]$且有$\rho = 0$或$\lambda(\rho) = \lambda(\gamma(\alpha/\gamma - \delta)) = \lambda(\gamma)\lambda(\alpha/\gamma-\delta)\leq \frac{1}{2}\lambda(\gamma) \leq \lambda(\gamma)$

因此得到$\Z[i]$是一个欧几里得整环.$\square$



这个环被称为$\text{ring of Gaussian integers}$即$\text{Gaussian}$整数环,以$\text{C.F. Gauss}$的名字命名,这是因为$\text{Gauss}$首先详细地研究了它的算术性质.

数字$\pm 1$,$\pm i$都是$x^4 = 1$在复数域上的根.考虑等式$x^3 = 1$.由于$x^3 -1 = (x-1)(x^2+x+1)$得到等式的根为$1,\frac{-1\pm \sqrt{-3}}{2}$.令$\omega = \frac{-1+\sqrt{-3}}{2}$得到$\omega^2 = \frac{-1-\sqrt{-3}}{2}$从而可以发现$1+\omega+\omega^2 = 0$.

考虑集合$\Z[\omega] = \{a+b\omega: a,b\in \Z\}$.得到$\Z[\omega]$在加减法下是封闭的.且$(a+b\omega)(c+d\omega) = ac+bd\omega^2+(ad+bc)\omega = ac-bd(1+\omega)+(ad+bc)\omega $$= (ac-bd)+(ad+bc-bd)\omega$.因此$\Z[\omega]$对于乘法封闭.因此$\Z[\omega]$是一个环.由于$\Z[\omega]$在复数域中,因此其是一个整环.

我们注意到$\Z[\omega]$在复共轭下是封闭的.事实上,因为$\overline{\sqrt{-3}}= \overline{\sqrt{3}i} = -\sqrt{3}i = - \sqrt{-3}$我们得到了$\overline{\omega} = \omega^2$.因此若$\alpha = a + b\omega \in \Z[\omega]$则有$\overline{\alpha} = a+b\overline{\omega} = a+b\omega^2 = a-b - b\omega \in \Z[\omega]$.



命题$1.4.2$ $\Z[\omega]$是一个欧几里得整环.

[证明]

令$\alpha = a+b\omega \in \Z[\omega]$且令$\lambda(\alpha) = a^2-ab+b^2$.通过简单的计算可以得知$\lambda(\alpha) = \overline{\alpha}\alpha$.

现在,令$\alpha,\beta \in \Z[\omega]$且假设$\beta \neq 0$于是有$\alpha/\beta = \alpha \overline{\beta}/\beta \overline{\beta} = r+s\omega$其中$r,s$为实数(事实上是有理数).不难发现有$\beta\overline{\beta} = \lambda(\beta)$且$\alpha\overline{\beta} \in \Z[\omega]$.

可以找到两个整数$m,n$使得$|r-m|\leq\frac{1}{2}$且$|s-n|\leq \frac{1}{2}$,接着令$\gamma = m+n\omega$可以得到$\lambda(\alpha/\beta - \gamma) = (r-m)^2-(r-m)(s-n)+(s-n)^2\leq \frac{1}{4}+\frac{1}{4}+\frac{1}{4}<1$.

令$\rho= \alpha-\gamma\beta$得到$\rho = 0$或$\lambda(\rho)= \lambda(\beta(\alpha/\beta - \gamma)) = \lambda(\beta) \lambda(\alpha/\beta - \gamma) <\lambda(\beta)$.

因此得知$\Z[\omega]$是一个欧几里得整环.$\square$



由于$\Z[i]$和$\Z[\omega]$均为欧几里得整环,因此它们都是$\text{PID}$.也就是说唯一因式分解在它们上均成立.为了进一步分析这些环,我们必须研究其上的单位和素元.在$\text{Exercise}$中有一些这种性质的结果.



> ### $\text{\large{N}\small{OTES}}$ (太多了,此处并非重点,暂时不译)
>
> 支持唯一分解定理的环称为唯一因子分解整环$(\text{unique factorization domains(UFD)})$.事实上$\text{Euclid}$已经悄然证明了$\Z$是一个唯一因子分解整环,但是第一个明确而清晰的结果似乎是在$\text{C.F.Gauss}$的$Disquisitiones\, Arithmeticae$中被记载.$\text{Zermelo}$通过归谬法给出了一个巧妙的证明.





## $\text{\large{E}\small{XERCISES}}$

1. 令$a,b$为非负整数.我们可以找到非负整数$q,r$使得$a = qb + r$其中$0 \leq r<b$.证明$(a,b) = (b,r)$

   

   由于$a - qb = r$因此有$r \in (a,b)$,因此任意的$k \in (b,r)$都可以写为$k = s_1b+s_2r = s_1b+s_2(a-qb) = (s_1-s_2q)b +s_2a \in (a,b)$,其中$s_1,s_2\in \Z$且$q$为非负整数.

   因此得知$(b,r)\subset (a,b)$.

   同理证明$(a,b)\subset (b,r)$

   因此有$(a,b) = (b,r)$

   

2. (延续上问) 若$r \neq 0$且我们可以找到$q_1$和$r_1$使得$b = q_1 r+r_1$且$0\leq r_1<r$.证明$(a,b) = (r,r_1)$.这个过程是可以重复的.证明它必然在有限步后停止.证明最后一个非零余数必然等于$(a,b)$.这个过程看起来像
   $$
   a&=& qb + r, &\, &0\leq r<b\\
   b&=& q_1r+r_1 , &\, &0\leq r_1<r\\
   r &=& q_2r_1+r_2 , &\, &0\leq r_2<r_1\\
   \vdots\\
   r_{k-1}&=&q_{k+1}r_k+r_{k+1} , &\,&0 \leq r_{k+1}<r_k\\
   r_k &=& q_{k+2}r_{k+1}
   $$
   则$r_{k+1} = (a,b)$.这个寻找$(a,b)$的过程称为$\text{Euclidean algorithm}$.

   

   首先证明$(a,b) = (r,r_1)$由于$(a,b) = (b,r)$而$(b,r) = (r,r_1)$因此得知$(a,b) = (r,r_1)$.

   接下来证明这个过程在持续有限步后必然停止.

   假设这个过程可以无限重复下去,那么对于任意的正整数$n$都有$0< r_{n+1} < r_{n}$,且$r_{n}$和$r_{n+1}$均为整数.

   由于$b$是一个整数,而$0\leq r_{n+1}<r_n<\cdots <r<b$

   也就是说在经过$b$步后必然有$r_b = q_br_{b-1} = 0$.

   即存在$k$使得$r_{k+2} =0$且$r_{k+1} > 0$.

   因此得到这个步骤必然在有限步后停止.

   接下来由于$(a,b) = (b,r) = (r,r_1) = \cdots = (r_{k-1},r_k) = (r_{k},r_{k+1}) = (r_{k+1},r_{k+2}) = (r_{k+1},0) = r_{k+1}x+0 = (r_{k+1})$因

   因此$r_{k+1} = (a,b)$.

   

3. 计算$(187,221),(6188, 4709),(314, 159)$

   读者自行计算即可

   $221 = 187 + 34$

   $187 = 5 \times 34+ 17$

   $34 = 2 \times 17$

   因此$17 = (187,221)$

   

   $6188 = 4709 + 1479$

   $4709 = 3 \times 1479 + 272$

   $1479 = 5 \times 272 + 119$

   $272 = 2\times 119 + 34$

   $119 = 3 \times 34+ 17$

   $34 = 2\times 17$

   因此$17 = (6188,4709)$

   

   $314 = 159 + 155$

   $159 = 155+4$

   $155 = 38 \times 4 + 3$

   $4 = 3+1$

   $3 = 3 \times 1$

   因此$1 = (314,159)$

   

4. 令$d = (a,b)$使用$\text{Euclidean algorithm}$找到整数$m,n$使得$am+bn = d$.

   

   反过来使用$\text{Euclidean algorithm}$,令最后个非零元$r_{k+1} = d$.

   因此有$r_k = q_{k+2}d$,

   那么$r_{k-1} = q_{k+1}q_{k+2}d + d$

   $r_{k-2} = q_{k}(q_{k+1}q_{k+2}d+d) + q_{k+2}d = q_kq_{k+1}q_{k+2}d+q_kd+q_{k+2}d$

   $r_{k-3} = q_{k-1}(q_kq_{k+1}q_{k+2}d+q_kd+q_{k+1}d)+ q_{k+1}q_{k+2}d+d = (q_{k-1}q_kq_{k+1}q_{k+2}+q_{k-1}q_k+q_{k-1}q_{k+1}+q_{k+1}+q_{k+2}+1)d$

   以此类推可以得知$m$与$n$的值.

   

5. 计算3中给出数的$m,n$

   读者当自强

   自己算吧

   

6. 令$a,b,c\in \Z$.证明等式$ax+by = c$有整数解当且仅当$(a,b)\mid c$.

   

   $(\Leftarrow)$ 若$(a,b)\mid c$则有$c \in (a,b)$因此存在$x,y \in \Z$使得$ax+by = c$.

   $(\Rightarrow)$ 若$ax+by = c$有整数解,即$c \in (a,b)$因此自然有$(a,b)\mid c$

   

7. 令$d = (a,b)$且$a = da'$以及$b = db'$,证明$(a',b') = 1$.

   

   由于$d = (a,b)$因此对于任意的$c\mid a$且$c\mid b$有$c \mid d$.

   若$(a',b')\neq 1$即存在$c$使得$(a',b') =c $则有$c \mid a'$且$c\mid b'$.

   因此得到$a =da' =  dca''$其中$a' = ca''$,$b = db' =  dcb''$.

   由于$d,c$均为整数,有$dc  > d$且$dc \mid a$,$dc \mid b$.因此有$dc \mid d$造成矛盾.

   于是有$c =1$即$(a',b') = 1$.

   

8. 令$x_0,y_0$为$ax+by = c$的解.证明所有这样的解都形如$x = x_0 + t(b/d)$,$y = y_0 - t(a/d)$其中$d  = (a,b)$且$t \in \Z$.

   

   由于$d = (a,b)$因此有$(a/d,b/d) = 1$.

   由于$ax+by = c$有解的条件为$(a,b)\mid c$因此有$c/d$为一个整数

   令$a/d = a',b/d = b',c/d = c'$有$(a',b') = 1$

   且$ax+ by = c$的解即为$a'x+b'y = c'$的解.

   由于$(a',b') =1$因此$\frac{a'}{b'}$必然不为整数.

   由于$y = \frac{c' - a'x}{b'} = \frac{c' - a'x_0+a'x_0 - a'x}{b'} = y_0 +\frac{a'x_0-a'x}{b'} = y_0 + a'\frac{x_0  - x}{b'}$

   得到$x$必然形如$x_0 - tb'$的形式.

   

9. 假设$u,v \in \Z$且$(u,v) =1$.若$u\mid n$且$v\mid n$证明$uv \mid n$.并且证明若$(u,v)\neq 1$则不成立

   

   由于$(u,v) = 1$因此存在$s,r \in \Z$使得$us +vr = 1$.

   因为$u \mid n$因此存在$t$使得$n = ut$,我们需要证明$v\mid t$

   由于$v \mid n = ut$且$v \nmid u$,$(v,u) = 1$因此有$v\mid t$(命题$1.1.1$).

   因此得到$uv \mid n$.

   

   若$(u,v) \neq 1$则无$us + vr = 1$.

   则无$ust + vrt = t$即$v(es+rt) = t$因此无$v \mid t$即无法得到$uv \mid n$

   

10. 假设$(u,v) = 1$则$(u+v,u-v)$要么为$1$要么为$2$

    

    因$(u+v)+(u-v) = 2u$且$(u+v)-(u- v) = 2v$

    因$(u,v) = 1$因此存在$s,r$使得$su + rv = 1$

    若对于$(u+v,u-v) = x_1(u+v)+x_2(u-v) = u(x_1+x_2)+v(x_1-x_2)$不存在$x_1,x_2$使得$x_1+x_2 = s$且$x_1 - x_2 = r$则$(u+v,u-v)\neq 1$

    但是因$2u,2v \in (u+v,u-v)$于是有$2su+2rv = 2 \in (u+v,u-v)$

    因此$(u+v,u-v)$要么为$1$要么为$2$

    

11. 证明$(a,a+k)\mid k$

    

    即证$k \in (a,a+k) = x_1a + x_2(a+k)$其中$x_1,x_2\in \Z$取$x_1 = -1,x_2 = 1$即可

    

12. 假设我们将正多边形复制了几次,并试图在一个公共顶点上均匀地摆放它们.证明唯一可能是$6$个等边三角形,$4$个正方形和$3$个六边形.

    

    问题其实可以转化为问满足内角可以整除$2\pi$的正$n$边形有什么?

    根据正$n$边形的内角和为$(n-2)\pi$得到正$n$边形的每一个内角均为$(n-2)\pi/n$.

    因此问题转化为求能够整除$2$的所有$(n-2)/n = 1 - 2/n$即$\frac{2n}{n-2}$且$n$为整数的情况.

    显然有$n = 3,4,6$满足情况,

    对于其他的$n$,$n$为奇数时,$n-2$为奇数而$2n$为偶数,因此不成立.

    当$n$为大于$6$的偶数时,$n = 2k(k >3)$那么$\frac{2n}{n-2} = \frac{4k}{2(k-1)} = \frac{2k}{k-1}$由于$k-1>2$因此得到$\frac{2n}{n-2}$均不为整数.

    

13. 令$n_1,n_2,\cdots,n_s \in \Z$.定义$n_1,n_2,\cdots,n_s$的最大公因子$d$证明存在整数$m_1,m_2,\cdots,m_s$使得$m_1n_1+m_2n_2+\cdots+m_sn_s = d$.

    

    $(\Leftarrow)$根据题意显然有$d \in (n_1,n_2,\cdots,n_s)$.因此有$(d)\subset (n_1,n_2,\cdots,n_s)$

    接下来证明反向包含也成立.

    任取$c \in (n_1,n_2,\cdots,n_s)$由于$d$是$n_1,n_2,\cdots,n_s$的公因子,必然有$d\mid c$因此$c\in (d)$.

    因此有$(d) = (n_1,n_2,\cdots,n_s)$

    则此时$d$确实为$n_1,n_2,\cdots,n_s$的最大公因子.

    

    $(\Rightarrow)$接下来设$d$为最大公因子.

    那么对于任意的公因子$c$都有$c \mid d$.且对于任意的$n_i$均有$d \mid n_i$.

    由于$d$是最大公因子,因此取$n_i = dn_i'$.

    我们断言$(n_1',n_2',\cdots,n_s')=1$不然存在一个公因子$c$使得$dc > d$且$dc \mid n_i$对于任意的$n_i$均成立.

    因此得到$(n_1',n_2',\cdots,n_s') = (1)$即存在$m_1,m_2,\cdots,m_s$使得$m_1n_1'+m_2n_2'+\cdots+m_sn_s' = 1$因此得到

    $m_1n_1+m_2n_2+\cdots+m_sn_s = d$.

    

    

14. 讨论$a_1x_1+a_2x_2+\cdots+a_rx_r = c$的解的性质.

    

    若$a_1x_1+a_2x_2+\cdots+a_rx_r = c$有解,则$c\in (a_1,a_2,\cdots,a_r)$

    因此得到$(a_1,a_2,\cdots,a_r)\mid c$

    

15. 证明$a \in \Z$是某个整数的平方当且仅当对于所有的素数$p$都有$\text{ord}_p a$是偶数.

    

    若$a$是某个数$b$的平方,则对于$b$进行唯一因式分解得到
    $$
    b = (-1)^{\varepsilon(n)}\prod_p p^{a(p)}
    $$
    因此有$a = b^2$即$\text{ord}_pa = \text{ord}_pb^2 = 2\text{ord}_p b$必然是一个偶数($0$也是偶数)

    

    若$\text{ord}_p a$是一个偶数,则$\frac{1}{2}\text{ord}_p a$是一个整数,因此令$a'(p) = \frac{1}{2}\text{ord}_p a$从而构建一个唯一因式分解
    $$
    b' = \prod_pp^{a'(p)}
    $$
    有$b^2 = a$

    

16. 若$(u,v) = 1$且$uv = a^2$则$u$和$v$均为某个整数的平方.

    

    不难得到$\text{ord}_p uv = \text{ord}_p u + \text{ord}_p v$是偶数.

    因$(u,v) =1$因此对于任意的素数$p$都有若$p \mid u$则$p \nmid v$.

    因此得到$\text{ord}_p u$和$\text{ord}_p v$在同一个$p$下至多只有一个非零.

    因此得到对于每一个$p$都有$\text{ord}_p u$和$\text{ord}_p v$是偶数.

    因此根据15得到$u$和$v$均为某个整数的平方.

    

17. 证明$2$的平方根是无理数,也就是说没有有理数$r = a/b$使得$r^2 = 2$.

    

    由于$2$为素数,因此$2$的唯一因式分解中$\text{ord}_22 = 1$为奇数.

    因此$2$不为整数的平方.

    接下来证明$2$也不为有理数的平方.

    对于有理数$a/b$有$a,b$均为整数,因此我们可以对于$a,b$分别进行唯一因式分解得到:
    $$
    a &=& (-1)^{\varepsilon(a)}\prod_p p^{a(p)}\\
    b &=& (-1)^{\varepsilon(b)}\prod_p p^{b(p)}
    $$
    因此得到了$a/b = (-1)^{\varepsilon(a) - \varepsilon(b)}\prod_p p^{a(p)-b(p)}$

    其中$a(p) - b(p)$也是整数.

    若$r^2 = 2$则$2(a(2) - b(2)) = 1$这与$a(p) - b(p)$为整数这一事实相矛盾,因此$\sqrt{2}$是无理数

    

18. 证明$\sqrt[n]{m}$在$m$不为一个整数的$n$次方时是无理数.

    

    仍然假设$\sqrt[n]{m}$是一个有理数,即存在$a/b$使得$\sqrt[n]{m} =a/b$

    由于$m$不为一个整数的$n$次方,于是存在$p$使得对于$\text{ord}_p m$有$n \nmid \text{ord}_p m$.

    仍然对于$a,b$进行唯一因式分解

    而后得到在素数$p$上有$a(p) - b(p)$是一个整数.

    那么因为$m = (a/b)^n$,则有$n \nmid n(a(p)-b(p))$这与$a(p)-b(p)$为整数相矛盾.

    因此$m$必然是一个无理数

    

19. 定义两个整数$a,b$的最小公倍数为一个整数$m$满足$a\mid m$且$b\mid m$且$m$可以整除$a$和$b$的任意公倍数.证明$m$是存在的,我们将使用$[a,b]$来标记它.

    

    考虑正整数的情况,容易扩充到$\Z$上.

    首先由于$a,b$为整数,因此总是存在一个整数$m$使得$a \mid m$且$b  \mid m$(考虑$ab$)

    接下来证明所有的公倍数中总是存在一个最小公倍数

    我们任取一个公倍数$m_0$,使得存在一个公倍数$m_1 \mid m_0$,

    然后对于$m_1$重复如上操作.

    我们就可以得到一个不断上升的链$(m_0)\subset (m_1)\subset (m_2) \subset \cdots$

    我们证明这条链在有限步之内会断开.

    由于显然有$m_1<m_0$,且$m_1$为一个公倍数

    因此经过$m_0 - \sup\{a,b\}$步后必然有$m_{m_0 - \sup\{a,b\}} = m_{m_0 - \sup\{a,b\}+1}$不然$m_{m_0 - \sup\{a,b\}+1}<\sup \{a,b\}$这与其为一个最小公倍数矛盾.

    因此最小公倍数必然存在

    

20. 证明下述结果:

    $(\text{a}) \text{ord}_p[a,b]= \max(\text{ord}_p a,\text{ord}_p b)$

    $(\text{b})(a,b)[a,b] = ab$

    $(\text{c})(a+b,[a,b]) = (a,b)$

    

    $(\text{a})$

    不难发现$\text{ord}_p[a,b] \geq \max(\text{ord}_p a ,\text{ord}_pb)$这是由$a \mid [a,b]$且$b \mid [a,b]$导出的.

    若有$\text{ord}_p [a,b] >\max (\text{ord}_p a, \text{ord}_p b)$则$\text{ord}_p[a,b] \geq \max (\text{ord}_p a, \text{ord}_p b)+1$.那么我们取$m = (-1)^{\varepsilon}\prod_p p^{\max(\text{ord}_pa,\text{ord}_pb)}$可以得到$a\mid m$且$b \mid m$此外还有$m\mid [a,b]$

    因此$\text{ord}_p[a,b]= \max(\text{ord}_p a,\text{ord}_p b)$

    

    $(\text{b})$

    不难发现$\text{ord}_p (a,b) = \min(\text{ord}_p a ,\text{ord}_p b)$因此可以得到$\text{ord}_p (a,b)[a,b] = \text{ord}_p a + \text{ord}_p b = \text{ord}_p ab$.由于$(a,b)$的符号默认为正,因此可以得到$[a,b]$的正负号与$ab$相同.

    因此根据唯一因式分解定理得到$(a,b)[a,b] = ab$

    

    $(\text{c})$

    首先由于$(a,b)\mid a$且$(a,b)\mid b$因此有$(a,b)\mid (a+b)$

    因此可以得到$(a,b)\mid (a+b,[a,b])$

    剩下内容结合21使用唯一因式分解进行证明就行了

    

21. 证明$\text{ord}_p (a+b) \geq \min (\text{ord}_p a,\text{ord}_p b)$当$\text{ord}_p a \neq \text{ord}_p b$时等式成立

    

    使用唯一因数分解可以轻松得到不等式

    而$\text{ord}_2 a = \text{ord}_2 b\neq 0$时$\text{ord}_2(a+b)=1+\text{ord}_pa $

    

22. 若我们考虑环$k[x]$而不是环$\Z$时,前面几乎所有的练习仍然有效.事实上,在大多是情况下,我们考虑任何的欧几里得整环.本题的目的是让你相信这个事实,不过简单起见,我们将继续使用$\Z$.

    

23. 假设$a^2+b^2 = c^2$且$a,b,c \in \Z$.举个例子,$3^2+4^2 = 5^2$以及$5^2+12^2=13^2$.假设$(a,b) = (b,c) = (c,a) =1$.证明存在整数$u,v$使得$c-b =  2u^2$且$c+b = 2v^2$且有$(u,v) = 1$(不失一般性,可以假设$b,c$为奇数且$a$为偶数)因此$a = 2uv,b = v^2-u^2,c = v^2+u^2$.反过来说明若$u,v$已知,那么由这些公式所给出的三个数$a,b,c$满足$a^2+b^2 = c^2$.

    

    先证明反向

    若存在$u,v$满足上式则有$a^2+b^2 = 4u^2v^2+v^4-2v^2u^2+u^4= (u^2+v^2)^2$.于是确实有$c = v^2+u^2$.

    由于$(u,v) = 1$因此有$[u,v] = uv$.有$(2uv,u^2-v^2) = (2uv,u^2+v^2) =(u^2-v^2,u^2+v^2) = 1$.

    再证明正向

    由于$a^2+b^2 = c^2$于是有$a^2 = (c-b)(c+b)$由于$(b,c) = 1$有$(b-c,b+c) = 1$或$2$.由于我们假设了$b,c$均为奇数于是有$(b-c,b+c) = 2$,且有$2 \mid a$

    因此得到$\frac{a}{2}$,$\frac{c-b}{2}$和$\frac{c+b}{2}$是一个整数.

    因此可以得到$(\frac{a}{2})^2 = \frac{c-b}{2}\frac{c+b}{2}$且$(\frac{b-c}{2},\frac{b+c}{2}) = 1$.

    因此根据16得知存在$u,v$使得$u^2 = \frac{c-b}{2},v^2 = \frac{b+c}{2}$.

    由于$(u^2,v^2) =1$因此可以得到$(u,v) = 1$.

    

24. 证明恒等式

    $(\text{a}) x^n -y^n = (x-y)(x^{n-1}+x^{n-2}y+\cdots + y^{n-1})$

    $(\text{b})$若$n$是奇数,则$x^n+y^n = (x+y)(x^{n-1}-x^{n-2}y+x^{n-3}y^2-\cdots+y^{n-1})$

    

    两问均可在等式两侧同时除以$y^n$转化为等比数列求和得到,读者自行证明即可

    

25. 若$a^n-1$是一个素数,证明$a = 2$且$n$是一个素数.形如$2^p - 1$的素数称为$\text{Mersenne}$素数.比如说$2^3 - 1 = 7$以及$2^{5} - 1 = 31$现在暂且不知晓$\text{Mersenne}$素数是否是无穷多个的.

    

    $a^n - 1 = (a-1)(a^{n-1}+a^{n-2}+\cdots + 1)$为一个素数,所以有$a = 2$,

    而若$n$不为素数,则存在$p,q$使得$n = pq$,而$2^n - 1 = 2^{pq} -1 = (2^p)^q -1 = (2^p -1)(2^{p(q-1)}+\cdots +1)$不为素数

    

26. 若$a^n + 1$是一个素数,证明$a$是偶数且$n$是$2$的幂.形如$2^{2^t}+1$的素数称为$\text{Fermat}$素数.举个例子$2^{2^1}+1 = 5$以及$2^{2^2}+1 = 17$现在暂且不知晓$\text{Fermat}$素数是否是无穷多个的.

    

    若$n$为奇数则$a^n+1$不为素数,因此$n$必然为偶数.

    而奇数的幂为奇数,于是$a$必然为偶数.

    若$n$不为$2$的幂,且$n$为偶数,则有$n = 2^mk$其中$k$为奇数,$m$为一个整数.

    因此我们可以得到$x^n+1 = x^{2^mk}+1 = (x^{2m})^k+1$就可以按照24进行分解了

    

27. 证明对于所有的奇数$n$有$8 \mid n^2-1$若$3 \nmid n$则$6 \mid n^2 -1$

    

    $n = 1$时有$n^2 -1  = 0$满足条件.

    对于$n \geq 3$时$n = 2k + 1,k\geq1$则有$n^2 -1 = (n-1)(n+1) = (2k+2)2k = 4(k+1)k$由于$k+1$和$k$中必然有一个是偶数

    因此得到$8 \mid n^2-1$

    

    若$3 \nmid n$则$n = 1$时有$6\mid 0$

    由于$3 \nmid n$因此有$n \neq 3k$即$n^2 -1 \neq (3k-1)(3k+1)$.

    因此有$6 \mid n^2 -1$

    

28. 证明对于所有的$n$有$30 \mid n^5 - n$且$42 \mid n^7 - n$

    

    $n^5 - n = n(n^4 - 1) = n(n^2+1)(n+1)(n-1)$而$30 = 6\times 5 = 2\times 3 \times 5 = (2-1)2(2+1)(2^2+1)$

    因此得到$30 \mid n^5 - n$

    同理证明$42$的情况

    

29. 假设$a,b,c,d \subset \Z$且$(a,b)= (c,d) = 1$若$(a/b)+(c/d)$等于一个整数证明$b = \pm d$

    

    由于$(a/b) + (c/d)$为一个整数,由于$(a,b) = (c,d) = 1$因此$a/b$和$c/d$均为既约分数,因此自然有$b = \pm d$

    

30. 证明$\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n}$不是一个整数

    

    由于$(1,i) = 1,i\in \Z_{\geq 1}$因此根据$29$得知其不为一个整数

    

31. 证明在$\Z[i]$中有$2$被$(1+i)^2$整除.

    

    $(1+i)^2 = 2i$有$2 = 2i \times (-i)$因此$(1+i)^2 \mid 2$

    

32. 对于$\alpha = a+bi \in\Z[i]$我们定义$\lambda(\alpha) = a^2 + b^2$根据$\lambda$的性质证明$(a^2+b^2)(c^2+d^2) = (ac-bd)^2+(ad-bc)^2$

    

    由于$(a+bi)(c+di) = (ac-bd)+(ad-bc)i$因此$(a^2+b^2)(c^2+d^2) = \lambda(a+bi)\lambda(c+di) = \lambda((a+bi)(c+di)) = (ac-bd)^2 + (ad - bc)^2$

    

33. 证明$\alpha \in \Z[i]$是一个单位当且仅当$\lambda(\alpha) = 1$.这诱导了$1,-1,i,-i$是$\Z[i]$上的单位.

    

    若$\alpha$是一个单位,则$(\alpha) = \Z[i]$,也就是说有$\alpha \mid 1$,即$1 = t\alpha +0$由于$1 \mid \alpha$于是得到$t$也为一个单位,因此得到$\lambda(t)\lambda(\alpha) = \lambda(t\alpha) = \lambda(1) = 1$.由于$\lambda$的特性可知$\lambda(t) = \lambda(1) = \lambda(\alpha) = 1$

    

34. 证明$3$可以被$\Z[\omega]$的$(1-\omega)^2$整除.

    

    $(1-\omega)^2 = 1 - 2\omega + \omega^2 = -3\omega$因此得到$3 = (1-\omega)^2 (-3 \omega^2) = (1-\omega)^2(-3(1-\omega))$因此$(1-\omega)^2 \mid 3$.

    

35. 类似于33读者自证即可

    

36. 定义$\Z[\sqrt{-2}]$是所有形如$a+b\sqrt{-2}$的复数所构成的集合,其中$a,b \in \Z$.证明$\Z[\sqrt{-2}]$构成一个环.定义$\lambda(\alpha) = a^2+2b^2$其中$\alpha = a+b\sqrt{-2}$.使用$\lambda$证明$\Z[\sqrt{-2}]$是一个欧几里得整环

    

    不难验证$\Z[\sqrt{-2}]$对于加减法封闭.对于乘法有$(a+b\sqrt{-2})(c+d\sqrt{-2}) = (a-2bd)+(bc+ad)\sqrt{-2}\in \Z[\sqrt{-2}]$因此$\Z[\sqrt{-2}]$确实构成环.

    接下来验证构成欧几里得整环.

    考虑$\alpha = a+ b\sqrt{-2}$且$\beta = c + d\sqrt{-2}\neq 0$得到$\delta = \alpha/\beta = r+s\sqrt{-2}$.

    其中$r,s$均为实数

    我们可以得到两个整数$m,n$使得$|r-m|<1/2$且$|s-n|<1/2$

    令$\rho = \alpha - \beta \delta$得到$\rho = 0$或$\lambda(\rho) = \lambda(\beta)\lambda(\alpha/\beta-\delta) = \lambda(\beta)\lambda(m-r+(n-s)\sqrt{-2}) <\lambda(\beta)(1/4+1/2)<\lambda(\beta)$

    因此确实构成一个欧几里得整环

    

37. 证明$\Z[\sqrt{-2}]$的单位只有$1,-1$

    

    $\lambda(\alpha) = 1$

    

38. 假设$\pi \in \Z[i]$且$\lambda(\pi) = p$为$\Z$上的一个素数.证明$\pi$是$\Z[i]$上的一个素元.且证明相同的结果在$\Z[\omega]$和$\Z[\sqrt{-2}]$上成立

    

    由于$\lambda(\pi) = p$因此对于$\alpha = a+bi$,$\beta = c+di$有$p\mid \lambda (\alpha\beta) \Leftrightarrow p \mid \lambda (\alpha)\lor p \mid \lambda(\beta)$

    因此我们有$\lambda(\pi)\mid \lambda(\alpha \beta) \Leftrightarrow \lambda(\pi)\mid \lambda(\alpha) \lor \lambda(\pi)\mid \lambda(\beta)$

    得到$\alpha\beta = k_1\pi + 0 \Leftrightarrow \alpha = k\pi + 0 \lor \beta = t \pi +0$

    因此得到$\pi$是$\Z[i]$上的一个素元

    

39. 证明在任意整环上有素元是不可约元.

    

    若整环$R$上的素元$p$可约,则有$p = qr$其中$q,r \in R$且不为单位

    于是有$p \mid qr$因此$p \mid q$或$p \mid r$又因为$q \mid p$且$r \mid p$于是得到其中必有一个单位元.与假设矛盾.

