---
layout: page
title: Blog
permalink: /blog/
---

# Why is deep learning interesting?

Deep learning consists of a family of statistical models that can be optimised by [automatic differentiation](https://en.wikipedia.org/wiki/Automatic_differentiation) to well approximate complicated real-world distributions (e.g. the probability that a given image [contains an Aadvark](http://www.image-net.org/explore?wnid=n02082791), the discounted future value of an arbitrary [move in Go](https://www.youtube.com/watch?v=WXuK6gekU1Y), or the probability distribution of the next word in an [arbitrary sentence written on the Internet](https://arxiv.org/abs/2005.14165)) and which obey [power](https://arxiv.org/abs/1712.00409) [laws](https://arxiv.org/abs/2001.08361) in the scaling limit of large datasets and large compute.

* **Generalisation**. Stochastic gradient descent (SGD) is the optimisation algorithm which locates good configurations of a deep neural network among all possible parameters. In practice for modern architectures and with modern initialisation and normalisation, sufficiently large datasets and sufficient compute there is a high probability of SGD finding a neural network which both (a) achieves low loss on the training set and (b) generalises well to the test set. Deep learning is important because of the conjunction of (a) and (b).

* **Power laws**. The existence of [power laws](https://arxiv.org/abs/2001.08361) for neural language models is (in DM's opinion) likely to be from a historical perspective one the most important scientific discoveries of the early 21st century (with a much larger practical impact, and achieved at much lower cost, than the discovery of the Higgs boson).
