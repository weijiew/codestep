# 第四章：语法分析

语法分析存在两种类型：**自顶向下**和**自底向上**。

自顶向下是从语法分析树的根节点出发向下分析到叶子节点构建分析树。自底向上的方法则反之，从叶子节点出发向上分析到根节点构建分析树。

从推导和规约两个角度来分析，分别是自顶向下和自底向上两种类型的语法分析。而前者是文法产生规则来实现，后者是从自动机识别语言的角度出发。除此之外前者可以采用递归下降分析来实现，后者则可以使用算符优先分析法来实现，LR(0), SLR(1), LR(1), LALR(1) 。

## 4.1 自顶向下分析

自顶向下分析是从整体到局部。计算机采用**递归下降分析**来实现自顶向下分析。

自顶向下的技术均属于 LL(1) 文法规则的范畴。但对于复杂的文法规则就不适用的，且效率低。

首先从根节点出发，根节点是文法的开始符号，叶子节点是词串（单词）。自顶向下的分析也称为文法的开始符号到词串的分析过程。

但是分析之时总得有个顺序，这个顺序分为左，右两种分析方式。

**最左推导**：总是选择每个句型的最左非终结符进行替换。与之相对应的是**最右规约**：最右规约是最左推导的逆过程。

**最右推导**：总是选择每个句型的最右非终结符进行替换。与之相对应的是**最左规约**：最左规约是最右推导的逆过程。

建议手动画一遍分析过程，加深印象。

写推导过程：

![image-1](https://cdn.jsdelivr.net/gh/weijiew/pic@master/images/image.2vva96vm8j00.png)

![image-2](https://cdn.jsdelivr.net/gh/weijiew/pic@master/images/image.1nwdlaf2hce8.png)

画语法树：

![image-2](https://cdn.jsdelivr.net/gh/weijiew/pic@master/images/image.16bxyfrk00ak.png)

在分析句子之时会先进行预测分析，预测分析成功的话就不要回溯了，而回溯会降低计算机的运行速度。

## 4.2 文法转换

自定向下的分析并不适用于所有的文法，所以对于不适应的文法需要进行转换！

不适用的文法如下：

1. 公共前缀：

当输入存在多个文法可以匹配时会导致回溯的发生。如图，两个 a 的存在导致了回溯的产生。

![image-3](https://cdn.jsdelivr.net/gh/weijiew/pic@master/images/image.3hx3nrl3zhu0.png)

2. 间接左递归

产生式的右部和左部存在同样的部分，迭代的过程会导致死循环。

经过推导间接的产生了这种形式称为**间接左递归**。

![image-4](https://cdn.jsdelivr.net/gh/weijiew/pic@master/images/image.1du863oef9ts.png)

如何消除直接左递归？

首先要明白为什么导致左递归。根源在于文法定义模糊，不够具体。所以增加新的语法变量，细化文法即可解决这个问题。当然因为文法复杂了，所以效率会降低。

直接左递归改成右递归即可。注意边界条件，最好把每一种情况都分析一下。

间接左递归的解法是先将其替换为直接左递归，代换即可，将非终结符替换成终结符即可。

然后再按照直接左递归的计算方法来。

## 4.3 LL(1) 文法

在叙述 LL(1) 文法之前先分析一个问题。当一个文法中某个产生式存在多个候选式时怎么办？也就是存在语法树中存在多条路径选哪个的问题。

$$
A \rightarrow B_1 \\
A \rightarrow B_2 \\ 
A \rightarrow B_3
$$

直观的思考就是一个一个尝试，但是效率显然很低。 

LL(1) 文法就是解决这个问题的。为了解决文法二义性的问题。也就是当文法存在多个候选式时选哪个。该文法实现了不需要回溯也能直接选到最优的候选式。

带有预测分析的文法不需要回溯，LL1 文法就是一种预测分析文法。

LL(1) 文法名字的含义，第一个 L 表示从左向右扫描符号串，第二个 L 表示产生式最左推导，1 代表每次推导时都向前查看一个字符。

需要构造一张 First 集来存，通过该表来消除二义性。除此之外还存在一个问题，一旦存在空集。那么依旧存在二义性。需要构造 Follow 集来解决这个问题。

### 4.3.1 LL(1) 文法严格定义

产生式：$A \rightarrow \alpha | \beta$ 中:

1. 如果 $\alpha$,$\beta$ 均不能推出空集，那么 $First(\alpha) \cap First(\beta) = \epsilon$ 。也就是二者不能存在交集。

2. 如果存在一方可以退出空集，那么至多只能有一个可以推出空集，不能两个都推出空集。

3. 如果 $\beta$ 可以推出空集，那么 $First(\alpha) \cap First(\beta) = \phi$ 。

### 4.3.2 判断 LL(1) 文法

首先要进行改造文法的三部曲。

改造成 LL(1) 文法的步骤，消除二义性，消除左递归，提取左因子。

如果还不行那么说明 LL(1) 文法已经搞不定了，需要添加辅助信息。

要判断一个文法是否是 LL(1) 文法，那么就逐个判断产生式的 First 集是否存在交集。如果存在则说明存在二义性不是 LL(1) 文法，反之则是。

### 4.3.3 First 集和 Follow 集

> 写起来太繁琐了。

这两节能把 First 集和 Follow 集弄明白。

https://www.bilibili.com/video/BV1yk4y197nS?p=11

https://www.bilibili.com/video/BV1yk4y197nS?p=12


## 4.4 递归下降分析

递归下降分析属于 LL(1) 文法，这个分析技术很简单，只需要将文法写清晰就好了。缺点是处理能力有限。