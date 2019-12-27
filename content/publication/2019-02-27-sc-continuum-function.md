---
title: "Strongly compact cardinals and the continuum function"
authors: [A.W. Apter, S. Dimopoulos, T. Usuba]
date: 2019-02-27
doi: ""
math: true
diagram: true
markup: mmark

# Schedule page publish date (NOT publication's date).
publishDate: 2019-27-02

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: "ArXiv"
publication_short: ""

abstract: "" #"We study the general problem of the behaviour of the continuum function in the presence of non-supercompact strongly compact cardinals."

# Summary. An optional shortened abstract.
#summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags: ""
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: https://arxiv.org/abs/1901.05313
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
#image:
#  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/jdD8gXaTZsc)'
#  focal_point: ""
#  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

This is a joint paper with Arthur W. Apter and Toshimichi Usuba, which looks at the problem of changing the continuum function while preserving strongly compact cardinals. Among other results, it contains a new breakthrough by Usuba regarding the violation of GCH at a strongly compact cardinal from optimal assumptions.

Easton's theorem (see Theorem 15.18 in [Jech's book](https://www.springer.com/gp/book/9783540440857)) was a milestone in set theory, which showed that ZFC by itself does not impose severe limitations on the behaviour of the continuum function at regular cardinals. However, when we bring large cardinals into the picture, the situation is more complicated. Often the mere violation of GCH at a large cardinal requires strong assumptions. The prototypical example is the case of a measurable cardinal. By results of Gitik [here](https://www.sciencedirect.com/science/article/pii/0168007289900699) and [here](https://core.ac.uk/download/pdf/82536312.pdf) (see also Mitchell's [article](https://www.cambridge.org/core/journals/mathematical-proceedings-of-the-cambridge-philosophical-society/article/the-core-model-for-sequences-of-measures-i/3E6F0DB1000D093E43CDA775FC2CACC8)), the violation of GCH at a measurable cardinal is equiconsistent with the existence of a measurable cardinal $$\kappa$$ such that $$o(\kappa) = \kappa^{+ +}$$.

In this paper, we look at the possible behaviour of the continuum function in the presence of strongly compact cardinals that are not supercompact. Our goal will be to work with strongly compact cardinals which possess no non-trivial degrees of supercompactness. There are fundamental open questions in this regard, such as whether it is possible to force GCH at an arbitrary non-supercompact strongly compact cardinal.

As motivation, let us mention that if we allow enough supercompactness assumptions, the continuum function at a non-supercompact strongly compact cardinal can be manipulated fairly easily. For instance, to realise a $$\Delta_2$$-definable Easton function $$F$$, we can use a result due to [Menas](https://www.jstor.org/stable/1997517), which shows that it is possible to realise $$F$$ while preserving the supercompactness of a cardinal $$\kappa$$. We can then use [Magidor's Prikry iteration](https://www.sciencedirect.com/science/article/pii/0003484376900243) that destroys all measurable cardinals below $$\kappa$$. In the resulting model, $$\kappa$$ is strongly compact, $$\kappa$$ is the least measurable cardinal (and so is not $$2^\kappa$$-supercompact), and $$F$$ is still realised.

In a similar vein, suppose that $$F$$ is an Easton function definable by a $$\Delta_2$$ formula in a model $$V$$ of ZFC + GCH in which $$\lambda$$ is a supercompact limit of supercompact cardinals. The aforementioned theorem of Menas shows that it is possible to force over $$V$$ to obtain a model $$V_1$$ in which $$\lambda$$ remains a supercompact limit of supercompact cardinals and the Easton function $$F$$ has been realised.

In $$V_1$$, let $$\kappa \lt \lambda$$ be the least measurable limit of supercompact cardinals. Another theorem of Menas shows that in $$V_1$$, $$\kappa$$ is both strongly compact and not $$2^\kappa$$-supercompact. In particular, by starting with hypotheses stronger than the existence of a measurable limit of supercompact cardinals, it is possible to force and construct a model containing a non-supercompact strongly compact cardinal in which $$F$$ has been realised.

Also, if we assume that the strongly compact cardinal has a sufficient degree of supercompactness, there are positive results. In [this article](https://arxiv.org/abs/math/9808012), Hamkins shows that if $$\kappa$$ is both strongly compact and $$\lambda$$-supercompact, then $$\kappa$$ can be forced to have its strong compactness and $$\lambda$$-supercompactness indestructible under any $$\kappa$$-directed closed forcing that has size at most $$\lambda$$.  In particular, it is possible to realise suitable Easton functions in the interval $$[\kappa,\lambda)$$.

Our results are separated into two categories, depending on whether we are interested in preserving a single strongly compact cardinal or more than one strongly compact cardinal. For the former, we first answer a long-standing open question on the problem of whether it is possible to violate GCH at a strongly compact cardinal using no stronger assumptions. We show that just assuming $$2^\kappa =\kappa^+$$ and $$\kappa$$ is strongly compact, it is possible to preserve the strong compactness of $$\kappa$$ while forcing any desired value for $$2^\kappa$$. This result is due to the T. Usuba. We then address the question of what sort of Easton functions can be realised in the presence of a certain non-supercompact strongly compact cardinal. We show that if $$\kappa$$ is the least measurable limit of supercompact cardinals and $$F$$ is an arbitrary Easton function defined on regular cardinals greater than or equal to $$\kappa$$, then it is possible to force to realise $$F$$ while preserving the fact that $$\kappa$$ is the least measurable limit of supercompact cardinals. The techniques used, however, will of necessity destroy many supercompact cardinals. We therefore also present another result along the same lines, where the Easton function realised has restrictions placed on it, but all supercompact cardinals are preserved.

For the latter, we begin by showing how to iterate the partial orderings used in Section 3 so as to preserve all measurable limits of supercompact cardinals simultaneously, while realising certain Easton functions at all of them. We then prove a theorem which gives a partial answer to the problem of the simultaneous preservation of all supercompact and measurable limits of supercompact cardinals while violating GCH at each of them. Finally, Section 5 contains some open questions.

In order to present our results in full generality, we make the minimal number of assumptions on the structure of the class of strongly compact and supercompact
cardinals in our ground model. However, if we force over a model in which GCH and the property of *compactness coincidence*[^1] both hold (such as the one constructed by the first author and Shelah [here](https://arxiv.org/abs/math/9502232)), then all strongly compact cardinals will be preserved to our generic extension. This is since the only strongly compact cardinals which exist in a model satisfying compactness coincidence are the supercompact cardinals and the measurable limits of supercompact cardinals.


[^1]: The property of *compactness coincidence* states that the strongly compact and supercompact cardinals coincide, except at measurable limit points.
