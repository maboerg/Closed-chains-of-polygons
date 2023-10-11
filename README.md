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

Figure 3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`m = 7`&nbsp;&nbsp;and&nbsp;&nbsp;`m = 10`

- Is it possible to build closed chains by joining identical regular polygons as suggested by figure 3?
- Are there finitely many of them?
- Can we proceed to more neighbouring vertices lying in the interior?
- How far can we proceed?
  
We introduced the number of neighbouring vertices of each polygon lying in the interior of the chain (in figures 1, 2, this number is&nbsp; $2~$; in figure 3 this number is&nbsp; $3~$ resp.&nbsp; $4~$).&nbsp; If we ignore the vertices where two polygons meet we reduce this number by&nbsp; $2~$.&nbsp; The reduced number will be denoted by&nbsp; $n~$.&nbsp; It is the number of "free" inner neighbouring vertices of each polygon. For another definition of&nbsp; $n~$ we describe the interior of the chain as "star" with&nbsp; $n~$ "points" (identical to the number of polygons); then neighbouring points lie&nbsp; $n~$ vertices apart.

Now we have a parameter $n$ establishing a system of chains. 

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

$n$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Number of "free" inner neighbouring vertices of each polygon. Neighbouring points of the inner star lie&nbsp; $n~$ vertices apart.

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

$2/j + (4+2n)/m~=~1$

$j\cdot m~=~2\cdot m + j\cdot (4+2n)$

Now we have a short equation for&nbsp; $n,~m,~j$.&nbsp; We can transform this equation in two ways:

$2\cdot m~=$&nbsp; $j\cdot (m-4-2n)$ &nbsp;&nbsp;&nbsp;and&nbsp;&nbsp;&nbsp; $m\cdot (j-2)~=~j\cdot (4+2n)$

$2\cdot m\cdot (4+2n)$&nbsp; $=$&nbsp; $j\cdot (4+2n)\cdot (m-4-2n)$&nbsp; $=$&nbsp; $m\cdot (j-2)\cdot (m-4-2n)$

$\mathbf{(1)}$ &nbsp; $\mathbf{8 + 4n~=~(j-2)(m-4-2n)}$

With&nbsp; $n~$ given we have&nbsp; $j-2~$ and&nbsp; $m - 4 - 2n~$ as divisors of&nbsp; $8+4n~$. The number of divisors of&nbsp; $k~$ is denoted by&nbsp; $d(k)$ .
This is our main result:

$\mathbf{(2)}$ &nbsp; $\mathbf{a(n) = d(8 + 4n)}$

With&nbsp; $(t_1, t_2)$ &nbsp;running through all pairs of divisors of&nbsp; $8+4n~$ (meaning&nbsp; $t_1\cdot t_2~=~8 + 4n$&nbsp;)&nbsp; we get

$\mathbf{(3)}$ &nbsp; $\mathbf{m = t_1 + 4 + 2n}$ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\mathbf{j = t_2 + 2}$

The divisors `1, 2, 4, 2+n, 4+2n, 8+4n` appear for every `n`. For `n = 0` there are two doublets, leaving `1, 2, 4, 6`. For `n = 2` there is one doublet, leaving `1, 2, 4, 8, 16`.

`m - 4 - 2n > 0`, so `m > 5`.  With `m - 4 - 2n = 1` all odd `m > 3` appear, with `m - 4 - 2n = 2` all even `m > 4` appear, with `n` running from `0`.

With `n` running, `8 + 4n = 4(2 + n)` has all natural `t` as divisors. With `t = j - 2` all `j > 2` will appear.

We got a complete result:

- There are infinitely many closed chains of identical regular polygons.

- For each `n` there are several and finitely many closed chains.

- The exact number of closed chains is `a(n) = d(8 + 4n)`.

- For `n = 0` there are `a(0) = 4` closed chains. For `n = 2` there are `a(2) = 5` closed chains. For all other `n` there are `a(n) > 5` closed chains.

- `a(n) = 6   <--->   n = 6  or  n+2 prime`.

- The number of vertices in each polygon is `m = t + 4 + 2n` where `t` runs through the divisors of `8 + 4n`. The corresponding number of `m-gons` in the chain is `j = (8+4n)/t + 2`.

- Changing the roles of `m` and `j` we get: The number of polygons in the chain is `j = t + 2` where `t` runs through the divisors of `8 + 4n`. The corresponding number of vertices in each of the `j` polygons is `m = (8+4n)/t + 4 + 2n`.

- For every `m > 4` exists a closed chain of `m-gons`.

- For every `j > 2` exists a closed chain with exactly `j` polygons.

We compare this result with the figures above:

In figure 1 we have `n = 0` and `m = 5`. From (1) we get `j = 10`. Thus the chain will eventually close, see figure 6.

In figure 2 we have `n = 0`. We know `a(0) = 4`. There must be two other chains with a regular polygon as interior. One of these is the completion of figure 1. See figure 6 for all four chains.

In figure 3 left we have `n = 1` and `m = 7`. From (1) we get `j = 14`. Thus the chain will eventually close, see figure 7.

In figure 3 right we have `n = 2` and `m = 10`. From (1) we get `j = 10`. Thus the chain will eventually close, see figure 8.

In figure 4 we have `n = 3` and `m = j = 12`. This matches with (1), see figure 9.

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

Here is a Mathematica list of a(n):

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

The pictures appeal by their symmetry and beauty. We stopped at `n = 3`. With increasing `n` the polygons appear more and more like circles, though some more nice examples can be produced - the reader should try and display them by a suitable program.

The aesthetic value of the chains may be attributed to a variety of notions in art and nature. Some of the notions coming to mind - with some fantasy - are shown in figure 10.

![figure10b](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/afa64479-5104-46f5-b9f5-dde45b6f06ed)

Figure 10

The (more or less) star-like interiors of the chains give pleasant pictures in their own way, see figure 11.

![figure11b](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/59d90c50-0da3-4b6a-97c4-ab484d5e137f)

Figure 11

### OEIS

The sequence `d(.)` rendering the number of divisors of natural numbers is available in the database OEIS as A000005.

We got `a(n) = d(8 + 4n)` in (2). Remember that `a(n)` starts with `n=0`. See the sequence A000005 with a(n) highlighted:

1, 2, 2, 3, 2, 4, 2, $\textbf{4}$, 3, 4, 2, $\textbf{6}$, 2, 4, 4, $\textbf{5}$, 2, 6, 2, `6`, 4, 4, 2, `8`, 3, 4, 4, `6`, 2, 8, 2, `6`, 4, 4, 4, `9`, 2, 4, 4, `8`, 2, 8, 2, `6`, 6, 4, 2, `10`, 3, 6, 4, `6`, 2, 8, 4, `8`, 4, 4, 2, `12`, 2, 4, 6, `7`, 4, 8, 2, `6`, 4, 8, 2, `12`, 2, 4, 6, `6`, 4, 8, 2, `10`, 5, 4, 2, `12`, 4, 4, 4, `8`, 2, 12, 4, `6`, 4, 4, 4, `12`, 2, 6, 6, `9`, 2, 8, 2, `8`




