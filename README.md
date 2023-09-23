# Closed-chains-of-polygons
Number of closed chains of identical regular polygons

## Introduction

WORK IN PROGRESS - TO BE COMPLETED SOON

We want to assemble identical regular polygons in order to build closed chains of high symmetry.

`m` is the number of vertices - meaning that we assemble `m`-polygons in a "circular" way.

A possible start is shown in figure 1.

![figure01](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/1813d65b-7c50-4dc1-bba9-de354c39c31d)

Figure 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`m = 5`&nbsp;&nbsp; Will this chain eventually close to a perfect and symmetrical chain?

The following considerations and proofs should encourage the readers of this contribution to program all possible ways for closed chains of regular polygons.

## Simple examples

The polygons have to be joined edge to edge in a "circular" way as suggested by figure 1.

`j` is the number of polygons in a closed chain.

Two examples of closed chains come easily to mind as they are well known from the domain of tessellations; see figure 2.

![figure02](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/d4b2eb65-1436-4163-9e90-f29f7fca8dcc)

Figure 2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Left:&nbsp;`m = j = 6`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Right:&nbsp;`m = 8`&nbsp;&nbsp;`j = 4`

Here the first questions arise:
- Are there other closed chains similar to those in figure 2 with the described properties?
- Finitely many?

## More ways to create chains

Before we present any theory let's have a look at other ways of joining the polygons. In figures 1 and 2 exactly `2` neighbouring vertices of each polygon lie in the interior of the chain. But that can be changed. In figure 3 we see `3` resp. `4` neighbouring vertices lying in the interior.

![figure02b](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/57606683-d43d-4c21-98e1-f14bcf2cb531)

Figure 3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`m = 7`&nbsp;&nbsp;and&nbsp;&nbsp;`m = 10`

- Is it possible to build closed chains by joining identical regular polygons as suggested by figure 3?
- Are there finitely many of them?
- Can we proceed to more neighbouring vertices lying in the interior?
- How far can we proceed?
  
We introduced the number of neighbouring vertices of each polygon lying in the interior of the chain (in figures 1, 2, this number is `2`; in figure 3 this number is `3` resp. `4`). If we ignore the vertices where two polygons meet we reduce this number by `2`. The reduced number will be denoted by `n`. It is the number of "free" inner neighbouring vertices of each polygon. For another definition of `n` we describe the interior of the chain as "star" with `n` "points" (identical to the number of polygons); then neighbouring points lie `n` vertices apart.

Now we have a parameter `n` establishing a system of chains. 

- `n = 0`&nbsp;&nbsp;&nbsp;&nbsp;see three examples in figures 1, 2
- `n = 1`&nbsp;&nbsp;&nbsp;&nbsp;see an example in figure 3 left
- `n = 2`&nbsp;&nbsp;&nbsp;&nbsp;see an example in figure 3 right

If you (the reader) doubt if this is leading anywhere we present the closed chain in figure 4 for further motivation. I want to remark that with this picture we enter a domain of highly aesthetic geometry.

![figure02e](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/86325691-f641-4227-887f-f210b5cdca06)

Figure 4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`n = 3   m = j = 12`

## Counting the closed chains

Our aim is to assess for each `n` the number `a(n)` of closed chains. As yet `a(n)` could be `0` or `infinite`.

- `n = 0` yields an inner regular polygon.
- `n = 1` yields an interior proper star with identical edges and angles.
- `n > 1` yield star-like interiors with identical edges.

Now to exact geometry. Here are the parameters involved:

`n`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Number of "free" inner neighbouring vertices of each polygon. Neighbouring points of the inner star lie `n` vertices apart.

`a(n)`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Number of closed circular chains of identical regular polygons.

`m`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Number of vertices in each polygon.

`j`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Number of polygons in the chain.

Figure 5 shows the angles involved in our problem. We want to examine the case of closed chains. Then `&alpha; = 360°/j`.

![figure02g](https://github.com/maboerg/Closed-chains-of-polygons/assets/88709288/29c7e392-210b-4b0f-9fd8-8ebfe919a0b0)

Figure 5

## Program

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


