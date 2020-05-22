---
layout: page
title: Onramp
permalink: /onramp/
---

How do you get started? Here is our onramp for new students:

  * **Step 0**: Yann LeCun "[The Epistemology of Deep Learning](https://www.youtube.com/watch?v=gG5NCkMerHU)" is an excellent survey of the history of deep learning, and the need for theory.
  
  * **Step 1**: read Michael Nielsen's excellent online book "[Neural networks and deep learning](http://neuralnetworksanddeeplearning.com/)" from beginning to end. Understand and run all the code, and do the exercises (in a previous life Nielsen worked on quantum computing, you might have read his [textbook](https://www.amazon.com/Quantum-Computation-Information-10th-Anniversary/dp/1107002176) as a physics student).
  
  * **Step 2**: buy a copy of the [deep learning book](https://www.deeplearningbook.org/). For work in singular learning theory, the basic background is Chapter 3 Probability and Information theory (3.1-3.13), Chapter 5, Chapter 6, and Chapter 8 and for more advanced topics Chapter 19 (for variational inference and ELBO). You should know what the following terms mean: *Bayesian posterior*, *Kullback-Leibler divergence*, *feedforward network*, *stochastic gradient descent*.
  
  * **Step 3**: install and learn how to use one of the deep learning packages, [PyTorch](https://pytorch.org/) or [TensorFlow](https://www.tensorflow.org/).
  
 More background reading:

  * For more advanced topics in information theory and machine learning, see David MacKay's book "[Information Theory, Inference, and Learning Algorithms](https://www.inference.org.uk/itprnn/book.pdf)".
  
  * For reinforcement learning see [Sutton & Barto](http://incompleteideas.net/book/the-book-2nd.html).
  
For the projects related to singular learning theory:

  * S. Watanabe "[Almost all learning machines are singular](http://watanabe-www.math.dis.titech.ac.jp/users/swatanab/foci2007.pdf)", Invited Paper in FOCI2007.
  
  * S. Watanabe "[A Widely Applicable Bayesian Information Criterion](http://www.jmlr.org/papers/volume14/watanabe13a/watanabe13a.pdf)" Journal of Machine Learning Research 14 (2013) 867-897.
  
# Installing software

You can run some tutorials and basic experiments using free hosted Jupyter notebooks such as [Google Colab](https://colab.research.google.com/) however for research you will want to set up your own machine (see below). Operating systems in order of preference for deep learning development are Linux > Mac > Windows. You might have trouble on Windows. For experiments we usually need to use cloud machines, either [AWS](https://aws.amazon.com/) or [GCP](https://cloud.google.com/) (expensive!) or on local clusters such as [Nectar](https://nectar.org.au/) or [Spartan](https://dashboard.hpc.unimelb.edu.au/).

You will need the following

  * Python >= 3.7 (on Mac or Windows you might like to install this via [Anaconda](https://www.anaconda.com/distribution/)).
  * Deep learning libraries [PyTorch](https://pytorch.org/get-started/locally/) or [TensorFlow 2](https://www.tensorflow.org/install) on top of Python, what we use depends on the project.
  * If you have a GPU you want to install drivers and [CUDA](https://developer.nvidia.com/cuda-zone) (a parallel computing platform and programming model developed by NVIDIA for general computing on GPUs) in the way suggested on the webpages for PyTorch and TensorFlow. If you only have a CPU (e.g. you are on a laptop) you can run the same code, but more slowly.

You will run your models either through Jupyter notebooks hosted locally (Anaconda can help with that) or through Python files that you host and run through some other IDE (Susan likes [PyCharm](https://www.jetbrains.com/pycharm/)). Installing all this can be a painful process, when you get stuck **Google your error** and try again. Finally, find some basic PyTorch or TensorFlow tutorial online (e.g. training a small CNN on MNIST) and run it on your local machine to make sure everything works. 

**If you get really stuck, drop into office hours or the Discord** and one us will try to help (see the main page).

# Building your own machine

You can buy complete machines from people like [Lambda labs](https://lambdalabs.com/) but if you feel comfortable building one yourself, you will save a lot of money. There are many guides to relevant hardware online, e.g. Lambda labs helpfully maintains a list of parts on PC Part Picker [here](https://pcpartpicker.com/b/FGP323). You should use their choices of hardware as a sane baseline in your own decision-making. 

In general you should use PC Part Picker to verify that your choices of motherboard, CPU, heatsink and GPU are compatible, and then order somewhere like [Newegg](https://www.newegg.com/global/au-en/). The hardware you want varies with the kind of deep learning you want to do, for instance reinforcement learning is often CPU-heavy, whereas for computer vision tasks you are unlikely to be bottlenecked by your CPU. If you aren't sure, then spend more money on the GPU than the CPU.

*Dan*: Here is my machine, which cost AUD $7000 in May 2019. To give you some idea of how I allocated that between the different components I'll list the prices as of May 2019, but these have changed and you may not be able to buy these precise parts any more. You do not need to spend that much, and you probably want to spend more on your GPU than your CPU (I need lots of threads for RL tasks).

  * **CPU**: AMD Ryzen Threadripper 2990WX 32-core 64-thread 3.0 Ghz (AUD $2500). This is a pretty extravagant part, you probably don't need it.
  * **GPU**: you probably want an NVIDIA card, with as much memory as you can afford. [NVIDIA GeForce RTX 2080](https://www.nvidia.com/en-au/geforce/graphics-cards/rtx-2080/) 8Gb (AUD $1267) (mine was an MSI "SEA HAWK". You do need to pay attention to the fan arrangement and how that will work with your case. Redistributors package the NVIDIA silicon into their own boards, and the boards do vary, so you have to do your homework).
  * **HDD**: Samsung 970 Pro 512Gb PCIe NVMe SSD (AUD $289).
  * **Power supply**: Thermaltake Toughpower 1500W (AUD $414).
  * **Motherboard**: MSI X399 SLI (AUD $453).
  * **RAM**: Corsair 32Gb (AUD $214).
  * **Case**: Lian Li PC-O11AIR ATC mid tower (AUD $207).
  * **CPU cooler**: Noctua NH-U14S TR4-SP3 (not optional!) (AUD $85).
  
I almost bought the Intel Core i9-9980XE instead of the Threadripper, but the extra threads on the latter won me over. The only tricky part of the assembly was the CPU installation and heatsink, but there are good YouTube videos. The heatsink is also so huge that I can't close the case, so if you want to reproduce that exact build: buy a wider case! Air cooling seems fine. You'll need a monitor, keyboard, wireless networking card etc. but I'm sure you can handle that. You'll want to install Linux on the machine. I run mine headless, connected via Ethernet to an iMac. The linux machine starts a Jupyter server on boot, and I run experiments through a browser on the iMac and SSH.

I did a lot of homework before buying these parts, you should too. A good starting point is [Tim Dettmers](https://timdettmers.com/) homepage, find his most recent GPU performance comparisons. Lambda labs also publish blog posts with GPU comparisons. Not all GPUs are created equal when it comes to deep learning, so be careful and unless you know what you are doing stick with NVIDIA cards that are recommended by people doing deep learning.

**Again, if you want help feel free to drop into office hours or the Discord.**
