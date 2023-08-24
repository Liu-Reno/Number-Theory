# Chapter 1 : Unique Factorization

The notion of prime number is fundamental in number theory. The first part of this chapter is devoted to proving that every integer  can be written as a product of primes in an essentially unique way.

After that, we shall prove an analogous theorem in the ring of polynomials over a field.

On a more abstract plane, the general idea of unique factorization is treated for principal ideal domains.

Finally, returning from the abstract to the concrete, the general theory is applied tv two special rings that will be important later in the book.



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

