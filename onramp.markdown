---
layout: page
title: Onramp
permalink: /onramp/
---

How do you get started? Here is our onramp for new students:

  * **Step 1**: read Michael Nielsen's excellent online book "[Neural networks and deep learning](http://neuralnetworksanddeeplearning.com/)" from beginning to end. Understand and run all the code, and do the exercises. In a previous life Nielsen worked on quantum computing, you might have read his [textbook](https://www.amazon.com/Quantum-Computation-Information-10th-Anniversary/dp/1107002176) as a physics student.
  
  * **Step 2**: buy a copy of the [deep learning book](https://www.deeplearningbook.org/). For work in singular learning theory, the basic background is Chapter 3 Probability and Information theory (3.1-3.13), Chapter 5, Chapter 6, and Chapter 8 and for more advanced topics Chapter 19 (for variational inference and ELBO). You should know what the following terms mean: *Bayesian posterior*, *Kullback-Leibler divergence*, *feedforward network*, *stochastic gradient descent*.
  
  * **Step 3**: install and learn how to use one of the deep learning packages, [PyTorch](https://pytorch.org/) or [TensorFlow](https://www.tensorflow.org/).
  
 More background reading:

  * For more advanced topics in information theory and machine learning, see David MacKay's [Information Theory, Inference, and Learning Algorithms](https://www.inference.org.uk/itprnn/book.pdf).
  
  * For reinforcement learning see [Sutton & Barto](http://incompleteideas.net/book/the-book-2nd.html).
  
For the projects related to singular learning theory:

  * S. Watanabe "[Almost all learning machines are singular](http://watanabe-www.math.dis.titech.ac.jp/users/swatanab/foci2007.pdf)", Invited Paper in FOCI2007.
  
  * S. Watanabe "[A Widely Applicable Bayesian Information Criterion](http://www.jmlr.org/papers/volume14/watanabe13a/watanabe13a.pdf)" Journal of Machine Learning Research 14 (2013) 867-897.
  
# Installing software

You can run some tutorials and basic experiments using free hosted Jupyter notebooks such as [Google Colab](https://colab.research.google.com/) however for research you will want to set up your own machine (preferably with a GPU, but this is not strictly necessary). Operating systems in order of preference for deep learning development are Linux > Mac > Windows. You might have trouble on Windows. For experiments we usually need to use cloud machines, either [AWS](https://aws.amazon.com/) or [GCP](https://cloud.google.com/) (expensive!) or on local clusters such as [Nectar](https://nectar.org.au/) or [Spartan](https://dashboard.hpc.unimelb.edu.au/).

You will need the following

  * Python >= 3.7 (on Mac or Windows you might like to install this via [Anaconda](https://www.anaconda.com/distribution/)).
  * Deep learning libraries [PyTorch](https://pytorch.org/get-started/locally/) or [TensorFlow 2](https://www.tensorflow.org/install) on top of Python, what we use depends on the project.
  * If you have a GPU you want to install drivers and [CUDA](https://developer.nvidia.com/cuda-zone) (a parallel computing platform and programming model developed by NVIDIA for general computing on GPUs) in the way suggested on the webpages for PyTorch and TensorFlow. If you only have a CPU (e.g. you are on a laptop) you can run the same code, but more slowly.

You will run your models either through Jupyter notebooks hosted locally (Anaconda can help with that) or through Python files that you host and run through some other IDE (Susan likes [PyCharm](https://www.jetbrains.com/pycharm/)).

  * *Example*: DM has two machines in his home office, an iMac (no GPU) and a Linux machine (with a GPU) on which is installed TensorFlow, PyTorch etc. They are on an Ethernet network, and the Linux machine is setup to serve via Apache a Jupyter notebook over HTTP to the iMac machine. DM just opens a Jupyter notebook via a browser, and is connected via the Terminal and SSH to the Linux machine. GPUs are expensive, but if you are serious about deep learning and comfortable building your own machine, you should consider building a Linux machine to run experiments.

Installing all this can be a painful process, when you get stuck **Google your error** and try again. Finally, find some basic PyTorch or TensorFlow tutorial online (e.g. training a small CNN on MNIST) and run it on your local machine to make sure everything works. 

**If you get really stuck, drop into office hours** and one us will try to help (see the main page).
