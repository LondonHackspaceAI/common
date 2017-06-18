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

* [Compiling CUDA with clang](http://llvm.org/docs/CompileCudaWithLLVM.html) (some discussion on [HN](https://news.ycombinator.com/item?id=14309756))

* [CUDA and cuBLAS GPU matrices in Clojure](http://dragan.rocks/articles/17/CUDA-and-cuBLAS-GPU-matrices-in-Clojure) ([HN](https://news.ycombinator.com/item?id=14386291))

* On Haskell:

    * [Data.Array.Accelerate](https://hackage.haskell.org/package/accelerate) defines an embedded array language for computations for high-performance computing in Haskell. Computations on multi-dimensional, regular arrays are expressed in the form of parameterised collective operations, such as maps, reductions, and permutations.
        * modules:
            * accelerate-llvm-native: Backend supporting parallel execution on multicore CPUs. 
            * accelerate-llvm-ptx: Backend supporting parallel execution on CUDA-capable NVIDIA GPUs. Requires a GPU with compute capability 2.0 or greater. 
            * accelerate-cuda: Backend targeting CUDA-enabled NVIDIA GPUs. Requires a GPU with compute compatibility 1.2 or greater (deprecated)
            * accelerate-io: Fast conversions between Accelerate arrays and other array formats (including vector and repa).
            * accelerate-fft: Discrete Fourier transforms, with FFI bindings to optimised implementations. 
        * [GPGPU Programming in Haskell with Accelerate (speakerdeck.com)](https://speakerdeck.com/tmcdonell/gpgpu-programming-in-haskell-with-accelerate) (2013)
        * [Github](https://github.com/AccelerateHS/accelerate)
    * [GPU (wiki.haskell.org)](https://wiki.haskell.org/GPU)
    
* On OCaml:

    * [spoc (stream processing with OCaml)](http://mathiasbourgoin.github.io/SPOC/)
    * random links:
        * [High-Performance GPGPU Programming with OCaml (hgpu.org)](http://hgpu.org/?p=10694) (2013)
        * [GPGPU Composition with OCaml](http://dl.acm.org/citation.cfm?id=2627379) (2014)
        * [Ocaml for scientific compution: why not? (Reddit)](https://www.reddit.com/r/ocaml/comments/3cwn7i/ocaml_for_scientific_compution_why_not/) (2016)

* On F#:

    * [Use F# for GPU Programming (fsharp.org)](http://fsharp.org/use/gpu/)
    

## Hardware

* [NVIDIA GeForce GTX 1080 .. Performance Faster Than Titan X and 980 SLI](http://wccftech.com/nvidia-geforce-gtx-1080-launch/), [HN](https://news.ycombinator.com/item?id=11648110); also:
  * [8x Nvidia GTX 1080 Hashcat Benchmarks](https://gist.github.com/epixoip/a83d38f412b4737e99bbef804a270c40) ([HN](https://news.ycombinator.com/item?id=11852958))

* ([Considerations when setting up deep learning hardware](http://www.pyimagesearch.com/2016/06/13/considerations-when-setting-up-deep-learning-hardware/) ([HN](https://news.ycombinator.com/item?id=11894094)), overpriced, HN discussion more interesting.)

* [Deep Learning GPU Benchmarks](http://add-for.com/deep-learning-benchmarks/) ([HN](https://news.ycombinator.com/item?id=12693745))

* [Using GPUs to Speed Through the 1.2B Record Taxi Dataset (mapd.com)](https://www.mapd.com/blog/2016/10/13/speeding-through-nyc-the-billion-row-nyc-taxi-dataset/) ([HN](https://news.ycombinator.com/item?id=12714448), "For Graphistry's GPU platform, we suggest our users to go with server-grade GPUs because they get (a) more memory and (b) great multitenancy. So using MapD as a personal system is an expensive use of resources, but when a system is architected and billed as an elastic, multitenant system, total cost of ownership for a team is less."; "If you really have a tight budget and need to use gamer cards as workstation cards (...), find yourself some aftermarket coolers, preferably liquid cooling.")

* [Volta: Advanced Data Center GPU](https://devblogs.nvidia.com/parallelforall/inside-volta/) ([HN](https://news.ycombinator.com/item?id=14309756))

