---
author: Carson Connard
title: Things I've been thinking about recently
date: 2025-02-18
description: math currently on my mind
math: true
---

A place for me to talk about some of my recent mathematical musings.
<!--more-->
---

{{< math.inline >}}
{{ if or .Page.Params.math .Site.Params.math }}
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.css" integrity="sha384-zB1R0rpPzHqg7Kpt0Aljp8JPLqbXI3bhnPWROx27a9N0Ll6ZP/+DiW/UqRcLbRjq" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.js" integrity="sha384-y23I5Q6l+B6vatafAwxRu/0oK/79VlbSz7Q9aiSZUvyWYIYsd+qj+o24G5ZU2zJz" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
{{ end }}
{{</ math.inline >}}

## [02-18-25] Morse-Bott homology

{{< math.inline >}}

<p>
In preparation for a talk at the grad student Differential Geometry Seminar at UW, I've been digging in to some different directions coming from the Morse theory that I studied at the end of my undergrad. Namely, I've been reading about Morse-Bott functions, and how they pose a sort of "non-isolated" form of Morse theory/handle decomposition. Namely, in Bott's paper <i>Nondegenerate critical submanifolds</i>, the isomorphism \(H_k(M^{p+\epsilon}\cap U,M^{p-\epsilon}\cap U)\cong H_{k-\lambda}(\{p\})\) is extended to the situation in which we have a space \(S\) consisting of a disjoint union of finitely many connected <i>submanifolds</i> of critical points; that is, \(H_k(M^{p+\epsilon}\cap U,M^{p-\epsilon}\cap U)\cong H_{k-\lambda}(S)\). (<i>Note: our choice of \(p\in S\) here is arbitrary; we impose the condition that \(\text{Hess}_f(p)\) is nondegenerate in the normal direction to \(S\) for all \(p\).</i>)
</p>

<p>
A paper that I've found to be of interest (ableit, it may not be the source of material that I will cover in my talk) is <i>Morse-Bott homology</i>, authored by A. Banyaga and D. Hurtubise. I found great interest in Morse homology (i.e., part 1 of Audin and Damian's book) during my first exposure to it, and the extension to orbifolds in Cho and Hong's paper <i>Orbifold Morse-Smale-Witten complexes</i> was a similar positive learning experience. Banyaga and Hurtubise's paper is again an extension of classical results for Morse functions on Riemannian manifolds to a more general setting, and I look forward to working through this paper.
</p>

{{</ math.inline >}}


## [11-27-23] More general structure than expected?

{{< math.inline >}}

<p> 
As mentioned in my previous post, we can construct product structures via the use of Gromov-Witten invariants. However, note the following theorem, due to (at least in part, I believe) Gromov:
</p>

<p> 
<b> Theorem. </b> Symplectic manifolds always have almost-complex structures which are compatible with the symplectic structure. Further, there exists an infinite-dimensional space of compatible almost-complex structures. This space is contractible however, and leads to the fact that all of these almost-complex structures are in fact homotopy equivalent.
</p>

<p>
So, in the case of manifolds, up to homotopy, the crucial data which allows for the application of Gromov-Witten theory to deform cohomology products does not come from symplectic structure, rather the almost-complex structure on the manifold. This extends to Lagrangians: it is known that a Lagrangian submanifold will be totally-real with respect to the almost-complex structure on the manifold. This motivates the following:
</p>

<p>
<b> If we consider a symplectic orbifold </b> \(\mathcal{X}\) <b> and a Lagrangian suborbifold </b> \(\mathcal{L}\subset\mathcal{X}\), <b> then the data required to extract the exotic product described in the previous post on </b> \(H^\bullet(I_{\mathcal{X}}\mathcal{L})\) <b> is dependent on some almost-complex/totally-real structure instead of symplectic/Lagrangian structure. </b>
</p>

{{</ math.inline >}}

## [11-22-23] Chen-Ruan product analogue for "Lagrangian suborbifolds"

{{< math.inline >}}

<p>
Consider a symplectic manifold \((X,\omega)\) whose cohomology \(H^\bullet(X)\) is equipped with the Poincaré pairing \(\langle\cdot,\cdot\rangle\).

Gromov-Witten theory is a powerful tool in symplectic geometry which connects to mathematical physics, namely Type IIA string theory. The main point of study are the Gromov-Witten invariants, which "count" genus \(g\) pseudo-holomorphic curves with \(n\) marked points, mapping into \(X\). That is, we consider <i> stable maps </i> \(f: \mathbb{C} P^1\to X\). It turns out that the set of these functions forms a moduli space, which allows us to define the Gromov-Witten invariants:
</p>

<p>
<b> Definition. </b> Consider the stable maps \(\mathbb{C} P^1\to X\) of genus \(g\), where \(\mathbb{C}P^1\) has \(n\) marked points. Then we can form a moduli space \(\mathcal{M}_{g,n}(X)\) of such curves. Note that for our use, we only consider genus 0 curves with 3 marked points; that is, \(\mathcal{M}_{0,3}(X)\). We define the <i> evaluation maps </i> on the moduli space, \(\text{ev}_i:\mathcal{M}_{0,3}(X)\to X\), by sending a stable map to the value of the stable map at a marked point, \([f:(\mathbb{C}P^1,x_1,x_2,x_3)\to X]\mapsto f(x_i)\).
</p>

<p>
This moduli space and its evaluation maps allow us to define the Gromov-Witten invariants. Consider three cohomology classes \(\alpha,\beta,\gamma\) on \(X\). Then the <i> Gromov-Witten invariants </i> are given as
$$
GW_{0,3}(X)=\int_{\mathcal{M}_{0,3}(X)} \text{ev}_1^*\alpha\wedge\text{ev}_2^*\beta\wedge\text{ev}_3^*\gamma.
$$
</p>

<p>
Interestingly, if we identify the Poincaré pairing with the Gromov-Witten invariants of \(X\), 
$$
\langle\alpha\star\beta,\gamma\rangle=GW_{0,3}(X),
$$
it turns out that the product \(\star\) which satisfies this equality is the <i> quantum product </i> on the quantum ring \(H^\bullet(X)[[q]]\). If we now restrict to just constant curves by setting \(q=0\), this quantum product reduces to the standard cup product on \(H^\bullet(X)\).

We can do the same construction for a Lagrangian submanifold \(L\subset X\), but we instead consider a "disk" with three marked points instead of a projective sphere \(\mathbb{C}P^1\) as the source for the pseudo-holomorphic curves.
</p>

<p>
I spent the majority of the Summer of 2023 working with orbifolds; an extension of the ideas mentioned above would be to a symplectic orbifold \(\mathcal{X}\). It turns out that when similar processes as above are performed on \(\mathcal{X}\), we require the use of the cohomology of the <i> inertia orbifold</i> \(I\mathcal{X}\). Amazingly, when we identify
$$
\langle\alpha\star\beta,\gamma\rangle=GW_{0,3}(\mathcal{X})
$$
and restrict to \(q=0\), we retrieve the <i> Chen-Ruan product </i> on \(H^\bullet(I\mathcal{X})[[q]]\)! This is a remarkable result, as this product structure is not immediately observable when one studies the cohomology of orbifolds.
</p>

<p>
We also would like to study a Lagrangian suborbifold \(\mathcal{L}\subset\mathcal{X}\) as modeled in the manifold case. However, the notion of a "Lagrangian suborbifold" is not well defined. However, in a 2023 <a href="https://arxiv.org/abs/2308.01595">preprint</a> of Chen, Ono, and Wang, the idea of the <i> dihedral twisted sector </i> \(I_{\mathcal{X}}\mathcal{L}\) is introduced -- as the notation may suggest, this acts as a sort of Lagrangian "relative" to \(\mathcal{X}\). 
</p>

<p>
<b> So, we conjecture that another exotic cohomology product could be constructed on </b> \(I_{\mathcal{X}}\mathcal{L}\) <b> by restricting </b> \(H^\bullet(I_\mathcal{X}\mathcal{L})[[q]]\) <b> to </b> \(q=0\).
</p>

<p>
In an alternative approach towards such a result, techniques from  <a href="https://arxiv.org/abs/math/0502280">this paper</a> suggest the need to construct a <i> double </i> inertia orbifold \(II_{\mathcal{X}}\mathcal{L}\) and an obstruction class in its \(K\)-theory. This would provide an explicit description of this conjectured product structure on the cohomology of the dihedral twisted sector.
</p>
{{</ math.inline >}}


