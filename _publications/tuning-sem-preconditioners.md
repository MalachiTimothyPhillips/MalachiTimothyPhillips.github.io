---
title: "Tuning Spectral Element Preconditioners for Parallel Scalability on GPUs"
collection: publications
permalink: /publication/tuning-sem-preconditioners
date: 2022-02-24
venue: 'SIAM PP 22 Proceeding'
paperurl: 'https://doi.org/10.1137/1.9781611977141.4'
---

This paper is concerning runtime tuning spectral element preconditioners for parallel scalability on GPUs.
A nascent tuning strategy is proposed to help alleviate the difficulty of choosing a reasonable preconditioner for a given problem.
A variety of novel preconditioning schemes are also proposed, including $p$-multigrid with Chebyshev-accelerated Schwarz smoothers, low-order operator preconditioning, and even hybridizing the two approach by treating the low-order operator as the coarse grid operator.

[Link to paper](https://doi.org/10.1137/1.9781611977141.4)

bibtex entry:
```
@inbook{tuning-sem-preco,
author = {Malachi Phillips and Stefan Kerkemeier and Paul Fischer},
title = {Tuning Spectral Element Preconditioners for Parallel Scalability on GPUs},
booktitle = {Proceedings of the 2022 SIAM Conference on Parallel Processing for Scientific Computing (PP)},
chapter = {},
pages = {37-48},
doi = {10.1137/1.9781611977141.4},
URL = {https://epubs.siam.org/doi/abs/10.1137/1.9781611977141.4},
eprint = {https://epubs.siam.org/doi/pdf/10.1137/1.9781611977141.4},
}
```