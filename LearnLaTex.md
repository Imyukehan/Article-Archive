

# $ \LaTeX{} $历史

$\LaTeX{}$（/ˈlɑːtɛx/，常被读作/ˈlɑːtɛk/或/ˈleɪtɛk/），文字形式写作LaTeX，是一种基于TEX的排版系统，由美国计算机科学家莱斯利·兰伯特在20世纪80年代初期开发，利用这种格式，即使用户没有排版和程序设计的知识也可以充分发挥由TEX所提供的强大功能，能在几天，甚至几小时内生成很多具有书籍质量的印刷品。对于生成复杂表格和数学公式，这一点表现得尤为突出。因此它非常适用于生成高印刷质量的科技和数学类文档。这个系统同样适用于生成从简单的信件到完整书籍的所有其他种类的文档。

$ \LaTeX{} $使用TEX作为它的格式化引擎。

# 控制序列

所谓控制序列，是以反斜杠`\`开头，以第一个**空格或非字母** 的字符结束的一串文字，他们并不被输出，但是他们会影响输出文档的效果。
**TeX 对控制序列的大小写是敏感的**
> 部分控制序列还有被方括号`[]`包括的可选参数。
> 所谓文档类，即是 TeX 系统预设的（或是用户自定的）一些格式的集合。不同的文档类在输出效果上会有差别。

# Markdown中插入$ \LaTeX{}$公式

## 1．如何插入公式

的数学公式有两种：行中公式和独立公式。行中公式放在文中与其它文字混编，独立公式单独成行。

行中公式可以用如下方法表示：

```
$ 数学公式 $

```

独立公式可以用如下方法表示：

```
$$ 数学公式 $$

```

自动编号的公式可以用如下方法表示： 

若需要手动编号，参见大括号和行标的使用。 

```
\begin{equation}
数学公式
\end{equation}

```

例子：

J_\alpha(x) = \sum_{m=0}^\infty \frac{(-1)^m}{m! \Gamma (m + \alpha + 1)} {\left({ \frac{x}{2} }\right)}^{2m + \alpha}

显示： 
$$
J\alpha(x) = \sum{m=0}^\infty \frac{(-1)^m}{m! \Gamma (m + \alpha + 1)} {\left({ \frac{x}{2} }\right)}^{2m + \alpha}
$$
例子：

1. `\begin{equation}`
2. `E=mc^2`
3. `\end{equation}`

显示： 

$$
\begin{equation}E=mc^2\end{equation}
$$

## 2．如何输入上下标

^表示上标, _表示下标。如果上下标的内容多于一个字符，要用{}把这些内容括起来当成一个整体。上下标是可以嵌套的，也可以同时使用。

例子：x^{y^z}=(1+{\rm e}^x)^{-2xy^w}

显示： $ x^{y^z}=(1+{\rm e}^x)^{-2xy^w} $

另外，如果要在左右两边都有上下标，可以用\sideset命令。

例子：\sideset{^1_2}{^3_4}\bigotimes

显示： $ \sideset{^1_2}{^3_4}\bigotimes $

## 3．如何输入括号和分隔符

()、[]和|表示自己，{}表示{}。当要显示大号的括号或分隔符时，要用 `\left` 和 `\right` 命令。 

例子：f(x,y,z) = 3y^2z \left( 3+\frac{7x+5}{1+y^2} \right)

显示：$ f(x,y,z) = 3y^2z \left( 3+\frac{7x+5}{1+y^2} \right) $

有时候要用\left.或\right.进行匹配而不显示本身。

例子：\left. \frac{{\rm d}u}{{\rm d}x} \right| _{x=0}

显示： $ \left. \frac{{\rm d}u}{{\rm d}x} \right| _{x=0} $

## 4．如何输入分数

例子：\frac{1}{3} 或 1 \over 3

显示： $ \frac{1}{3} $

## 5．如何输入开方

例子：\sqrt{2} 和 \sqrt[n]{3}

显示： $ \sqrt{2} $

## 6．如何输入省略号

数学公式中常见的省略号有两种，\ldots表示与文本底线对齐的省略号，\cdots表示与文本中线对齐的省略号。

例子：f(x_1,x_2,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2

显示： 

$$
f(x1,x2,\ldots,x_n) = x1^2 + x2^2 + \cdots + x_n^2
$$

## 7．如何输入矢量

例子：\vec{a} \cdot \vec{b}=0

显示：$ \vec{a} \cdot \vec{b}=0 $

例子：\overrightarrow{xy} \overleftrightarrow{xy}

显示： $ \overrightarrow{xy} \overleftrightarrow{xy} $

## 8．如何输入积分

例子：\int_0^1 x^2 {\rm d}x

显示： $ \int_0^1 x^2 {\rm d}x $

## 9．如何输入极限运算

例子：\lim_{n \rightarrow +\infty} \frac{1}{n(n+1)}

显示： $ \lim_{n \rightarrow +\infty} \frac{1}{n(n+1)} $

## 10．如何输入累加、累乘运算

例子：\sum_{i=0}^n \frac{1}{i^2} 和 \prod_{i=0}^n \frac{1}{i^2}

显示： 

$$
\sum{i=0}^n \frac{1}{i^2}
$$


和

$$
\prod{i=0}^n \frac{1}{i^2}
$$


## 11．如何输入希腊字母

例子：

\alpha A \beta B \gamma \Gamma \delta \Delta \epsilon E

\varepsilon \zeta Z \eta H \theta \Theta \vartheta

\iota I \kappa K \lambda \Lambda \mu M \nu N

\xi \Xi o O \pi \Pi \varpi \rho P

\varrho \sigma \Sigma \varsigma \tau T \upsilon \Upsilon

\phi \Phi \varphi \chi X \psi \Psi \omega \Omega

显示： 

$$
\alpha A \beta B \gamma \Gamma \delta \Delta \epsilon E

\varepsilon \zeta Z \eta H \theta \Theta \vartheta

\iota I \kappa K \lambda \Lambda \mu M \nu N

\xi \Xi o O \pi \Pi \varpi \rho P

\varrho \sigma \Sigma \varsigma \tau T \upsilon \Upsilon

\phi \Phi \varphi \chi X \psi \Psi \omega \Omega
$$


## 12．如何输入其它特殊字符

若找不到需要的符号，使用来画出想要的符号。 

![img](http://img0.tuicool.com/3Mfqyu2.png!web)

### (1)．关系运算符

±：\pm

×：\times

÷：\div

∣：\mid

∤：\nmid

⋅：\cdot

∘：\circ

∗：\ast

⨀：\bigodot

⨂：\bigotimes

⨁：\bigoplus

≤：\leq

≥：\geq

≠：\neq

≈：\approx

≡：\equiv

∑：\sum

∏：\prod

∐：\coprod

### (2)．集合运算符

∅：\emptyset

∈：\in

∉：\notin

⊂：\subset

⊃：\supset

⊆：\subseteq

⊇：\supseteq

⋂：\bigcap

⋃：\bigcup

⋁：\bigvee

⋀：\bigwedge

⨄：\biguplus

⨆：\bigsqcup

### (3)．对数运算符

log：\log

lg：\lg

ln：\ln

### (4)．三角运算符

30∘：30^\circ 

30 ∘

sin：\sin

sin x

cos：\cos

tan：\tan

cot：\cot

sec：\sec

csc：\csc

⊥：\bot

平 面 A ⊥ 平 面 B

∠：\angle

∠ A = 30 ∘

### (5)．微积分运算符

′：\prime 

′

∫：\int∬：\iint∭：\iiint∬∬：\iiiint∮：\oint 

lim：\lim

lim

∞：\infty

∞

∇：\nabla

∇

### (6)．逻辑运算符

∵：\because 

∵

∴：\therefore

∴

∀：\forall

∀

∃：\exists

∃

≠：\not=

≠

≯：\not>

≯

⊄：\not\subset

⊄

### (7)．戴帽符号

y^：\hat{y} 

^

xy^:\widehat{xy}

x ˆ

yˇ：\check{y}

ˇ

y˘：\breve{y}

˘

### (8)．连线符号

a+b+c+d：\overline{a+b+c+d} 

a + b + c +

a+b+c+d：\underline{a+b+c+d}

a + b + c +

a+b+c1.0+d2.0：\overbrace{a+\underbrace{b+c}_{1.0}+d}^{2.0}

a + b + c 1.0 + 2.0

### (9)．箭头符号

↑：\uparrow

↓：\downarrow

⇑：\Uparrow

⇓：\Downarrow

→：\rightarrow

←：\leftarrow

⇒：\Rightarrow

⇐：\Leftarrow

⟶：\longrightarrow

⟵：\longleftarrow

⟹：\Longrightarrow

⟸：\Longleftarrow

## 13．如何进行字体转换

要对公式的某一部分字符进行字体转换，可以用{\rm 需转换的部分字符}命令，其中\rm可以参照下表选择合适的字体。一般情况下，公式默认为意大利体 a m p l e

。

| 项目   | 说明   | 示例    | 项目    | 说明   | 示例   |
| ---- | ---- | ----- | ----- | ---- | ---- |
| \rm  | 罗马体  | \it   | 意大利体  |      |      |
| \bf  | 粗体   | \cal  | 花体    |      |      |
| \Bbb | 黑板粗体 | \sf   | 等线体   |      |      |
| \mit | 数学斜体 | \tt   | 打字机体  |      |      |
| \scr | 手写体  | \frak | 旧德式字体 |      |      |

## 14．大括号和行标的使用

使用 `\left` 和 `\right` 来创建自动匹配高度的 (圆括号)，[方括号] 和 {花括号} 。 

在每个公式末尾前使用 `\tag{行标}` 来实现行标。 

例子：

1. `$$`
2. `f\left(`
3. `\left[`
4. `\frac{`
5. ` 1+\left\{x,y\right\}`
6. ` }{`
7. `\left(`
8. `\frac{x}{y}+\frac{y}{x}`
9. `\right)`
10. `\left(u+1\right)`
11. ` }+a`
12. `\right]^{3/2}`
13. `\right)`
14. `\tag{行标}`
15. `$$`

显示： 

1 + { x , } ( + ) ( u + 1 ) + a 3 / 2 ( 行 标 ) 

## 15．其它命令

### (1)．定义新的符号 \operatorname

例子：

1. `$$ \operatorname{Sample} A $$`

显示： 

Sample A

### (2)．添加注释文字 \text

例子：

1. `$$ f(n)= \begin{cases} n/2, & \text {if $n$ is even} \\ 3n+1, & \text{if $n$ is odd} \end{cases} $$`

显示： 

( n ) = { n / 2 , 3 n + 1 , if  n  is even if  n  is odd

## 二、矩阵使用参考

## 1．如何输入无框矩阵

在开头使用 `begin{matrix}` ，在结尾使用 `end{matrix}` ，在中间插入矩阵元素，每个元素之间插入 `&` ，并在每行结尾处使用 `\\` 。 

例子：

1. `$$`
2. `\begin{matrix}`
3. ` 1 & x & x^2 \\`
4. ` 1 & y & y^2 \\`
5. ` 1 & z & z^2 \\`
6. `\end{matrix}`
7. `$$`

显示： 

1 1 1 x 2 2 2

## 2．如何输入边框矩阵

在开头将 `matrix` 替换为 `pmatrix` `bmatrix` `Bmatrix` `vmatrix` `Vmatrix` 。 

例子：

1. `$ \begin{matrix} 1 & 2 \\ 3 & 4 \\ \end{matrix} $`
2. `$ \begin{pmatrix} 1 & 2 \\ 3 & 4 \\ \end{pmatrix} $`
3. `$ \begin{bmatrix} 1 & 2 \\ 3 & 4 \\ \end{bmatrix} $`
4. `$ \begin{Bmatrix} 1 & 2 \\ 3 & 4 \\ \end{Bmatrix} $`
5. `$ \begin{vmatrix} 1 & 2 \\ 3 & 4 \\ \end{vmatrix} $`
6. `$ \begin{Vmatrix} 1 & 2 \\ 3 & 4 \\ \end{Vmatrix} $`

显示：

| matrix  | pmatrix | bmatrix | Bmatrix | vmatrix | Vmatrix |
| ------- | ------- | ------- | ------- | ------- | ------- |
| 1 3 2 4 |         |         |         |         |         |

## 3．如何输入带省略符号的矩阵

使用 `\cdots` ⋯

, 

```
\ddots
```

 

⋱ 

, 

```
\vdots
```

⋮

来输入省略符号。

例子：

1. `$$`
2. `\begin{pmatrix}`
3. ` 1 & a_1 & a_1^2 & \cdots & a_1^n \\`
4. ` 1 & a_2 & a_2^2 & \cdots & a_2^n \\`
5. `\vdots & \vdots & \vdots & \ddots & \vdots \\`
6. ` 1 & a_m & a_m^2 & \cdots & a_m^n \\`
7. `\end{pmatrix}`
8. `$$`

显示： 

1 1 ⋮ 1 a 1 a 2 ⋮ a m a 2 1 a 2 2 ⋮ a 2 m ⋯ ⋯ ⋱ ⋯ a n 1 a n 2 ⋮ a n m

## 4．如何输入带分割符号的矩阵

详见"数组使用参考"。 

例子：

1. `$$ \left[`
2. `\begin{array}{cc|c}`
3. ` 1&2&3\\`
4. ` 4&5&6`
5. `\end{array}`
6. `\right] $$`

显示： 

[ 1 4 2 5 3 6 ]

其中 `cc|c` 代表在一个三列矩阵中的第二和第三列之间插入分割线。 

## 5．如何输入行中矩阵

若想在一行内显示矩阵，

使用 `\bigl(\begin{smallmatrix} ... \end{smallmatrix}\bigr)` 。 

例子：

1. `这是一个行中矩阵的示例 $\bigl( \begin{smallmatrix} a & b \\ c & d \end{smallmatrix} \bigr)$ 。`

显示：

这是一个行中矩阵的示例 ( a c b )

。

## 三、方程式序列使用参考

## 1．如何输入一个方程式序列

人们经常想要一列整齐且居中的方程式序列。使用 `\begin{align}…\end{align}` 来创造一列方程式，其中在每行结尾处使用 `\\` 。 

例子：

1. `\begin{align}`
2. `\sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\`
3. ` & = \sqrt{\frac{73^2}{12^2}\cdot\frac{73^2-1}{73^2}} \\ `
4. ` & = \sqrt{\frac{73^2}{12^2}}\sqrt{\frac{73^2-1}{73^2}} \\`
5. ` & = \frac{73}{12}\sqrt{1 - \frac{1}{73^2}} \\ `
6. ` & \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)`
7. `\end{align}`

显示： 

= 73 2 − 1 12 2 √ = 73 2 12 2 ⋅ 73 2 − 1 73 2 √ = 73 2 12 2 √ 73 2 − 1 73 2 √ = 73 12 1 − 1 73 2 √ ≈ 73 12 ( 1 − 1 2 ⋅ 73 2 ) (2) (3) (4) (5) (6)

方程式序列中无需再次声明公式符号 `\$` 或 `\$$` 。 

## 四、条件表达式使用参考

## 1．如何输入一个条件表达式

使用 `begin{cases}` 来创造一组条件表达式，在每一行条件中插入 `&` 来指定需要对齐的内容，并在每一行结尾处使用 `\\` ，以 `end{cases}` 结束。 

条件表达式需要指定 `$$` 或 `$` 。 

例子：

1. `$$`
2. `f(n) =`
3. `\begin{cases}`
4. `n/2, & \text{if $n$ is even} \\`
5. ` 3n+1, & \text{if $n$ is odd}`
6. `\end{cases}`
7. `$$`

显示： 

( n ) = { n / 2 , 3 n + 1 , if  n  is even if  n  is odd

## 2．如何输入一个左侧对齐的条件表达式

若想让文字在 **左侧对齐显示** ，则有如下方式： 

例子：

1. `$$`
2. `\left.`
3. `\begin{array}{l}`
4. `\text{if $n$ is even:}&n/2\\`
5. `\text{if $n$ is odd:}&3n+1`
6. `\end{array}`
7. `\right\}`
8. ` =f(n)`
9. `$$`

显示： 

if  n  is even: if  n  is odd: n / 2 3 n + 1 } = ( n )

## 3．如何使条件表达式适配行高

在一些情况下，条件表达式中某些行的行高为非标准高度，此时使用 `\\[2ex]` 语句代替该行末尾的 `\\` 来让编辑器适配。 

例子：

1. `f(n) =`
2. `\begin{cases}`
3. `\frac{n}{2}, & \text{if $n$ is even} \\`
4. `3n+1, & \text{if $n$ is odd}`
5. `\end{cases}`


1. `f(n) =`
2. `\begin{cases}`
3. `\frac{n}{2}, & \text{if $n$ is even} \\[2ex]`
4. `3n+1, & \text{if $n$ is odd}`
5. `\end{cases}`

显示：

| 不适配[2ex]                                 |
| ---------------------------------------- |
| ( n ) = { n 2 , 3 n + 1 , if  n  is even if  n  is odd |

| 适配[2ex]                                  |
| ---------------------------------------- |
| ( n ) = n 2 , 3 n + 1 , if  n  is even if  n  is odd |

一个 `[ex]` 指一个 "X-Height"，即x字母高度。可以根据情况指定多个 `[ex]` ，如 `[3ex]` `[4ex]` 等。 

## 五、数组与表格使用参考

## 1．如何输入一个数组或表格

通常，一个格式化后的表格比单纯的文字或排版后的文字更具有可读性。数组和表格均以 `begin{array}` 开头，并在其后定义列数及每一列的文本对齐属性， `c` `l` `r` 分别代表居中、左对齐及右对齐。若需要插入垂直分割线，在定义式中插入 `|` ，若要插入水平分割线，在下一行输入前插入 `\hline` 。与矩阵相似，每行元素间均须要插入 `&` ，每行元素以 `\\` 结尾，最后以 `end{array}` 结束数组。 

例子：

1. `\begin{array}{c|lcr}`
2. `n & \text{左对齐} & \text{居中对齐} & \text{右对齐} \\`
3. `\hline`
4. `1 & 0.24 & 1 & 125 \\`
5. `2 & -1 & 189 & -8 \\`
6. `3 & -20 & 2000 & 1+10i`
7. `\end{array}`

显示： 

n 1 2 3 左 对 齐 0.24 − 1 − 20 居 中 对 齐 1 189 2000 右 对 齐 125 − 8 1 + 10 i

## 2．如何输入一个嵌套的数组或表格

多个数组/表格可 **互相嵌套** 并组成一组数组/一组表格。 

使用嵌套前必须声明 `$$` 符号。 

例子：

1. `$$`
2. `% outer vertical array of arrays 外层垂直表格`
3. `\begin{array}{c}`
4. ` % inner horizontal array of arrays 内层水平表格`
5. `\begin{array}{cc}`
6. ` % inner array of minimum values 内层"最小值"数组`
7. `\begin{array}{c|cccc}`
8. `\text{min} & 0 & 1 & 2 & 3\\`
9. `\hline`
10. ` 0 & 0 & 0 & 0 & 0\\`
11. ` 1 & 0 & 1 & 1 & 1\\`
12. ` 2 & 0 & 1 & 2 & 2\\`
13. ` 3 & 0 & 1 & 2 & 3`
14. `\end{array}`
15. ` &`
16. ` % inner array of maximum values 内层"最大值"数组`
17. `\begin{array}{c|cccc}`
18. `\text{max}&0&1&2&3\\`
19. `\hline`
20. ` 0 & 0 & 1 & 2 & 3\\`
21. ` 1 & 1 & 1 & 2 & 3\\`
22. ` 2 & 2 & 2 & 2 & 3\\`
23. ` 3 & 3 & 3 & 3 & 3`
24. `\end{array}`
25. `\end{array}`
26. ` % 内层第一行表格组结束`
27. `\\`
28. ` % inner array of delta values 内层第二行Delta值数组`
29. `\begin{array}{c|cccc}`
30. `\Delta&0&1&2&3\\`
31. `\hline`
32. ` 0 & 0 & 1 & 2 & 3\\`
33. ` 1 & 1 & 0 & 1 & 2\\`
34. ` 2 & 2 & 1 & 0 & 1\\`
35. ` 3 & 3 & 2 & 1 & 0`
36. `\end{array}`
37. ` % 内层第二行表格组结束`
38. `\end{array}`
39. `$$`

显示： 

min 0 1 2 3 0 0 0 0 0 1 0 1 1 1 2 0 1 2 2 3 0 1 2 3 max 0 1 2 3 0 0 1 2 3 1 1 1 2 3 2 2 2 2 3 3 3 3 3 3 Δ 0 1 2 3 0 0 1 2 3 1 1 0 1 2 2 2 1 0 1 3 3 2 1 0

## 3．如何输入一个方程组

使用 `\begin{array}…\end{array}` 和 `\left\{…\right.` 来创建一个方程组。 

例子：

1. `$$`
2. `\left\{ `
3. `\begin{array}{c}`
4. `a_1x+b_1y+c_1z=d_1 \\ `
5. `a_2x+b_2y+c_2z=d_2 \\ `
6. `a_3x+b_3y+c_3z=d_3`
7. `\end{array}`
8. `\right.`
9. `$$`

显示： 

$$
\left\{
  \begin{array}{c}
  a_1x+b_1y+c_1z=d_1 \\
  a_2x+b_2y+c_2z=d_2 \\
  a_3x+b_3y+c_3z=d_3
  \end{array}
\right.
$$
或者使用条件表达式组 `\begin{cases}…\end{cases}` 来实现相同效果： 

例子：

1. `$$\begin{cases}`
2. `a_1x+b_1y+c_1z=d_1 \\ `
3. `a_2x+b_2y+c_2z=d_2 \\ `
4. `a_3x+b_3y+c_3z=d_3`
5. `\end{cases}`
6. `$$`

显示： 

$$
\begin{cases}
  a_1x+b_1y+c_1z=d_1 \\
  a_2x+b_2y+c_2z=d_2 \\
  a_3x+b_3y+c_3z=d_3
  \end{cases}
$$

## 六、连分数使用参考

就像输入分式时使用 `\frac` 一样，使用 `\cfrac` 来创建一个连分数。 

例子：

1. `$$`
2. `x = a_0 + \cfrac{1^2}{a_1`
3. ` + \cfrac{2^2}{a_2`
4. ` + \cfrac{3^2}{a_3 + \cfrac{4^4}{a_4 + \cdots}}}}`
5. `$$`

显示： 

$$
x = a_0 + \cfrac{1^2}{a_1
+ \cfrac{2^2}{a_2
+ \cfrac{3^2}{a_3 + \cfrac{4^4}{a_4 + \cdots}}}}
$$
不要使用普通的 `\frac` 或 `\over` 来创建，否则会看起来 **很恶心** 。 

例子：

1. `$$`
2. `x = a_0 + \frac{1^2}{a_1`
3. ` + \frac{2^2}{a_2`
4. ` + \frac{3^2}{a_3 + \frac{4^4}{a_4 + \cdots}}}}`
5. `$$`

显示： 

$$
x = a_0 + \frac{1^2}{a_1
+ \frac{2^2}{a_2
+ \frac{3^2}{a_3 + \frac{4^4}{a_4 + \cdots}}}}
$$
当然，你可以使用 `\frac` 来表达连分数的 **紧缩记法** 。 

例子：

1. `$$`
2. `x = a_0 + \frac{1^2}{a_1+}`
3. `\frac{2^2}{a_2+}`
4. `\frac{3^2}{a_3 +} \frac{4^4}{a_4 +} \cdots`
5. `$$`

显示： 

$$
x = a_0 + \frac{1^2}{a_1+}
\frac{2^2}{a_2+}
\frac{3^2}{a_3 +} \frac{4^4}{a_4 +} \cdots
$$
Continued fractions are too big to put inline. Display them with `$$…$$` or use a notation like `[a0;a1,a2,a3,…]` . 

连分数通常都太大以至于不易于排版，所以建议在连分数前后声明 `$$` 符号，或使用像 `[a0;a1,a2,a3,…]` 一样的紧缩记法。 

## 七、一些特殊的注意事项

These are issues that won't affect the correctness of formulas, but might make them look significantly better or worse. Beginners should feel free to ignore this advice; someone else will correct it for them, or more likely nobody will care.

现在指出的小问题并不会影响方程式及公式等的正确显示，但能让它们看起来明显更好看。初学者可无视这些建议，自然会有强迫症患者替你们改掉它的，或者更可能地，根本没人发现这些问题。

Don't use `\frac` in exponents or limits of integrals; it looks bad and can be confusing, which is why it is rarely done in professional mathematical typesetting. Write the fraction horizontally, with a slash: 

在以e为底的指数函数、极限和积分中尽量不要使用 `\frac` 符号：它会使整段函数看起来很怪，也正是因此它在专业数学排版中从不出现。横着写这些分式，中间使用斜线间隔 `/` 。 

例子：

1. `\begin{array}{cc}`
2. `\mathrm{Bad} & \mathrm{Better} \\`
3. `\hline \\`
4. `e^{i\frac{\pi}2} \quad e^{\frac{i\pi}2}& e^{i\pi/2} \\`
5. `\int_{-\frac\pi2}^\frac\pi2 \sin x\,dx & \int_{-\pi/2}^{\pi/2}\sin x\,dx \\`
6. `\end{array}`

显示： 

$$
\begin{array}{cc}
\mathrm{Bad} & \mathrm{Better} \\
\hline \\
e^{i\frac{\pi}2} \quad e^{\frac{i\pi}2}& e^{i\pi/2} \\
\int_{-\frac\pi2}^\frac\pi2 \sin x\,dx & \int_{-\pi/2}^{\pi/2}\sin x\,dx \\
\end{array}
$$
The `|` symbol has the wrong spacing when it is used as a divider, for example in set comprehensions. Use `\mid` instead: 

`|` 符号在被当作分隔符时会产生错误的间隔，因此在需要分隔时最好使用 `\mid` 来代替它。 

例子:

1. `\begin{array}{cc}`
2. `\mathrm{Bad} & \mathrm{Better} \\`
3. `\hline \\`
4. `\{x|x^2\in\Bbb Z\} & \{x\mid x^2\in\Bbb Z\} \\`
5. `\end{array}`

显示： 

$$
\begin{array}{cc}
\mathrm{Bad} & \mathrm{Better} \\
\hline \\
\{x|x^2\in\Bbb Z\} & \{x\mid x^2\in\Bbb Z\} \\
\end{array}
$$
For double and triple integrals, don't use `\int\int` or `\int\int\int` . Instead use the special forms `\iint` and `\iiint` : 

使用多重积分符号时，不要多次使用 `\int` 来声明，直接使用 `\iint` 来表示 **二重积分** ，使用 `\iiint` 来表示 **三重积分** 等。对于无限次积分，可以用 `\int \cdots \int` 表示。 

例子：

1. `\begin{array}{cc}`
2. `\mathrm{Bad} & \mathrm{Better} \\`
3. `\hline \\`
4. `\int\int_S f(x)\,dy\,dx & \iint_S f(x)\,dy\,dx \\`
5. `\int\int\int_V f(x)\,dz\,dy\,dx & \iiint_V f(x)\,dz\,dy\,dx`
6. `\end{array}`

显示： 

$$
\begin{array}{cc}
\mathrm{Bad} & \mathrm{Better} \\
\hline \\
\int\int_S f(x)\,dy\,dx & \iint_S f(x)\,dy\,dx \\
\int\int\int_V f(x)\,dz\,dy\,dx & \iiint_V f(x)\,dz\,dy\,dx
\end{array}
$$
无 限 次 积 分 ： ⋯

Use `\,` , to insert a thin space before differentials; without this 

will mash them together:

在微分符号前加入 `\,` 来插入一个小的间隔空隙；没有 `\,` 符号的话， 

将会把不同的微分符号堆在一起。

例子：

1. `\begin{array}{cc}`
2. `\mathrm{Bad} & \mathrm{Better} \\`
3. `\hline \\`
4. `\iiint_V f(x)dz dy dx & \iiint_V f(x)\,dz\,dy\,dx`
5. `\end{array}`

显示： 

$$
\begin{array}{cc}
\mathrm{Bad} & \mathrm{Better} \\
\hline \\
\iiint_V f(x)dz dy dx & \iiint_V f(x)\,dz\,dy\,dx
\end{array}
$$
