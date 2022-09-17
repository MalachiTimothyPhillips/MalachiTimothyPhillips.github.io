---
title: "pplacerDC: a new scalable phylogenetic placement method"
collection: publications
permalink: /publication/pplacer-dc
date: 2021-09-25
venue: 'Proceedings of the 12th ACM Conference on Bioinformatics, Computational Biology, and Health Informatics'
paperurl: 'https://dl.acm.org/doi/abs/10.1145/3459930.3469516'
---

This paper presents a novel algorithm for phylogenetic placement that is scalable to large datasets.
The general idea is to decompose a given tree using a centroid decomposition, and to apply recursively until the trees are small enough such that they may be solved using pplacer.
From there, the results are merged together to produce a final placement.

[Link to paper](https://dl.acm.org/doi/abs/10.1145/3459930.3469516)
[Link to code](https://github.com/kodingkoning/pplacerDC)

bibtex entry:
```
@inproceedings{koning2021ppiacerdc,
  title={ppIacerDC: a new scalable phylogenetic placement method},
  author={Koning, Elizabeth and Phillips, Malachi and Warnow, Tandy},
  booktitle={Proceedings of the 12th ACM Conference on Bioinformatics, Computational Biology, and Health Informatics},
  pages={1--9},
  year={2021}
}
```