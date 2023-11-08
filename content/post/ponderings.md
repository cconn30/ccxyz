---
author: Carson Connard
title: Things I've been thinking about recently
date: 2023-11-07
description: math currently on my mind
math: true
---

A place for me to talk about some of my recent mathematical musings
<!--more-->
---
## [11-07-23] Stringy product analogue for "Lagrangian suborbifolds"
Gromov-Witten theory is a powerful invariant in symplectic topology which count pseudoholomorphic curves on symplectic manifolds. A standard construction of this "enumerative geometry" is the so-called quantum product, which is (handwavily) constructed as follows:


{{< math.inline >}}
{{ if or .Page.Params.math .Site.Params.math }}
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.css" integrity="sha384-zB1R0rpPzHqg7Kpt0Aljp8JPLqbXI3bhnPWROx27a9N0Ll6ZP/+DiW/UqRcLbRjq" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.js" integrity="sha384-y23I5Q6l+B6vatafAwxRu/0oK/79VlbSz7Q9aiSZUvyWYIYsd+qj+o24G5ZU2zJz" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
{{ end }}
{{</ math.inline >}}

{{< math.inline >}}
<p>
Consider a symplectic manifold \((X,\omega)\) equipped with a Poincare pairing \(\langle\cdot,\cdot\rangle\), and consider its cohomology \(H^\bullet(X)\). Via the theory of pseudoholomorphic curves, one can study a moduli space \(\mathcal{M}\) of holomorphic maps from \(\mathbb{C}P^1\to X\) with three marked points. 
</p>

<p>
Consider three cohomology classes \(\alpha,\beta,\gamma\) on the target \(X\), and integrate
$$
A(\alpha,\beta,\gamma)=\int_{\mathcal{M}} \text{ev}_1^*\alpha\wedge \text{ev}_2^*\beta\wedge \text{ev}_3^*\gamma.
$$
This defines a 3-tensor, which turns out is such that \(A(\alpha,\beta,\gamma)=\langle\alpha\star\beta,\gamma\rangle\); this product \(\star\) is the <i> quantum product </i>. This product along with the Poincare pairing which \(X\) is equipped with define a Frobenius algebra over \(\mathbb{C}[[q]]\). If we set \(q=0\), we are effectively just counting the constant, or zero-energy, holomorphic curves: it turns out that this retrieves the standard cohomology of \(X\).
</p>

<p>
If we consider now a Lagrangian submanifold \(L\subset X\), we can again study the moduli space of curves on a disk with boundary on \(L\) with three marked points, and deform the cup product on \(H^\bullet(L)\). This determines a non-commutative Frobenius algebra, where again restricting to constant curves allows one to retrieve the cohomology of \(L\).
</p>

<p>
I spent the majority of the Summer of 2023 working with orbifolds; naturally, an extension of the ideas mentioned above would be to symplectic orbifolds. It turns out that when similar processes as above are performed on an orbifold \(\mathcal{X}\) (which requires the use of the <i> inertia orbifold</i>), we are able to construct the <i> stringy </i> product. This is a remarkable result, as this product structure is not immediately observable when one studies the cohomology of orbifolds.
</p>

<p>
As mentioned in the manifold case, we also would like to study the Lagrangian case. However, the notion of a "Lagrangian suborbifold" is not well defined. However, in a 2023 <a href="https://arxiv.org/abs/2308.01595">preprint</a> of Chen, Ono, and Wang, the idea of the <i> dihedral twisted sector </i> \(I_{\mathcal{X}}L\) is introduced -- as the notation may suggest, this acts as a sort of Lagrangian "relative" to \(\mathcal{X}\). <b> So, we conjecture that another exotic cohomology product could be constructed on </b> \(I_{\mathcal{X}}L\).
</p>
{{</ math.inline >}}


