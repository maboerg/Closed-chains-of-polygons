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


