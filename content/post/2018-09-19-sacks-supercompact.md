---
title: Sacks forcing and supercompact cardinals
date: 2018-09-19
math: true
diagram: true
slug: "sacks-supercompact"
#markup: mmark
tags:
  - Supercompact cardinals
  - Sacks forcing
---

Time for the first ever blog post! And it is about one of my favourite topics, the preservation of large cardinals through forcing.

The motivation behind this post, is a discussion I had with James Cummings in the "Set theory today" conference that took place in the KGRC in Vienna last week. He explained to me how supercompact cardinals can be preserved through iterations of Sacks forcing, a fact that I was not aware of and which I find very useful. Although the technique was already known by some set theorists (Sy Friedman and Radek Honzik were aware of it for instance), it seems that it has not appeared in the literature yet. So, with James' permission, in this post I will describe the proof that he showed me.

I believe it would be useful to say a few words on why such a technique is useful. One of the most interesting and active areas in set theory is to fully understand the behaviour of the continuum function, which calculates the size of the power set of all infinite cardinals. During the late 20th century we had a wealth of results that have given us a much greater understanding of this problem. However, things get more complicated when we bring large cardinals in the picture. Given a large cardinal, the challenge is to find all the possible configurations of the continuum function that can be true while preserving the properties of the large cardinal.

Originally, the main forcing notion that was used to force a desired configuration of the continuum function was Cohen forcing. However, about ten years ago, in work of S. Friedman, R. Honzik and K. Thompson ([here](http://logika.ff.cuni.cz/radek/papers/optimal-Easton-revised.pdf) and [here](http://www.logic.univie.ac.at/~sdf/papers/joint.katie.perfect.pdf)), Sacks forcing was used instead, bringing a new insight to the problem. The definition of Sacks forcing is more complicated than that of Cohen forcing, but it offers more room for combinatorial arguments and in a sense, this is the reason that we are able to have preservation arguments for large cardinals.

Let us now move to the main part of the post. If $\kappa$ is an inaccessible cardinal, let $Sacks(\kappa)$ denote the forcing notion whose conditions are trees $p \subseteq 2^{\lt \kappa}$ that satisfy the following conditions:
1. $p$ is downwards closed: for all $s\in p$ and $t\subseteq s$, $t\in p$,
2. $p$ does not have leaves: every $s\in p$ has a proper extension in $p$,
3. $p$ is upwards $\kappa$-closed: if $\langle s_\alpha\mid \alpha \lt \beta \lt \kappa \rangle$ is an increasing sequence of nodes in $p$, then their union is also in $p$,
4. there are club-many splitting levels: If $Split(p)$ denotes the set of nodes $s\in p$ such that $s^\frown 0,s^\frown 1\in p$, then there is a club $C\subseteq \kappa$ such that $Split(p)$ is exactly the set of nodes that their length is some ordinal in $C$.

The order of the forcing is inclusion, which means that $p$ is stronger than $q$ iff $p\subseteq q$. The definition is taken from [here](http://www.logic.univie.ac.at/~sdf/papers/joint.katie.perfect.pdf), where you can find information about the various properties of $Sacks(\kappa)$. In particular, it is a $\kappa$-closed and $\kappa^{+ +}$-c.c. forcing that adds an unbounded subset of $\kappa$, without collapsing any cardinals. In order to add $\lambda$-many Sacks subsets to $\kappa$, where $\lambda> \kappa$, we use $Sacks(\kappa,\lambda)$ which denotes the product forcing of length $\lambda$ and support $\leq \kappa$, where each factor is equal to $Sacks(\kappa)$.

Now, to go to our specific case, we wish to add $\lambda$-many Sacks subsets to a supercompact cardinal $\kappa$, while preserving its supercompactness. As usual, we would first need to do some preparatory forcing, like adding an appropriate number of Sacks subsets to every inaccessible cardinal below $\kappa$. Then, fixing a $\lambda$-supercompactness embedding $j:V\to M$ we would do a "generic" lift of $j$ through this preparatory forcing and then, we would come to the task of further lifting $j$ through $Sacks(\kappa,\lambda)$. The standard way to do this is by finding a master condition $q$ that extends all conditions of the form $j(p)$, where $p$ is a condition in the generic filter for $Sacks(\kappa,\lambda)$. It is exactly this construction that James described to me and for the sake of presentation, I am going to ignore the preparatory forcing and assume we already have the right generic embedding. The following theorem describes how to construct the master condition.

Theorem
=======

Suppose $\kappa$ is supercompact and $\lambda>\kappa$ is a cardinal such that $\lambda^\kappa=\lambda$. Also, assume that $G$ is a $V$-generic filter for $Sacks(\kappa,\lambda)$ and $j:V\to M$ is a generic $\lambda$-supercompactness embedding with $G\in M$. Then, there is a condition $q\in j(Sacks(\kappa,\lambda))$ such that $q\leq j(p)$ for all $p\in G$.

Proof
-----

Fix $\kappa,\lambda,G$ and $j$ as above. We are going to take as given that $Sacks(\kappa,\lambda)$ has the $\lambda$-c.c. and $M$ is closed under $\lambda$-sequences in $V[G]$. For more details, see [here]([here](http://www.logic.univie.ac.at/~sdf/papers/joint.katie.perfect.pdf)).

First, we need to specify the domain of $q$. Since $Sacks(\kappa,\lambda)$ is a $\leq\kappa$-support product, the domain of each $p\in G$ can be seen as a $\kappa$-sized subset of $\lambda$. By a standard density argument, we can easily see that every possible $\kappa$-sized subset of $\lambda$ appears as a domain in some condition in $G$, hence we define the domain of $q$ to be the set
$$A=j``[\lambda]^\kappa=\{j(a)\mid a\subseteq \lambda, |a|=\kappa\}.$$

Now, if we fix some $\alpha\in A$, we wish to define $q(\alpha)$ as an $M$-Sacks tree of height $j(\kappa)$. This will be done by an induction on $j(\kappa)$, i.e. on the levels of the tree, in $V[G]$. We impose the inductive hypothesis that at any stage $\beta$, if $s$ is a node at the $\beta$-level of $q(\alpha)$, then $s\in j(p)(\alpha)$ for all $p\in G$ with $\alpha\in supp(p)$. This is reasonable, since we want $q$ to extend all these conditions at the end of the construction.

To deal with the limit case first, suppose $\beta$ is a limit ordinal and that we have constructed all levels of $q(\alpha)$ smaller than $\beta$. By definition, each $p\in G$ is an upwards $\lt\kappa$-closed perfect tree and by elementarity, $j(p)$ is an upwards $\lt j(\kappa)$-closed tree in $M$. Thus, we do the only choice we have, i.e. add all branches that have been constructed so far. Formally, any function $s:\beta\to 2$ such that all its initial segments are in the already constructed levels of the tree, is itself a node in the $\beta$-level of $q(\alpha)$. Note that the construction takes place in $V[G]$, but since $M$ is closed under $\lambda$-sequences, everything can be defined in $M$ too. Also, it is clear that the inductive hypothesis still holds.

Now, we look at the successor case and this is the crucial step, as we need to decide which nodes will split or not. To do this, let

$D_\alpha=\bigcap\\{C\\mid C$ is the splitting club of $j(p)(\alpha)$ for some $p\in G$ such that $\\alpha\\in supp(j(p))\\}.$


Since $M$ is closed under $\lambda$-sequences and $G$ has size $\lambda$, $D_\alpha\in M$ and it is the intersection of $\lambda$-many clubs of $j(\kappa)$. Thus, $D_\alpha$ is a club of $j(\kappa)$ in $M$ and it is going to be the club of splitting levels of $q(\alpha)$.

Back to the construction, suppose we have defined the $\beta$-level of $q(\alpha)$ and $s$ is node of height $\beta$. If $\beta\in D_\alpha$, then we put both $s^\frown 0$ and $s^\frown 1$ in the $(\beta+1)$-level. If not, we have to choose only one extension of $s$. By the inductive hypothesis, there is $p\in G$ such that $s\in j(p)(\alpha)$. Then, either $s^\frown 0$ or $s^\frown 1$ is in $j(p)(\alpha)$ and without loss of generality, assume $s^\frown 0 \in j(p)(\alpha)$. Then, we let $s^\frown 0$ also be in the $(\beta+1)$-level of $q(\alpha)$, but we need to check if the inductive hypothesis will still hold. Let $p'\in G$ be some other condition such that $\alpha\in supp(j(p'))$. By genericity, there is $r\in G$ such that $r\leq p,p'$ and by elementarity, $j(r)(\alpha)\leq j(p)(\alpha),j(p')(\alpha)$. Since $j(r)(\alpha)$ extends $j(p)(\alpha)$, it has to be the case that $s^\frown 0\in j(r)(\alpha)$ and similarly, since it extends $j(p')(\alpha)$ it has to be the case that $s^\frown 0\in j(p')(\alpha)$. Thus, the inductive hypothesis indeed holds and the construction is complete.

Clearly, $q$ extends all conditions in $j``G$ and thus, the proof is complete.    $\square$

The theorem shows how to construct a master condition when we add Sacks subsets to $\kappa$ but in fact, the same technique would work when we add subsets to a cardinal greater than $\kappa$, as long as $j$ has a sufficient degree of supercompactness.

Since I am a beginner to the blog business, any comment or remark about the post is welcome! To contact me, you can find my email at the "Contact" section of the website.
