# Closed-chains-of-polygons
Number of closed chains of identical regular polygons

### Introduction

We want to assemble identical regular polygons in order to build closed chains of high symmetry.

$m~$ is the number of vertices - meaning that we assemble $~m$-gons in a "circular" way.

A possible start is shown in figure 1.

![figure01](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/1813d65b-7c50-4dc1-bba9-de354c39c31d)

Figure 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`m = 5`&nbsp;&nbsp; Will this chain eventually close to a perfect and symmetrical chain?

The following considerations and proofs should encourage the readers of this contribution to program all possible ways for closed chains of regular polygons.

### Simple examples

The polygons have to be joined edge to edge in a "circular" way as suggested by figure 1.

$j~$ is the number of polygons in a closed chain.

Two examples of closed chains come easily to mind as they are well known from the domain of tessellations; see figure 2.

![figure02](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/d4b2eb65-1436-4163-9e90-f29f7fca8dcc)

Figure 2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Left:&nbsp;`m = j = 6`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Right:&nbsp;`m = 8`&nbsp;&nbsp;`j = 4`

Here the first questions arise:
- Are there other closed chains similar to those in figure 2 with the described properties?
- Finitely many?

### More ways to create chains

Before we present any theory let's have a look at other ways of joining the polygons. In figures 1 and 2 exactly&nbsp; $2~$ neighbouring vertices of each polygon lie in the interior of the chain. But that can be changed. In figure 3 we see&nbsp; $3~$ resp.&nbsp; $4~$ neighbouring vertices lying in the interior.

![figure02b](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/57606683-d43d-4c21-98e1-f14bcf2cb531)

Figure 3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`m = 7`&nbsp;&nbsp;and&nbsp;&nbsp;`m = 10`&nbsp;&nbsp; Will these chains eventually close to perfect and symmetrical chains?

- Is it possible to build closed chains by joining identical regular polygons as suggested by figure 3?
- Are there finitely many of them?
- Can we proceed to more neighboring vertices lying in the interior?
- How far can we proceed?
  
We introduce the number&nbsp; $n~$ of neighboring vertices of each polygon lying in the interior of the chain, ignoring the vertices where two polygons meet (in figures 1, 2, this number is&nbsp; $0~$; in figure 3 this number is&nbsp; $1~$ resp.&nbsp; $2~$).&nbsp; It is the number of "free" inner neighboring vertices of each polygon. For another definition of&nbsp; $n~$ we describe the interior of the chain as "star" with&nbsp; $j~$ "points" (identical to the number of polygons); then neighboring points lie&nbsp; $n~$ vertices apart.

Now we have a parameter&nbsp; $n$&nbsp; establishing a system of chains. 

- $~n = 0$&nbsp;&nbsp;&nbsp;&nbsp;see three examples in figures 1, 2
- $~n = 1$&nbsp;&nbsp;&nbsp;&nbsp;see an example in figure 3 left
- $~n = 2$&nbsp;&nbsp;&nbsp;&nbsp;see an example in figure 3 right

If you (the reader) doubt if this is leading anywhere we present the closed chain in figure 4 for further motivation. I want to remark that with this picture we enter a domain of highly aesthetic geometry.

![figure02e](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/86325691-f641-4227-887f-f210b5cdca06)

Figure 4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`n = 3   m = j = 12`

### Counting the closed chains

Our aim is to assess for each&nbsp; $n~$ the number&nbsp; $a(n)$&nbsp; of closed chains. As yet&nbsp; $a(n)$&nbsp; could be&nbsp; $0~$ or&nbsp; $\infty~$.

- $~n = 0$&nbsp;&nbsp;yields an inner regular polygon.
- $~n = 1$&nbsp;&nbsp;yields an interior proper star with identical edges and angles.
- $~n \gt 1$&nbsp;&nbsp;yield star-like interiors with identical edges.

Now to exact geometry. Here are the parameters involved:

$n$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Number of "free" inner neighboring vertices of each polygon. Neighboring points of the inner star lie&nbsp; $n~$ vertices apart.

$a(n)$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Number of closed circular chains of identical regular polygons.

$m$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Number of vertices in each polygon.

$j$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Number of polygons in the chain.

Figure 5 shows the angles involved in our problem.

![figure02h](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/f1d5c28b-d545-4394-94f9-b7fc035ee257)

Figure 5

We want to examine the case of closed chains. From figure 5 we get:

$\alpha = 360°/j$

$\beta = 360°/m$ &nbsp;&nbsp;(equals the central angle of the polygons)

$\gamma = 180° + 360°/m$

The sum of angles in the&nbsp; $(n+3)$-gon&nbsp; in figure 5 is&nbsp; $(n+1) 180°$.

$(n+1)\cdot 180°~=$&nbsp; $\alpha + 2\cdot\beta + n\cdot \gamma~=$&nbsp; $360°/j + 720°/m + n\cdot180° + n\cdot 360°/m$

$1~=~2/j + (4+2n)/m$

$j\cdot m~=~2\cdot m + j\cdot (4+2n)$

Now we have a short equation for&nbsp; $n,~m,~j$.&nbsp; We can transform this equation in two ways:

$2\cdot m~=$&nbsp; $j\cdot (m-4-2n)$ &nbsp;&nbsp;&nbsp;and&nbsp;&nbsp;&nbsp; $m\cdot (j-2)~=~j\cdot (4+2n)$

$2\cdot m\cdot (4+2n)$&nbsp; $=$&nbsp; $j\cdot (4+2n)\cdot (m-4-2n)$&nbsp; $=$&nbsp; $m\cdot (j-2)\cdot (m-4-2n)$

$\mathbf{(1)}$ &nbsp; $\mathbf{8 + 4n~=~(j-2)(m-4-2n)}$

With&nbsp; $n~$ given we have&nbsp; $j-2~$ and&nbsp; $m - 4 - 2n~$ as divisors of&nbsp; $8+4n~$. The number of divisors of&nbsp; $k~$ is denoted by&nbsp; $d(k)$ .
This is our main result:

$\mathbf{(2)}$ &nbsp; $\mathbf{a(n) = d(8 + 4n)}$

With&nbsp; $(t_1, t_2)$ &nbsp;running through all pairs of divisors of&nbsp; $8+4n~$ (meaning&nbsp; $t_1\cdot t_2~=~8 + 4n$&nbsp;)&nbsp; we get from (1)

$\mathbf{(3)}$ &nbsp; $\mathbf{m = t_1 + 4 + 2n}$ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\mathbf{j = t_2 + 2}$

The divisors&nbsp; $1,~2,~4,~2+n,~4+2n,~8+4n$&nbsp; appear for every&nbsp; $n$&nbsp;.&nbsp; For&nbsp; $n = 0$&nbsp; there are two doublets, leaving&nbsp; $1,~2,~4,~8$&nbsp;.&nbsp; For&nbsp; $n = 2$&nbsp; there is one doublet, leaving&nbsp; $1,~2,~4,~8,~16$&nbsp;.

$m - 4 - 2n~\ge 1$ ,&nbsp; so&nbsp; $m \ge 5$&nbsp;.&nbsp;  With divisor&nbsp; $m - 4 - 2n~= 1$&nbsp; all odd&nbsp; $m \ge 5$&nbsp; appear, for&nbsp; $m - 4 - 2n~=~2$&nbsp; all even&nbsp; $m \ge 6$&nbsp; appear, with&nbsp; $n$&nbsp; running from&nbsp; $0$&nbsp;.

With&nbsp; $n$&nbsp; running,&nbsp; $8 + 4n = 4(2 + n)$&nbsp; has all natural&nbsp; $t$&nbsp; as divisors. With&nbsp; $t = j - 2$&nbsp; all&nbsp; $j \ge 3$&nbsp; will appear.

We got a complete result:

- There are infinitely many closed chains of identical regular polygons.

- For each&nbsp; $n$&nbsp; there are several and finitely many closed chains.

- The exact number of closed chains is&nbsp; $a(n) = d(8 + 4n)$.

- For&nbsp; $n = 0$&nbsp; there are&nbsp; $a(0) = 4$&nbsp; closed chains. For&nbsp; $n = 2$&nbsp; there are&nbsp; $a(2) = 5$&nbsp; closed chains. For all other&nbsp; $n$&nbsp; there are&nbsp; $a(n) \ge 6$&nbsp; closed chains.

- $a(n) = 6~~~~\Longleftrightarrow~~~ n = 6~~~\text{or}~~~n+2 ~~ \text{odd and prime}$.

- The number of vertices in each polygon is&nbsp; $m = t + 4 + 2n$&nbsp; where&nbsp; $t$&nbsp; runs through the divisors of&nbsp; $8 + 4n$&nbsp;.&nbsp; The corresponding number of&nbsp; $m$-gons in the chain is&nbsp; $j = (8+4n)/t + 2$&nbsp;.

- Changing the roles of&nbsp; $m$&nbsp; and&nbsp; $j$&nbsp; we get: The number of polygons in the chain is&nbsp; $j = t + 2$&nbsp; where&nbsp; $t$&nbsp; runs through the divisors of&nbsp; $8 + 4n$&nbsp;.&nbsp; The corresponding number of vertices in each of the&nbsp; $j$&nbsp; polygons is&nbsp; $m = (8+4n)/t + 4 + 2n$&nbsp;.

- $m$&nbsp; and&nbsp; $j$&nbsp; are interdepending:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\mathbf{m = 4 + 2n + (8+4n)/(j-2)}$

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\mathbf{j = 2 + (8+4n)/(m-4-2n)}$

- For every&nbsp; $m \ge 5$&nbsp; exists a closed chain of&nbsp; $m$-gons.

- For every&nbsp; $j \ge 3$&nbsp; exists a closed chain with exactly&nbsp; $j$&nbsp; polygons.

We compare these results with the figures above:

In figure 1 we have&nbsp; $n = 0$&nbsp; and&nbsp; $m = 5$&nbsp;. From (1) we get&nbsp; $j = 10$&nbsp;.&nbsp; Thus the chain will eventually close, see figure 6.

In figure 2 we have&nbsp; $n = 0$&nbsp;.&nbsp; We know&nbsp; $a(0) = 4$&nbsp;.&nbsp; There must be two other chains with a regular polygon as the interior. One of these is the completion of figure 1. See figure 6 for all four chains.

In figure 3 left we have&nbsp; $n = 1$&nbsp; and&nbsp; $m = 7$&nbsp;.&nbsp; From (1) we get&nbsp; $j = 14$&nbsp;.&nbsp; Thus the chain will eventually close, see figure 7.

In figure 3 right we have&nbsp; $n = 2$&nbsp; and&nbsp; $m = 10$&nbsp;.&nbsp; From (1) we get&nbsp; $j = 10$&nbsp;.&nbsp; Thus the chain will eventually close, see figure 8.

In figure 4 we have&nbsp; $n = 3$&nbsp; and&nbsp; $m = j = 12$&nbsp;.&nbsp; This matches with (1), see figure 9.

&nbsp;

**Start and end of the list of&nbsp; $m$&nbsp; and the list of&nbsp; $j$**

With the exception&nbsp; $n=0$&nbsp; and&nbsp; $n=2$&nbsp;, these lists contain at least&nbsp; $6$&nbsp; elements. We want to describe the first and last three elements.

For each&nbsp; $n$&nbsp;, the first and the second&nbsp; $m$&nbsp; in ascending order are&nbsp; $5+2n$&nbsp; and&nbsp; $6+2n$&nbsp;. The third&nbsp; $m$&nbsp; depends on&nbsp; $3$&nbsp; being a divisor of&nbsp; $8+4n$&nbsp;. This gives&nbsp; $n=1$ mod $3$&nbsp;.

- Third&nbsp; $m=7+2n$&nbsp; if&nbsp; $n=1$ mod $3$&nbsp; and&nbsp; $m=8+2n$&nbsp; else.

$n=0$ mod $3~~~\Rightarrow~$&nbsp; third&nbsp; $m~=~2+6h$&nbsp; for some&nbsp; $h\ge 1$

$n=1$ mod $3~~~\Rightarrow~$&nbsp; third&nbsp; $m~=~3+6h$&nbsp; for some&nbsp; $h\ge 1$

$n=2$ mod $3~~~\Rightarrow~$&nbsp; third&nbsp; $m~=~6h$&nbsp; for some&nbsp; $h\ge 2$

This shows that the list of third&nbsp; $m$&nbsp; is given by OEIS [A047244](http://oeis.org/A047244) (shifted).

The last and the second to last&nbsp; $m$&nbsp; are&nbsp; $12+6n$&nbsp; and&nbsp; $8+4n$&nbsp;.&nbsp; The third last&nbsp; $m$&nbsp; depends on&nbsp; $3$&nbsp; being a divisor of&nbsp; $8+4n$&nbsp;, giving&nbsp; $n=1$ mod $3$&nbsp;. The third last&nbsp; $m$&nbsp; is&nbsp; $(8+4n)/t+4+2n$ (see above) with&nbsp; $t=3$&nbsp; if&nbsp; $n=1$ mod $3$&nbsp; and&nbsp; $t=4$&nbsp; else.

- Third last&nbsp; $m = (10/3)\cdot (2+n)$ if&nbsp; $n=1$ mod $3$&nbsp; and&nbsp; $m = 3\cdot (2+n)$&nbsp; else.
  
$n=0$ mod $3~~~\Rightarrow~$&nbsp; third last&nbsp; $m~=~6+9h$&nbsp; for some&nbsp; $h\ge 0$

$n=1$ mod $3~~~\Rightarrow~$&nbsp; third last&nbsp; $m~=~10+10h$&nbsp; for some&nbsp; $h\ge 0$

$n=2$ mod $3~~~\Rightarrow~$&nbsp; third last&nbsp; $m~=~12+9h$&nbsp; for some&nbsp; $h\ge 0$

For each&nbsp; $n$&nbsp;, the first and the second&nbsp; $j$&nbsp; in descending order are&nbsp; $10+4n$&nbsp; and&nbsp; $6+2n$&nbsp;. The third&nbsp; $j$&nbsp; depends on&nbsp; $3$&nbsp; being a divisor of&nbsp; $8+4n$&nbsp;, giving&nbsp; $n=1$ mod $3$&nbsp;.

- Third&nbsp; $j = (2/3)\cdot (7+2n)$ if&nbsp; $n=1$ mod $3$&nbsp; and&nbsp; $j = 4+n$&nbsp; else.
 
$n=0$ mod $3~~~\Rightarrow~$&nbsp; third&nbsp; $j~=~4+3h$&nbsp; for some&nbsp; $h\ge 0$

$n=1$ mod $3~~~\Rightarrow~$&nbsp; third&nbsp; $j~=~6+4h$&nbsp; for some&nbsp; $h\ge 0$

$n=2$ mod $3~~~\Rightarrow~$&nbsp; third&nbsp; $j~=~6+3h$&nbsp; for some&nbsp; $h\ge 0$

The last and the second to last&nbsp; $j$&nbsp; are&nbsp; $3$&nbsp; and&nbsp; $4$&nbsp;. The third last&nbsp; $j$&nbsp; depends on&nbsp; $3$&nbsp; being a divisor of&nbsp; $8+4n$&nbsp;, giving&nbsp; $n=1$ mod $3$&nbsp;.

- Third last&nbsp; $j = 5$&nbsp; if&nbsp; $n=1$ mod $3$&nbsp; and&nbsp; $j = 6$&nbsp; else.

### Programs

Readers are encouraged to program pictures of the chains. They may draw upon the following Mathematica code providing the enumeration of the chains.

```
Do[Print["n = ", n, "   a(n) = ", Length[Divisors[8 + 4 n]]]; 
 d = Divisors[8 + 4 n]; le = Length[d];
 Do[t1 = d[[i]]; t2 = (8 + 4 n)/d[[i]]; 
  Print["          m = ", t1 + 4 + 2 n, "   j = ", t2 + 2];
  , {i, le}], {n, 0, 19}]
 ``` 

Output

![figure03](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/0e428ba5-7986-40cd-b8fa-e3c4cd8be78a)

Here is a Mathematica list of&nbsp; $a(n)$&nbsp;:

```
Table[{n, Length[Divisors[8 + 4 n]]}, {n, 0, 107}] // TableForm
```

![figure04](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/463cf555-42b3-44ee-a486-c1fb20635833)

### Pictures

![figure06c](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/0b2fde28-9d57-4b6e-bd94-23e0ddeb0dcb)

Figure 6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`n = 0`

&nbsp;
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
&nbsp;

![figure07b](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/a1daa5fc-5b43-40e1-8ee3-0014abdc5268)

Figure 7&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`n = 1`

&nbsp;
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
&nbsp;

![figure08](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/a78381ea-862d-4e73-a996-f986ef2eb4b0)

Figure 8&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`n = 2`

&nbsp;
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
&nbsp;

![figure09](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/cf91c70f-f241-412a-9642-21509dd71c59)

Figure 9&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`n = 3`

&nbsp;
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
&nbsp;

The pictures appeal by their symmetry and beauty. We stopped at&nbsp; $n = 3$&nbsp;.&nbsp; With increasing&nbsp; $n$&nbsp; the polygons appear more and more like circles, though some more nice examples can be produced&nbsp; -&nbsp; the reader should try and display them using a suitable program.

The aesthetic value of the chains may be attributed to a variety of notions in art and nature. Some of the notions coming to mind - with some fantasy - are shown in figure 10.

![figure10b](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/afa64479-5104-46f5-b9f5-dde45b6f06ed)

Figure 10

The (more or less) star-like interiors of the chains give pleasant pictures in their own way, see figure 11.

![figure11b](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/59d90c50-0da3-4b6a-97c4-ab484d5e137f)

Figure 11

### OEIS

The sequence&nbsp; $a(n) = (4, 6, 5, 6, 8, 6, 6, 9, 8, 6, 10, 6, 8, 12, 7, 6, 12, 6, 10, 12, 8, 6, 12, 9, 8, 12, 10, 6, 16, 6,$
$8, 12, 8, 12, 15, 6, 8, 12, 12, 6, 16, 6, 10, 18, 8, 6, 14, 9, 12, 12, 10, 6, 16, 12, 12, 12, 8, 6, 20, 6, 8, 18, 9, ...)$&nbsp; was accepted by the database OEIS as [A366872](http://oeis.org/A366872) on Dec 12, 2023.

We got&nbsp; $a(n) = d(8 + 4n)$&nbsp; in (2). The sequence&nbsp; $d(.)$&nbsp; is [A000005](http://oeis.org/A000005) in OEIS. See the sequence A000005 with&nbsp; $a(n)$&nbsp; highlighted (remember that&nbsp; $a(n)$&nbsp; starts with&nbsp; $n=0$&nbsp;)&nbsp;:

1, 2, 2, 3, 2, 4, 2, $\textbf{4}$, 3, 4, 2, $\textbf{6}$, 2, 4, 4, $\textbf{5}$, 2, 6, 2, $\textbf{6}$, 4, 4, 2, $\textbf{8}$, 3, 4, 4, $\textbf{6}$, 2, 8, 2, $\textbf{6}$, 4, 4, 4, $\textbf{9}$, 2, 4, 4, $\textbf{8}$, 2, 8, 2, $\textbf{6}$, 6, 4, 2, $\textbf{10}$, 3, 6, 4, $\textbf{6}$, 2, 8, 4, $\textbf{8}$, 4, 4, 2, $\textbf{12}$, 2, 4, 6, $\textbf{7}$, 4, 8, 2, $\textbf{6}$, 4, 8, 2, $\textbf{12}$, 2, 4, 6, $\textbf{6}$, 4, 8, 2, $\textbf{10}$, 5, 4, 2, $\textbf{12}$, 4, 4, 4, $\textbf{8}$, 2, 12, 4, $\textbf{6}$, 4, 4, 4, $\textbf{12}$, 2, 6, 6, $\textbf{9}$, 2, 8, 2, $\textbf{8}, ...$

The OEIS sequence [A383168](http://oeis.org/A383168), accepted on Apr 18, 2025, displays a triangle containing the possible&nbsp; $m$&nbsp; for&nbsp; $n$&nbsp; in the&nbsp; $n-$&th row. The top of this OEIS file shows the flattened version:

$5, 6, 8, 12, 7, 8, 9, 10, 12, 18, 9, 10, 12, 16, 24, 11, 12, 14, 15, 20, 30, 13, 14, 15, 16, 18, 20, 24, 36, 15, 16, 18, 21, 28, 42, 17, 18, 20, 24, 32, 48, 19, 20, 21, 22, 24, 27, 30, 36, 54, 21, 22, 24, 25, 28, 30, 40, 60, 23, 24, 26, 33, 44, 66$

The OEIS sequence [A383169](http://oeis.org/A383169), accepted on Apr 18, 2025, displays a triangle containing the possible&nbsp; $j$&nbsp; for&nbsp; $n$&nbsp; in the&nbsp; $n-$&th row. The top of this OEIS file shows the flattened version:

$10, 6, 4, 3, 14, 8, 6, 5, 4, 3, 18, 10, 6, 4, 3, 22, 12, 7, 6, 4, 3, 26, 14, 10, 8, 6, 5, 4, 3, 30, 16, 9, 6, 4, 3, 34, 18, 10, 6, 4, 3, 38, 20, 14, 11, 8, 6, 5, 4, 3, 42, 22, 12, 10, 7, 6, 4, 3, 46, 24, 13, 6, 4, 3, 50, 26, 18, 14, 10, 8, 6, 5, 4, 3$
