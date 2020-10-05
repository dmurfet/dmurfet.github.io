---
layout: page
title: Blog
permalink: /blog/
---

# Why is deep learning interesting?

Deep learning consists of a family of statistical models that can be optimised by [automatic differentiation](https://en.wikipedia.org/wiki/Automatic_differentiation) to well approximate complicated real-world distributions (e.g. the probability that a given image [contains an Aadvark](http://www.image-net.org/explore?wnid=n02082791), the discounted future value of an arbitrary [move in Go](https://www.youtube.com/watch?v=WXuK6gekU1Y), or the probability distribution of the next word in an [arbitrary sentence written on the Internet](https://arxiv.org/abs/2005.14165)) and which obey [power](https://arxiv.org/abs/1712.00409) [laws](https://arxiv.org/abs/2001.08361) in the scaling limit of large datasets and large compute.

* **Automatic differentiation**. Stochastic gradient descent (SGD) is the optimisation algorithm which locates good configurations of a deep neural network among all possible parameters. In practice for modern architectures and with modern initialisation and normalisation, sufficiently large datasets and sufficient compute there is a high probability of SGD finding a neural network which both (a) achieves low loss on the training set and (b) generalises well to the test set. This empirical fact remains a theoretical mystery.

* **Universality**. A small set of building blocks (feedforward, CNN, LSTM, Transformer) achieve good performance on a wide range of tasks across several modalities (vision, language, reinforcement learning). 

In the first place Deep Neural Networks (DNNs) are interesting *because they work*. So it is worth unpacking what this means.

* state of AI particularly in terms of choosing hyperparameters, cherry-picking, "throwing data at models and seeing what sticks", etc.? AI research is interesting but I can't help but feel a lot of it (at least the applied ML papers I've read) is very... dissatisfying.

Lot of hype from startups and overpromising (e.g. self-driving cars). Moreover, some of the most vocal critics of deep learning are also biased since they are professionally invested in alternative approaches to artificial intelligence.

While the variety of network architectures might seem overwhelming, it's worth keeping in mind that before deep learning there was a hand-crafted model for each tiny subset of computer vision, NLP, etc. etc., and and now deep learning models not only work much better (in many, perhaps most, cases) but the models are small variations on the same idea (resnets, Transformers, LSTMs) applied across a wide variety of tasks. So my sense is that deep learning has led to a remarkable unification of approaches across ML, viewed in the historical context. As @shreyash suggests, many expect that unification to continue.

For example, I find it remarkable that an architecture developed for language models (Transformers) plays an integral part in an agent (AlphaStar) developed to play a real time strategy game. That level of generality is quite surprising, although we quickly get used to it.
