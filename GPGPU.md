# GPGPU

* [Ask HN: Best place to learn GPU programing?](https://news.ycombinator.com/item?id=11999892)

* [An Even Easier Introduction to CUDA](https://devblogs.nvidia.com/parallelforall/even-easier-introduction-cuda/) ([HN](https://news.ycombinator.com/item?id=13565763))

* [Optimizing CUDA: Warps, Threads and Blocks](https://malagastockholm.wordpress.com/2013/01/13/optimizing-cuda-warps-threads-and-blocks/)

* [What is the best option for GPU programming?](https://www.researchgate.net/post/What_is_the_best_option_for_GPU_programming) careful: 2014

## Software

* [XLA](https://www.tensorflow.org/versions/master/experimental/xla/)
  *"a domain-specific compiler for linear algebra that optimizes
  TensorFlow computations"* (according to
  [HN](https://news.ycombinator.com/item?id=13568431) a jit (that
  compiles directly to CUDA assemblies?))

* [Parallel Thread Execution (PTX)](https://en.wikipedia.org/wiki/Parallel_Thread_Execution), 
  [NVIDIA's CUDA/OpenCL PTX Back-End In LLVM 3.2](http://www.phoronix.com/scan.php?page=news_item&px=MTI1NDU) (LLVM had a "PTX" in the past, and now a "NVPTX" backend that was open sourced by Nvidia themselves)

* [Compiling CUDA with clang](http://llvm.org/docs/CompileCudaWithLLVM.html) (some discussion on [HN](https://news.ycombinator.com/item?id=14309756))

* On Python:

    * [GPGPU.org: Python](http://gpgpu.org/tag/python)
    * ([GPGPU programming in Python (Stackoverflow)](https://stackoverflow.com/questions/3455608/gpgpu-programming-in-python), careful: 2011!)
        * CLyther attempts to abstract everything out. You write the host-side code in Python. You write the device-side code in a subset of Python (in a similar way to Cython). This is very high level and easy-to-use. 
        * PyOpenCL is a comparatively low-level binding to the OpenCL API from Python. Device-side code is written in OpenCL's subset of C99. It gives you full access to and full control of OpenCL. Very little is abstracted away. 
    * [CLyther](https://srossross.github.io/Clyther/) *"is a just-in-time specialization engine for OpenCL. The main entry points for CLyther are its clyther.task and clyther.kernel decorators. Once a function is decorated with one of these the function will be compiled to OpenCL when called."*
        * *"Warning This is a brand new version of CLyther. I have not released this yet. If you do decide to use it then please think about Contributing."*, although the code seems to be on [Github](https://github.com/srossross/Clyther/).
    * ([PyGPU - Python for the GPU](http://fileadmin.cs.lth.se/cs/Personal/Calle_Lejdfors/pygpu/) *"is a compiler that lets you write image processing programs in Python that execute on the graphics processing unit (GPU) present in modern graphics cards."* But: OpenGL only, not GPGPU?)
    * [GPU Accelerated Computing with Python (nvidia.com)](https://developer.nvidia.com/how-to-cuda-python): *"Using the NumbaPro Python compiler, which is part of the Anaconda Accelerate package from Continuum Analytics, you get the best of both worlds: rapid iterative development and all other benefits of Python combined with the speed of a compiled language targeting both CPUs and NVIDIA GPUs."*
        * [NumbaPro / Quick Start](https://docs.continuum.io/numbapro/quickstart)
    * [PyCUDA](https://mathema.tician.de/software/pycuda/) *"lets you access Nvidia‘s CUDA parallel computation API from Python. Several wrappers of the CUDA API already exist–so what's so special about PyCUDA?"* (Just API, have to write in CUDA, right?)
    * [An introduction to CUDA using Python (PDF)](http://www.tsc.uc3m.es/~miguel/MLG/adjuntos/slidesCUDA.pdf) (haven't looked at it)
    * [Py-Videocore: Python Library for GPGPU on Raspberry Pi (HN)](https://news.ycombinator.com/item?id=10797603) (*"Although VC4 is capable enough to run simple GLSL shaders, it is not possible to compile a generic C (or OpenCL) code efficiently."*)

* On Rust:

    * [RustGPU](https://github.com/eholk/RustGPU), by Eric Holk who also created 
      [Harlan](https://github.com/eholk/harlan).
      [Compiling Rust for GPUs (Eric Holk, 2012)](http://blog.theincredibleholk.org/blog/2012/12/05/compiling-rust-for-gpus/) ([HN](https://news.ycombinator.com/item?id=6933912)).
    * [ocl](https://github.com/cogciprocate/ocl)
    * [GPU Programming using Rust? (Reddit)](https://www.reddit.com/r/rust/comments/4dnq0h/gpu_programming_using_rust/)
        * [Rust wrapper for ArrayFire](https://github.com/arrayfire/arrayfire-rust) 
            * [ArrayFire: a general purpose GPU library](https://github.com/arrayfire/arrayfire)
        * [rust-opencl - OpenCL bindings for Rust](https://github.com/luqmana/rust-opencl)
        * [Vulkano - Rust wrapper around the Vulkan graphics API](https://github.com/tomaka/vulkano)
        * [SPIR - The first open standard intermediate language for parallel compute and graphics](https://www.khronos.org/spir) (*"initially developed for use by OpenCL and SPIR versions 1.2 and 2.0 were based on LLVM. SPIR has now evolved into a true cross-API standard that is fully defined by Khronos with native support for shader and kernel features – called SPIR-V."*, *"For developers, using SPIR-V means that kernel source code no longer has to be directly exposed, kernel load times can be accelerated and developers can choose the use of a common language front-end, improving kernel reliability and portability across multiple hardware implementations."*)
    * ([Single-source GPU support (rust-lang.org)](https://internals.rust-lang.org/t/single-source-gpu-support/898) ideas (deprecated))

* On Julia:

    * [JuliaGPU](https://github.com/JuliaGPU) Github organization:
        * [CUDAnative.jl](https://github.com/JuliaGPU/CUDAnative.jl)
            * There was a talk [here](https://skillsmatter.com/meetups/8776-london-julia-users-group) and was recorded, should ask Skillsmatter where the video is.
        * OpenCL.jl (OpenCL Julia bindings)
        * CUDArt.jl (Julia wrapper for CUDA runtime API)
        * CUDAdrv.jl (A Julia wrapper for the CUDA driver API)
        * Cuda: CUBLAS.jl, CUSPARSE.jl, CUSOLVER.jl, CUFFT.jl, CURAND.jl, CUDAnativelib.jl, VulkanCore.jl, CUDNN.jl
        * OpenCL: CLBLAS.jl, CLFFT.jl
        * SPIRV.jl
        * GPUArrays.jl (Array operations defined for all kind of GPU backends)
        * (LLVM.jl, Cxx.jl, Clang.jl)
        * HSA.jl (Julia Bindings for the HSA Runtime) -- ?
        * Vulkan.jl
        * ArrayFire.jl 
    * [Options for GPU computing in Julia](https://stackoverflow.com/questions/38224609/options-for-gpu-computing-in-julia) (2016)

* On Erlang:

    * [GPGPU Programming Erlang (erlang-factory.com)](http://www.erlang-factory.com/upload/presentations/356/KevinSmith.pdf)
    * [Machine Learning in Erlang and CUDA](http://www.vas.io/blog/2013/03/23/machine-learning-in-erlang-and-cuda/) (2013)
        * *"I decided to create another project and so - the NumEr was born"*
    * [cl](https://github.com/tonyrog/cl) (OpenCL binding)
    * [NumEr](https://github.com/vascokk/NumEr) - Numeric Erlang - vector and matrix operations with CUDA. Heavily inspired by [Pteracuda](https://github.com/kevsmith/pteracuda) (= Framework for using CUDA from Erlang)

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
        * *"The SPOC library enables the detection and use of GPGPU devices with OCaml using Cuda and OpenCL."*
        * *"There is also a camlp4 syntax extension to handle external Cuda or OpenCL kernels, as well as a DSL (called Sarek) to express GPGPU kernels from the OCaml code."*
    * random links:
        * [High-Performance GPGPU Programming with OCaml (hgpu.org)](http://hgpu.org/?p=10694) (2013)
        * [GPGPU Composition with OCaml](http://dl.acm.org/citation.cfm?id=2627379) (2014)
        * [Ocaml for scientific compution: why not? (Reddit)](https://www.reddit.com/r/ocaml/comments/3cwn7i/ocaml_for_scientific_compution_why_not/) (2016)

* On F#:

    * [Use F# for GPU Programming (fsharp.org)](http://fsharp.org/use/gpu/)
        * [Alea GPU](http://www.aleagpu.com/release/3_0_3/doc/), GPU parallel-for and parallel aggregate, Automatic memory management to move data to and from the GPU, GPU scripting for rapid prototyping in the interactive console, "GPU JIT compilation" (they will just mean without restarting the program), on CUDA. Seems there's no compiler from F# though? Or is it: *"It is a full compiler based on F# and LLVM to generate highly optimized GPU code."*. 
            * Docs say: *"Alea GPU natively supports all .NET languages, including C#, F# and VB. It compiles .NET code directly to GPU code without first generating intermediate C or C++."* (So, not a subset of the source language, how well does that work? *"There is no performance compromise, compiled code runs as fast as CUDA C/C++."*, is that a marketing lie?)
            * Commercial, with a reduced-functionality Community Edition
        * [Brahma.FSharp](http://yaccconstructor.github.io/Brahma.FSharp/), *"Basic aim is to translate native F# code to OpenCL with minimization of different wrappers and custom types"*, via OpenCL
            * *"library for F# quotations to OpenCL translation"*
            * Eclipse Public License
            * latest commit 2017
        * [FSCL](https://github.com/FSCL/FSCL.Compiler), *"a source-to-source compiler that translates quoted F# function calls and other contructs into valid C99 OpenCL kernel sources"*
            * [project wiki](https://github.com/FSCL/FSCL.Compiler/wiki): *"the FSCL Compiler generates OpenCL C99 kernel source code out of F# collection functions and F# special functions/methods/lambdas"*
            * Apache License 2.0
            * latest commit 2016
        * [GpuLINQ](https://github.com/nessos/GpuLinq/), *"an open source F#/C# LINQ-to-OpenCL compiler"*
            * Apache License 2.0
            * latest commit 2015
    
* On Clojure:

    * [ClojureCL (uncomplicate.org)](http://clojurecl.uncomplicate.org/) *"supports GPUs, CPUs, and other accelerators. Sane interface and functions that fit into functional style while still respecting the reality of number crunching with OpenCL."*
        * but is actually only an OpenCL wrapper (see [Clojure is Not Afraid of the GPU - Dragan Djuric (2016) (youtube)](https://www.youtube.com/watch?v=bEOOYbscyTs))
    * [ClojureCUDA (uncomplicate.org)](http://clojurecuda.uncomplicate.org/) (same design and text templates as ClojureCL, same domain, same author)
    * [Neanderthal (uncomplicate.org)](http://neanderthal.uncomplicate.org/) (dito)
        * [CUDA and cuBLAS GPU matrices in Clojure](http://dragan.rocks/articles/17/CUDA-and-cuBLAS-GPU-matrices-in-Clojure) ([HN](https://news.ycombinator.com/item?id=14386291)): *"I've added a new engine to Neanderthal that gives us the full speed of Nvidia's CUDA based cuBLAS library."*; *"\[...\] One major thing was still left untapped though: Nvidia's proprietary CUDA-based libraries that require Nvidia's proprietary and closed source CUDA technology that is also tied to the Nvidia hardware."* *"\[With OpenCL-based Neanderthal engine got\] 60% utilization, which is quite impressive for a one-man team working part-time! \[...\] with the CUDA-based engine \[...\] almost at the specification maximum of the hardware."*; *"I expect to integrate at least cuSPARSE and cuSOLVER into Neanderthal, and I'm eyeing cuDNN as an engine for a possible deep learning library."*
    * [Bayadera](https://github.com/uncomplicate/bayadera), A Clojure Library for Bayesian Data Analysis and Machine Learning on the GPU. (Same author, Dragan Djuric.)
        * [Clojure is Not Afraid of the GPU - Dragan Djuric (youtube.com) (Reddit)](https://www.reddit.com/r/Clojure/comments/5dirtc/clojure_is_not_afraid_of_the_gpu_dragan_djuric/) (Jan 2017) *"Currently \[Bayadera\] requires an OpenCL 2.0 device, which practically means a recent (2-3 years) discrete AMD GPU."*

* On Fortran:

    * [CUDA FORTRAN](https://developer.nvidia.com/cuda-fortran): *"NVIDIA worked with The Portland Group (PGI) to develop a CUDA Fortran Compiler that provides Fortran language support for NVIDIA’s CUDA-enabled GPUs. Fortran developers with data parallel problems will be able to use this compiler to harness the massive parallel computing capability of NVIDIA GPUs to create high performance applications for scientific computing."*
    * [GPGPU: Fortran (gpgpu.org)](http://gpgpu.org/tag/fortran)
        * [Performance Portable Parallel Programming – Target CUDA and OpenMP in a Unified Codebase](http://gpgpu.org/2014/08/14/performance-portable-parallel-programming-target-cuda-and-openmp-in-a-unified-codebase)
            * [Hybrid-Fortran (Github)](https://github.com/muellermichel/Hybrid-Fortran)


## Hardware

* [NVIDIA GeForce GTX 1080 .. Performance Faster Than Titan X and 980 SLI](http://wccftech.com/nvidia-geforce-gtx-1080-launch/), [HN](https://news.ycombinator.com/item?id=11648110); also:
  * [8x Nvidia GTX 1080 Hashcat Benchmarks](https://gist.github.com/epixoip/a83d38f412b4737e99bbef804a270c40) ([HN](https://news.ycombinator.com/item?id=11852958))

* ([Considerations when setting up deep learning hardware](http://www.pyimagesearch.com/2016/06/13/considerations-when-setting-up-deep-learning-hardware/) ([HN](https://news.ycombinator.com/item?id=11894094)), overpriced, HN discussion more interesting.)

* [Deep Learning GPU Benchmarks](http://add-for.com/deep-learning-benchmarks/) ([HN](https://news.ycombinator.com/item?id=12693745))

* [Using GPUs to Speed Through the 1.2B Record Taxi Dataset (mapd.com)](https://www.mapd.com/blog/2016/10/13/speeding-through-nyc-the-billion-row-nyc-taxi-dataset/) ([HN](https://news.ycombinator.com/item?id=12714448), "For Graphistry's GPU platform, we suggest our users to go with server-grade GPUs because they get (a) more memory and (b) great multitenancy. So using MapD as a personal system is an expensive use of resources, but when a system is architected and billed as an elastic, multitenant system, total cost of ownership for a team is less."; "If you really have a tight budget and need to use gamer cards as workstation cards (...), find yourself some aftermarket coolers, preferably liquid cooling.")

* [Volta: Advanced Data Center GPU](https://devblogs.nvidia.com/parallelforall/inside-volta/) ([HN](https://news.ycombinator.com/item?id=14309756))

