# GPGPU

* [Ask HN: Best place to learn GPU programing?](https://news.ycombinator.com/item?id=11999892)

* [An Even Easier Introduction to CUDA](https://devblogs.nvidia.com/parallelforall/even-easier-introduction-cuda/) ([HN](https://news.ycombinator.com/item?id=13565763))

## Software

* ([ClojureCL - a Clojure library for parallel computations with OpenCL
  2.0](http://clojurecl.uncomplicate.org/)?, but doesn't say what it
  actually does, and
  [Neanderthal](http://neanderthal.uncomplicate.org/) claims speed "in
  Clojure" but then the
  [project](https://github.com/uncomplicate/neanderthal) says it is
  "based on" ATLAS. WTF?)

* [XLA](https://www.tensorflow.org/versions/master/experimental/xla/)
  *"a domain-specific compiler for linear algebra that optimizes
  TensorFlow computations"* (according to
  [HN](https://news.ycombinator.com/item?id=13568431) a jit (that
  compiles directly to CUDA assemblies?))

* [Parallel Thread Execution (PTX)](https://en.wikipedia.org/wiki/Parallel_Thread_Execution), 
  [NVIDIA's CUDA/OpenCL PTX Back-End In LLVM 3.2](http://www.phoronix.com/scan.php?page=news_item&px=MTI1NDU) (LLVM had a "PTX" in the past, and now a "NVPTX" backend that was open sourced by Nvidia themselves)

## Hardware

* [NVIDIA GeForce GTX 1080 .. Performance Faster Than Titan X and 980 SLI](http://wccftech.com/nvidia-geforce-gtx-1080-launch/), [HN](https://news.ycombinator.com/item?id=11648110); also:
  * [8x Nvidia GTX 1080 Hashcat Benchmarks](https://gist.github.com/epixoip/a83d38f412b4737e99bbef804a270c40) ([HN](https://news.ycombinator.com/item?id=11852958))

* ([Considerations when setting up deep learning hardware](http://www.pyimagesearch.com/2016/06/13/considerations-when-setting-up-deep-learning-hardware/) ([HN](https://news.ycombinator.com/item?id=11894094)), overpriced, HN discussion more interesting.)

* [Deep Learning GPU Benchmarks](http://add-for.com/deep-learning-benchmarks/) ([HN](https://news.ycombinator.com/item?id=12693745))

* [Using GPUs to Speed Through the 1.2B Record Taxi Dataset (mapd.com)](https://www.mapd.com/blog/2016/10/13/speeding-through-nyc-the-billion-row-nyc-taxi-dataset/) ([HN](https://news.ycombinator.com/item?id=12714448), "For Graphistry's GPU platform, we suggest our users to go with server-grade GPUs because they get (a) more memory and (b) great multitenancy. So using MapD as a personal system is an expensive use of resources, but when a system is architected and billed as an elastic, multitenant system, total cost of ownership for a team is less."; "If you really have a tight budget and need to use gamer cards as workstation cards (...), find yourself some aftermarket coolers, preferably liquid cooling.")

