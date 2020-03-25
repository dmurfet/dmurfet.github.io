---
layout: page
title: Onramp
permalink: /onramp/
---

# Background reading

  * The [deep learning book](https://www.deeplearningbook.org/). You probably want to buy a copy. This covers basic probability and information theory, machine learning as well as many common deep learning models. You can access the book on a page by page basis online, which is useful as a reference. For the singular learning theory work, the basic background is Chapter 3 Probability and Information theory (3.1-3.13), Chapter 5, Chapter 6, and Chapter 8 and for more advanced topics Chapter 19 (for variational inference and ELBO). Before you get started, you should know what the following terms mean: *Bayesian posterior*, *Kullback-Leibler divergence*, *feedforward network*, *stochastic gradient descent*.
  
  * For more advanced topics in information theory and machine learning, see David MacKay's [Information Theory, Inference, and Learning Algorithms](https://www.inference.org.uk/itprnn/book.pdf).
  
  * For reinforcement learning see [Sutton & Barto](http://incompleteideas.net/book/the-book-2nd.html).
  
For the projects related to singular learning theory:

  * S. Watanabe "[Almost all learning machines are singular](http://watanabe-www.math.dis.titech.ac.jp/users/swatanab/foci2007.pdf)", Invited Paper in FOCI2007.
  * S. Watanabe "[A Widely Applicable Bayesian Information Criterion](http://www.jmlr.org/papers/volume14/watanabe13a/watanabe13a.pdf)" Journal of Machine Learning Research 14 (2013) 867-897.
  
# Installing software

You can do quite a lot with free hosted Jupyter notebooks such as [Google Colab](https://colab.research.google.com/), where they give you access to a GPU. This might be a good idea to get started with some simple tutorials, but for serious development you will want to get something setup on your own machine (preferably with a GPU, but this is not strictly necessary). Operating systems in order of preference for deep learning development are Linux > Mac > Windows. In principle they all work, in practice you might have a lot of trouble with maintaining your packages and distributions on Windows. For serious experiments we usually need to run the experiments on cloud machines, either [AWS](https://aws.amazon.com/) or [GCP](https://cloud.google.com/) (expensive!) or on local clusters such as Nectar or Spartan (perhaps students cannot request these resources on their own, usually we will have access and assign logins to you if necessary).

You will need the following

  * Python >= 3.7 (on Mac or Windows you might like to install this via [Anaconda](https://www.anaconda.com/distribution/)).
  * Deep learning libraries [PyTorch](https://pytorch.org/get-started/locally/) or [TensorFlow 2](https://www.tensorflow.org/install) on top of Python, what we use depends on the project.
  * If you have a GPU you want to install drivers and [CUDA](https://developer.nvidia.com/cuda-zone) (a parallel computing platform and programming model developed by NVIDIA for general computing on GPUs) in the way suggested on the webpages for PyTorch and TensorFlow, so that you can use the GPU from within the libraries. If you only have a GPU (e.g. you are on a laptop) you can run the same code, but slowly.

You will run your models either through Jupyter notebooks hosted locally (Anaconda can help with that) or through Python files that you host and run through some other IDE (Susan likes [PyCharm](https://www.jetbrains.com/pycharm/)).

  * *Example*: DM has two machines in his home office, an iMac (no GPU) and a Linux machine (with a GPU) on which is installed TensorFlow, PyTorch etc. They are on an Ethernet network, and the Linux machine is setup to serve via Apache a Jupyter notebook over HTTP to the iMac machine. DM just opens a Jupyter notebook via a browser, and is connected via the Terminal and SSH to the Linux machine. GPUs are expensive, but if you are serious about deep learning and comfortable building your own machine, you should consider building a Linux machine to run experiments.

Installing all this can be a painful process, when you get stuck **Google your error** and try again. Finally, find some basic PyTorch or TensorFlow tutorial online (e.g. training a small CNN on MNIST) and run it on your local machine to make sure everything works. **If you get really stuck, feel free to drop into office hours** and one us will try to help (see the main page).
