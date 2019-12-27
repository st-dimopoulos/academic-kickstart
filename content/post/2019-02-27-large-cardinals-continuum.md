---
title: Violating GCH at large cardinals - why is it interesting and what's new
date: 2019-02-27
math: true
diagram: true
#markup: mmark
tags:
- Large cardinals
- Strongly compact cardinals
- Supercompact cardinals
- Continuum function
- Easton functions
---

While I was creating the [publication entry]({{< relref "2019-02-27-sc-continuum-function.md" >}}) for the recent submitted preprint joint with A. W. Apter and T. Usuba, I decided it is worth writing a separate blogpost explaining how our results extend an ongoing problem in set theory, the violation of GCH at large cardinals from optimal assumptions. This is connected to the problem of understanding the continuum function, which existed since the very early days of set theory, since Cantor himself was interested in the possible value of the continuum and formulated the Continuum Hypothesis. Of course, we now have a vast amount of results that have given us a much greater understanding of the behaviour of the continuum function, especially for regular cardinals.

My focus as usual will be large cardinals -at least measurable- and whether we can blow up the size of their power sets without destroying their large cardinal properties. Somewhat surprisingly, just violating GCH at a measurable cardinal while preserving its measurability is quite a hard task. Gitik made this precise ([here](https://www.sciencedirect.com/science/article/pii/0168007289900699) and [here](https://core.ac.uk/download/pdf/82536312.pdf)) by showing that to violate GCH at a measurable cardinal $\kappa$ we have to assume it has Mitchell rank at least $\kappa^{+ +}$. We were thus presented with the challenge to try and find what is the consistency strength of the violation of GCH at the various large cardinals above measurable.

Why is such a task useful? For someone already interested in large cardinals there is no point in asking this question, but the applications that emerged from such results can convince even a large cardinal "scepticist". The first and most important is the violation of GCH at a strong limit singular cardinal, which is a statement of non-trivial large cardinal strength as Gitik [showed]((https://core.ac.uk/download/pdf/82536312.pdf). In fact, the way we do it is to first violate GCH at a measurable $\kappa$ of Mitchell order $\kappa^{+ +}$ and then using Prikry forcing, turn $\kappa$ into a singular cardinal. With some more effort, we can even force $\kappa$ to become $\aleph_\omega$. This method of collapsing a large cardinal where GCH fails has been since applied to establish the consistency of several other statements like [the tree property at accessible cardinals](https://www.sciencedirect.com/science/article/pii/0003484372900174), or the [possible "small powers" of cardinals](https://link.springer.com/article/10.1007/BF01624081) and the list continues to grow. Therefore, the violation of GCH at large cardinals is often used to establish an upper bound on the consistency of a certain combinatorial property, thus it becomes important to know the optimal hypothesis from which we can force this violation.

How successful have we been? We have certainly managed to violate GCH at several large cardinals from modest assumptions and it is worth noting that a lot of breakthroughs were found in the last decade or so! We have a much better understanding of the problem in regard to [strong](http://logika.ff.cuni.cz/radek/papers/optimal-Easton-revised.pdf), [superstrong](http://logika.ff.cuni.cz/radek/papers/optimal-Easton-revised.pdf) and [supercompact](https://link.springer.com/article/10.1007/BF02761175) cardinals, but to my knowledge, results about extendible, huge and larger cardinals are still imperfect.

I did not mention strongly compact cardinals yet, for which the only known way to force a violation of GCH was to assume they have supercompactness properties. In autumn 2017, I visited Arthur Apter in New York and asked him if there was any progress in reducing the known hypotheses. At that time, the state of the art was Hamkins' use of the [lottery preparation](https://arxiv.org/abs/math/9808012) to show the following.

Theorem (Hamkins, 2000)
=======================

If $\kappa$ is strongly compact and $\lambda$-supercompact for some $\lambda\gt \kappa$, then we can force $2^\kappa=\lambda$ while preserving the strong compactness of $\kappa$.


Arthur noted that for certain special cases of strongly compact cardinals we do not necessarily need stronger assumptions. Recalling Menas' result that any measurable limit of supercompact cardinals is strongly compact, Arthur noted that if $\kappa$ is a measurable limit of supercompact cardinals, then we can actually force any desired value for $2^\kappa$ without assuming any stronger property for $\kappa$. This was amazing news since the least measurable limit of supercompact cardinals is not even $\kappa^+$-supercompact, which so far had been a necessary assumption.

That was the start of a joint project with Arthur, where we established generalisations of his result and wondered if there is any way to violate GCH at a strongly compact cardinal without stronger assumptions. The answer came from T. Usuba who heard about our progress and communicated to us the following unpublished theorem of his.

Theorem (Usuba, 2018)
===============

Suppose $\kappa$ is a strongly compact cardinal. Then, there is a forcing extension in which the strong compactness of $\kappa$ becomes indestructible under the Cohen forcing that adds $\lambda$-many subsets to $\kappa$, for any $\lambda\gt \kappa$.

This of course means that the violation of GCH at strongly compact cardinals from optimal assumptions is done! What is remarkable in Usuba's proof is that he uses only existing forcing technology, thus implying that even for larger large cardinals we could potentially establish similar results. To see the full proof of Usuba's theorem, along with other results, check our submitted [preprint](https://arxiv.org/pdf/1901.05313.pdf).

As for extendible cardinals, there has been [recent progress](https://arxiv.org/abs/1810.09195) by Bagaria and Poveda who considered violations of GCH on $C^{(n)}$-extendible cardinals in general. Their results are even broader since they address the issue of realising Easton functions, but one theorem that can be isolated from their results is the following.

Theorem (Bagaria `&` Poveda, 2018)
=========================

Suppose $\kappa$ is an extendible cardinal. If $F$ is a $\Delta_2$-definable Easton function, then we can force $2^\kappa=F(\kappa)$ while preserving the extendibility of $\kappa$.

Finally, as we climb the final steps of the large cardinal hierarchy, Dimonte and Friedman worked recently on the violation of GCH on [rank-into-rank cardinals](https://users.dimi.uniud.it/~vincenzo.dimonte/Dimonte_Friedman.pdf). In particular for $I0$-cardinals they show the following neat result.

Theorem (Dimonte `&` Friedman, 2014)
====================================

Suppose $\kappa$ is an $I0$ cardinal as witnessed by $j: L(V_{\lambda+1})\to L(V_{\lambda+1})$ and $F$ is an Easton function such that $E\restriction \lambda$ is definable in $V_\lambda$. Then, there is a forcing extension in which $\kappa$ remains $I0$ and $2^\kappa=F(\kappa)$.

The large cardinal zoo is vast and there is definitely more work to do. As an epilogue, I want to mention that no matter how innocent it seems, the violation of GCH at large cardinals can be a real challenge and quite often led to the discovery of completely new techniques for the preservation of large cardinals in forcing extensions.
