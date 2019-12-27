---
title: Strong compactness and functions with the Menas property
date: 2018-10-13
math: true
diagram: true
#markup: mmark
tags:
- Strongly compact cardinals
- Fast function
- Menas property
---

In this blog post I will travel back to the 70s and discuss about a result that appeared [here](https://core.ac.uk/download/pdf/82143213.pdf). Briefly, the result says that we can always find fast functions for strongly compact cardinals which are limits of strongly compact cardinals, without the need to force one.

Before explaining what all this means, let me describe my motivation since this is a somewhat specialised post. First of all, the aforementioned paper is one of the most important ones in set theory, since among other results, it establishes the non-equivalence between strong compactness and supercompactness. One of the results in the article was recently brought to my attention by Arthur Apter and I was surprised that I could not find it in the modern literature. I believe it is quite beneficial to look at old results and recast them using modern tools, since it can make them more easily accessible to other researchers, without needing to trace the whole history. I am definitely not the first person who did this for Menas' paper, since Joel Hamkins [adapted Menas' techniques](https://arxiv.org/abs/math/9808012) to argue about the preservation of strong compactness in forcing extensions. In fact, part of this post is inspired by Hamkins' approach.

To delve into the details now, recall that
$\kappa$ is $\lambda$-strongly compact if there is an elementary embedding $j:V\to M$ with $\text{crit}(j)=\kappa$, $j(\kappa)\gt\lambda$, that satisfies the $\lambda$-*covering property*, meaning that for any $x\subseteq M$ that has size at most $\lambda$ in $V$,  there is a set $s\in M$ such that
$x \subseteq s$
and
$|s|^M\lt j(\kappa)$.


Fortunately, these embeddings come with an ultrapower characterisation. If $U$ is a $\kappa$-complete fine ultrafilter on $\mathcal{P}_\kappa \lambda$, the ultrapower embedding $j_U:V \to M_U$ will have $\text{crit}(j_U)=\kappa$ and $j_U(\kappa)>\lambda.$ As for the $\lambda$-covering property, one can see that the fineness of $U$ implies that ${[id]}_U$ is a cover for $j_U``\lambda$ that has size less than $j_U(\kappa)$ in $M_U$ and using that, we can actually build a cover for any subset of $M_U$ of size at most $\lambda$.

The standard approach to preserve large cardinals in forcing extensions is to lift the corresponding elementary embeddings. Strong compactness embeddings are somewhat problematic when it comes to lifting arguments, since often the covering property is not enough. However, Menas noticed that things work better if we have a function $f:\kappa\to \kappa$ such that we are able to pick for every $\lambda>\kappa$ a $\lambda$-strong compactness embedding $j$ for which $j(f)(\kappa)$ can be quite large, namely larger than the size of the cover of $j``\lambda$. Not so surprisingly, Hamkins called this the *Menas property*. Let's make this precise.

Definition
==========

If $\kappa$ is a strongly compact cardinal, then a function $f\colon\kappa\to \kappa$ has the *Menas property* if for all $\lambda\geq\kappa$ there is $\lambda$-strong compactness embedding $j:V\to M$ given by a fine ultrafilter $U$ on $\mathcal{P}_\kappa \lambda$, such that
$|{[id]}_U|^M\lt j(f)(\kappa)$.

What can we do with such a function? The point is that if we want to force a property at $\kappa$, we use a $\kappa$-iteration whose non-trivial stages are the closure points of the function $f$. What happens then, is that the image of the iteration under $j$ will have a big jump, since $j(f)(\kappa)$ is quite larger than $\kappa$. For someone familiar with lifting arguments, this gives the tail forcing a large degree of closure, so we can force to get a generic filter for it without seriously affecting the preservation argument. Back to the topic of the post, the result I am going to discuss about is the following.

Theorem (Menas, 1974)
=====================

If $\kappa$ is strongly compact and a limit of strongly compact cardinals, then the function $f:\kappa\to \kappa$, where $f(\alpha)$ is the least strongly compact cardinal greater than $\alpha$, has the Menas propety.

Menas left open the question of the existence of such functions for arbitrary strongly compact cardinals, until Hamkins [showed](https://arxiv.org/abs/math/9808012) that we can always force one, using Woodin's fast function forcing. I will give two proofs of Menas' result, the first follows the original with the addition of some details, while the second uses the more modern framework of elementary embeddings.

Menas' original proof
---------------------

Pick an arbitrary $\lambda\geq\kappa$ and denote the club of closure points of $f$ by $C$. Since $\kappa$ is measurable, we can fix a normal ultrafilter $W$ on $\kappa$. Also, for each $\alpha\in C$, let $U_\alpha$ be a fine ultrafilter on $\mathcal{P}_{f(\alpha)}\lambda$. Since $W$ is normal and $C$ is a club, $C\in W$.

Now, we use the fact that we can compose these fine ultrafilters to define a fine ultrafilter $U$ on $\mathcal{P}_\kappa\lambda$ given by:
<center>$X\in U \leftrightarrow \{\alpha\in C\mid X\cap \mathcal{P}_{f(\alpha)}\lambda\in U_\alpha\}\in W.$</center>
(For a proof of this fact, see Theorem 22.19 in [Kanamori's book](https://www.springer.com/gp/book/9783540888666)).

Let $j:V\to M$ be the ultrapower embedding by $U$ with $\text{crit}(j)=\kappa$. We want to show that $j$ is the embedding that will satisfy the required property for $f$.

For each $\alpha\in C$, let
$D_\alpha=\{x\in \mathcal{P}_{f(\alpha)}\lambda\mid \alpha\lt|x|\}$.
Since $U_\alpha$ is $\kappa$-complete and fine, $D_\alpha\in U_\alpha$ (consider sets in $U_\alpha$ containing $|\alpha|^+$ as a subset).
It follows that
$\bigcup_{\alpha\in C}D_\alpha\in W$.
For each $x\in \mathcal{P}_\kappa\lambda$, let $s(x)$ be the unique $\alpha\in C$ such that $x\in D_\alpha$. Clearly, $\kappa\subseteq {[s]}_U$ and we claim that the converse is also true. To see this, suppose $\kappa={[l]}_U$ and let ${[h]}_U\in {[s]}_U$, for some $h:\mathcal{P}_\kappa\lambda\to V$. We want to show that $X\in U$, where
$X=\{x\in \mathcal{P}_\kappa\lambda\mid h(x)\in l(x)\}$.


If we fix some $\alpha\in C$, then for all $x\in D_\alpha$, $s(x)=\alpha$ and so, $h(x)\in \alpha$. Also, it must be the case that $\{x\in \mathcal{P}_\kappa\lambda\mid l(x)\text{ is transitive and } l(x)>\alpha\}\in U$, as otherwise either $\kappa={[l]}_U$ is not transitive or $\kappa={[l]}_U\leq \alpha$. By the definition of $U$, it follows that $\{x\in \mathcal{P}_{f(\alpha)}\lambda\mid \alpha\subseteq l(x)\}\in U_\alpha$. Hence,
<center>$X\cap D_\alpha=\{x\in D_\alpha \mid h(x)\in l(x)\}\in U_\alpha,$</center>
and in particular, $X\cap \mathcal{P}_{f(\alpha)}\lambda\in U_\alpha$. Since $\alpha$ was arbitrary, it follows that $X\in U$ and therefore,
${[h]}_U\in {[\kappa]}_U$.

Now, it follows that
$\{x\in\bigcup_{\alpha\in C}D_\alpha \colon |x|\lt f(s(x))\}\in U$
and hence, $|{[id]}_U|^M\lt j(f)(\kappa)$. $\square$

As you can see, Menas' original proof relies a lot on combinatorics and the particular properties of fine ultrafilters. In the next proof, I try to factor out these arguments and take advantage of the rich theory of elementary embeddings that we have today.

Modern proof
------------

Firstly, although the Menas property refers only to ultrapower embeddings, we can actually relax this condition. Namely, if $j:V\to M$ is a $\lambda$-strong compactness embedding with $\text{crit}(j)=\kappa$ such that the cover $s\in M$ of $j``\lambda$ induced by the $\lambda$-covering property satisfies $|s|^M\lt j(f)(\kappa)$, then there is an ultrapower embedding $j_U$ that witnesses the Menas property. The construction is quite simple, since assuming we have such a $j$, we use $s$ to define an ultrafilter $U$ on $\mathcal{P}_\kappa \lambda$ in the standard way:
<center>$X\in U \leftrightarrow s\in j(X).$</center>
Now, through a standard factoring argument it can be shown that $|{[id]}_U|^M<j_U(f)(\kappa)$ (see Theorem 1.12 in [here](https://arxiv.org/abs/math/9808012)).

So, the proof boils down to constructing such a $j$. To do this, pick an arbitrary $\lambda\geq\kappa$ and let $j:V\to M$ be a $\lambda$-strong compactness embedding, with $s\in M$ being the cover of $j"\\lambda$ induced by the $\\lambda$-covering property. If in $M$ there is no strongly compact cardinal less or equal to $|s|^M$, then we already know that $j(f)(\kappa)$ is larger than $|s|^M$ and there is nothing to prove. Otherwise, let $\mu>\kappa$ be the least strongly compact cardinal in $M$ above $\kappa$ and below $|s|^M$ and let $k:M\to N$ be a $\theta$-strong compactness embedding with critical point $\mu$, where $\theta$ is any ordinal greater than $|s|^M$. This entails that there is $s'\in N$ such that $k``s\subseteq s'$ and $|s'|^N\lt k(\mu)$. Since in $M$ there is no strongly compact cardinal between $\kappa$ and $\mu$, by elementarity, in $N$ there is no strongly compact cardinal between $k(\kappa)=\kappa$ and $k(\mu)$.

{{< figure library="true" src="diagram2.png" lightbox="true" height="300px" width="300px" class="alignright" >}}

We claim now that the embedding $j^\ast=k\circ j$ has the required property. It is easy to see that $j^\ast$ is a $\lambda$-strong compactness embedding with $\text{crit}(j^\ast)=\kappa$. Also, $j^\ast``\lambda\subseteq s'$ and $s'$ has size less than $k(\mu)$ in $N$. As we said before, there is no strongly compact cardinal between $\kappa$ and $k(\mu)$ in $N$, therefore $j^\ast(f)(\kappa)>|s'|^N,$ as required. $\square$
