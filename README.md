# Self Supervised Learning for Graph Classification

This study analyzes the performance and problems of self-supervised approach on the challenges of graph-based deep learning, focusing on graph classification task and generalization. Two proposed approaches, namely Graph Adversarial Pseudo Group Contrast (GAPGC) and a selfsupervised domain adaptation method for size generalization, are briefly introduced. GAPGC enhances the relevance between pretext and downstream tasks, while the self-supervised domain adaptation approach exploits the d-pattern characterization of local structures. Both have proven superior performance over state-of-the-art methods. However, problems of limitations include assumptions on node and edge features, the need for domain knowledge, and access to the test distribution. Additionally, we present possible direction for exploring automated pretext task selection for different domains.

## Motivation

* Social networks, Molecular sciences, Transportation, E-commerce
* Reliance on labeled data causes poor generalization and less robustness

## SSL

* Designing the pretext task (contrast based, auxilary etc.)
* From pretext to downstream task
* Comparisons of SSL methods' performance among different domains (text, image and graphs)
* OOD Generalization and SSL

<p align="center">
    <img width=400 height=200 src="https://github.com/hasanselimyagci/ml-seminar-ssl-graphs/blob/main/img/SizeGen.jpg">
  </p>

## Related Works

* Test Time Adaptation strategy

## Graph Adversarial Pseudo Group Contrast

* Graph Pseudo-Positive Samples
* Adversarial Learnable Augmenter

<p align="center">
    <img src="https://github.com/hasanselimyagci/ml-seminar-ssl-graphs/blob/main/img/tta.jpg">
  </p>


## Performance Evaluation and Problems

* Contrastive learning as self supervised task during testing improves test performance
* ALA contributes more than GPPS but when combined performs the best on average
* Experiments on molecular scaffold OOD dataset demonstrated state-of-the-art performance on GNNs
* Access to test distribution in real datasets?
* Can the parametrized augmenter generalize to other learnable graph generators?
* GCL projector and MLP in augmenter initialization?

## References
* [GraphTTA](https://arxiv.org/abs/2208.09126 "Test Time Adaptation on Graph Neural Networks")
* [From Local Structures to Size Generalization in Graph Neural Networks](https://arxiv.org/abs/2010.08853)
* [Automated Self-Supervised Learning for Graphs](https://arxiv.org/abs/2106.05470)
