---
layout: page
title: Blog
permalink: /blog/
---

# Why is deep learning interesting?

*Daniel Murfet 5-10-2020*

Deep learning consists of a family of statistical models that can be optimised by [automatic differentiation](https://en.wikipedia.org/wiki/Automatic_differentiation) to well approximate complicated real-world distributions and which obey [power](https://arxiv.org/abs/1712.00409) [laws](https://arxiv.org/abs/2001.08361) in the scaling limit of large datasets and large compute. In my opinion deep learning is interesting because of the conjunction of the following four factors:

* **Ability to fit complex data.** There are many natural data distributions for which we know approximations by neural networks but not by any other function approximation method, e.g. the probability that a given image [contains an Aadvark](http://www.image-net.org/explore?wnid=n02082791), the discounted future value of an arbitrary [move in Go](https://www.youtube.com/watch?v=WXuK6gekU1Y), or the probability distribution of the next word in an [arbitrary sentence written on the Internet](https://arxiv.org/abs/2005.14165).

* **Generalisation**. Stochastic gradient descent (SGD) is the optimisation algorithm which locates good configurations of a deep neural network among all possible parameters. In practice for modern architectures and with modern initialisation and normalisation, sufficiently large datasets and sufficient compute there is a high probability of SGD finding a neural network which not only achieves low loss on the training set but generalises well to the true distribution.

* **Power laws**. It has been observed in Transformer models of natural language that the test loss `L(n)` trained with early stopping on a dataset of size `n` is proportional to `n^{-0.095}`. Such [power laws](https://arxiv.org/abs/2001.08361) are (in DM's opinion) likely to be from a historical perspective one the most important scientific discoveries of the early 21st century (with a much larger practical impact, and achieved at much lower cost, than the discovery of the Higgs boson).

* **Parallelisation**. The performance of single-core CPUs hit a roof several decades ago. But neural network training can be made parallel in both the model and the data, so that large number of cores can be utilised to train large networks on large datasets. This means that the gains of scale predicted by power laws can be *realised in practice*. 

It seems likely that we will continue to see interesting new phenomena emerge as the large scale regime for Transformers is explored (e.g. [GPT-3](https://www.gwern.net/newsletter/2020/05#gpt-3)) and as new architectures with even more favourable scaling exponents are found.
