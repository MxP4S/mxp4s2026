---
layout: default
title: Speakers and Talks
---

# Speakers and talks

## Mixed Precision Math Unlocks Accelerated Computing
Piotr Luszczek, MIT Lincoln Lab and University of Tennessee, Knoxville, USA

### Abstract
Modern GPU hardware continues to deliver increasing levels of performance that are the computational foundation of Generative AI and large language models (LLMs). A key driver of this performance has been mixed-precision arithmetic that enables higher performance at lower precision.  The availability of high-performance mixed-precision hardware has triggered a revolution in new mixed-precision algorithms. In this talk, we will discuss the underlying forces driving these new capabilities. We will also show ways to harness the recent hardware advances to enable accurate computations while leveraging the power of mixed-precision computational hardware.

### About the speaker
Piotr Luszczek is a Technical Staff at MiT Lincoln Lab and Research Associate Professor in the Tickle College of Engineering at the University of Tennessee and a member of the Innovative Computing Laboratory. He has a long record of research and software development spanning benchmarking, numerical linear algebra for high-performance computing, automatic performance tuning for hardware accelerators, and stochastic models of performance metrics. His mixed-precision work goes back nearly 20 years with a new look at mixed-precision iterative refinement that is now implemented in nearly all modern numerical linear algebra libraries. He contributed to inner-outer iterative solvers that also exploited performance of lower-precision floating-point arithmetic. More recently, he used autotuning across multiple precisions and introduced a new factorization algorithm with scaling that maintains improved accuracy for reduced-precision computations. Piotr serves as Editor in Chief of ACM TOMS journal and on the Operations Committee of TOP500. He has been organizing and chairing community events around the mixed-precision topics for half a decade including BOFs, panels, tutorials, and workshops in affiliation with HPC and supercomputing venues including CUG, HPEC, ISC, and SC.

## Right Precision, Right Place: Rethinking HPC Applications with Adaptive Mixed Precision
Hatem Ltaief, King Abdullah University of Science and Technology, Saudi Arabia

### Abstract
The future of large-scale simulations is increasingly tied to hardware features originally designed for AI workloads—especially low-precision arithmetic. Modern GPUs embody this shift, delivering substantial speedups through reduced-precision computations that lower execution time, shrink memory footprints, and cut energy consumption. Building on these capabilities, we design fast mixed-precision linear algebra algorithms that adaptively choose the right precision at the right moment. Beyond computation, we extend this adaptivity to data storage, enabling mixed-precision representations that dynamically adjust to the needs of memory-bound applications. This approach significantly reduces data movement—now a dominant performance bottleneck—while preserving high accuracy only where it truly matters. Our dynamic precision-conversion strategy maintains application-level numerical reliability while improving overall efficiency. This talk will demonstrate how these techniques reshape computational performance for geospatial statisticians and geophysicists, with far-reaching benefits for environmental computational statistics, seismic imaging, and beyond.

### About the speaker
Dr. Hatem Ltaief is a Principal Research Scientist in the Computer Electrical and Mathematical Sciences and Engineering Division at KAUST. His research focuses on mixed-precision algorithms, low-rank matrix computations, parallel programming models, and performance optimizations for high-performance computing (HPC) systems equipped with hardware accelerators. He has contributed to integrating numerical algorithms into major scientific libraries including NVIDIA cuBLAS and Cray LibSci. Collaborating with domain scientists across diverse fields such as ground-based astronomy, geospatial statistics, computational chemistry, bioinformatics, and geophysics, Dr. Ltaief helps their scientific applications meet the exascale computing challenges.
Dr. Ltaief has co-authored all four of KAUST Gordon Bell finalist papers since 2022. In November 2024, he received the prestigious ACM Gordon Bell Prize (shared) in climate modeling for his contributions to developing an exascale climate emulator. This groundbreaking work addresses the computational and storage demands of high-resolution Earth System Model simulations and was achieved in collaboration with a distinguished team of experts.
He earned his engineering degree from Polytech Lyon at the University of Claude Bernard Lyon I in 2003, followed by an M.Sc. in applied mathematics in 2004 and a Ph.D. in computer science from the University of Houston in 2008. Before joining KAUST, Dr. Ltaief served as a research scientist at the Innovative Computing Laboratory in Knoxville Tennessee.
Dr. Ltaief has received multiple accolades including the Best Paper Award at the ACM PASC conference in 2018 and the Gauss Award for Best Paper at the ISC Conference in 2020. He currently serves as co-Editor-in-Chief of the ACM Transactions on Mathematical Software and as an Associate Editor-in-Chief of the Elsevier Parallel Computing Journal.

## Ozaki Schemes and Applications to Numerical Linear Algebra: Benchmark Results
Katsuhisa Ozaki, Shibaura Institute of Technology, Japan

### Abstract
In modern computing environments such as GPUs, where low-precision arithmetic is significantly faster than double precision, the Ozaki scheme has been proposed as an approach for emulating FP64-equivalent matrix multiplication.
At the beginning of the talk, we briefly introduce two variants of the Ozaki scheme: Ozaki Scheme I, which generates slices of floating-point numbers, and Ozaki Scheme II, which is based on the Chinese Remainder Theorem. We then discuss efficient ways of using Ozaki schemes and present benchmark results when they are applied to several representative problems in numerical linear algebra.
This is joint work with Yuki Uchino and Toshiyuki Imamura.

### About the speaker
Dr. Katsuhisa Ozaki is a Professor in the Department of Mathematical Sciences at Shibaura Institute of Technology, Japan. His research interests include floating-point arithmetic, numerical linear algebra, and verified numerical computation. He is particularly known for his work on high-reliability numerical methods for matrix computations, including the Ozaki Scheme. He has previously held appointments at Waseda University.

## Dispelling Many of the Perceived Challenges in Adopting the Ozaki Scheme in Scientific Computing
Harun Bayraktar, NVIDIA, USA

### Abstract
Modern GPU architectures deliver orders-of-magnitude more throughput in low-precision formats than in FP64, yet many scientific computing applications demand double-precision accuracy. The Ozaki scheme — which decomposes high-precision matrix multiplications into sequences of low-precision operations on tensor cores — bridges this gap, and is shipping in cuBLAS for FP64 GEMMs since the fall of 2025. Despite demonstrated speedups over native FP64 on NVIDIA Blackwell GPUs, adoption of the Ozaki scheme is hampered by a set of challenges that are erroneously perceived to be insurmountable. In this talk we will confront these one by one while also highlighting any remaining real challenges. We will also show how the flexibility in precision in the Ozaki-scheme is being leveraged to deliver significant performance gains in scientific computing domains such as computational quantum chemistry.

### About the speaker
Since joining NVIDIA in 2017, Harun Bayraktar has been leading the Math Libraries organization which builds software to help accelerate applications in science, engineering, Quantum Computing, and artificial intelligence (AI). Prior to joining NVIDIA, Harun’s career path includes development of commercial HPC computational mechanics software and physics-based simulation research and technology development for advanced composites materials in aerospace. Harun holds a PhD in mechanical engineering from UC Berkeley.

## Inexact yet Accurate: Unlocking low precision for efficient quantum modelling of materials at scale
Phani Motamarri, Indian Institute of Science, India

### Abstract
Modern GPU architectures offer dramatically higher throughput for low-precision arithmetic, yet eigensolvers in scientific simulations have struggled to exploit this capability without sacrificing accuracy. We present an eigensolver R-ChFSI, a residual-based reformulation of Chebyshev Filtered Subspace Iteration (ChFSI) provably tolerant to inexact matrix–vector products. By expressing the Chebyshev recurrence in terms of residuals rather than eigenvector estimates, R-ChFSI naturally accommodates reduced-precision arithmetic (FP32, TF32) in the filtering step, lossy compression formats for inter-process communication in distributed sparse matrix-vector products, and approximate inverses for generalized eigenproblems,. Large-scale experiments on GPU accelerators using finite-element discretized generalized eigenproblems arising in quantum modelling of materials, involving up to 85 million grid points and 13,500 eigenpairs, show that R-ChFSI achieves residual norms orders of magnitude smaller than standard ChFSI under inexactness, while delivering substantial performance gains. This work highlights a practical pathway to precision-aware eigensolvers enabling accurate and scalable quantum simulations.

### About the speaker
Dr. Phani Motamarri is an assistant professor in the Department of Computational and Data Sciences and the principal investigator of the MATRIX lab at the Indian Institute of Science. He completed his PhD in 2014 at the University of Michigan, Ann Arbor, USA. He has won several awards, including the ACM Gordon Bell prize in 2023. His research interests include mathematical techniques and hardware-aware algorithms for quantum modelling of materials on emerging computing architectures, quantum modeling of structural and functional materials, multi-scale modelling methodologies, machine learning frameworks to accelerate materials discovery, quantum computing based algorithms for scientific computations geared towards quantum-centric supercomputing, finite-element methods, numerical analysis, and large-scale scientific software development. He is one of the lead developers of open source code DFT-FE, a massively parallel finite-element code for density functional theory calculations.

## Using Numerical Profiling to Determine Where Mixed Precision is Usable in Multiphase Flow Simulations
Akash Dhruv, Argonne National Laboratory, USA

### Abstract
Modern HPC platforms offer growing capacity for low-precision arithmetic, yet scientific applications default to double precision due to concerns about accuracy and stability. Identifying where reduced precision is safe requires more than theoretical analysis. Practical experimentation guided by the structure of the application is essential in many circumstances. In this talk, we present results from applying RAPTOR, a practical numerical profiling tool, to multiphase flow simulations built with Flash-X. By selectively truncating precision in distinct physical components, we examine how mixed precision affects individual simulation modules and overall solution fidelity. Our experiments reveal that the impact of precision reduction is highly problem- and regime-dependent: refinement level, solver type, and physics coupling all influence where truncation is tolerable. These findings offer practical guidance for adopting adaptive precision in composed multiphysics applications.

### About the speaker
Akash Dhruv is an Assistant Computational Scientist at Argonne National Laboratory, where he works on the development of Flash-X multiphysics simulation software, AI-driven software engineering, and surrogate modeling for multiphase flows. In collaboration with researchers at RIKEN and ETH Zurich, he has explored mixed-precision strategies for scientific simulations using numerical profiling tools. He holds expertise in incompressible flow solvers and adaptive mesh refinement frameworks.

## Do We Need FP64 for Supercomputing? What can we do if we don’t have it?
Al Geist, Oak Ridge National Laboratory, USA

### Abstract
The talk will explore three main reasons we have FP64 in supercomputing: To reduce error build up, maintain numerical accuracy, and have range to represent the science. By exploring these reasons we can better understand where lower precision calculations can be exploited and the different methods for it to be incorporated into science applications. Finally, we discuss what can be done if FP64 is no longer supported in future computing chips.

### About the speaker
The talk will explore three main reasons we have FP64 in supercomputing: To reduce error build up, maintain numerical accuracy, and have range to represent the science. By exploring these reasons we can better understand where lower precision calculations can be exploited and the different methods for it to be incorporated into science applications. Finally, we discuss what can be done if FP64 is no longer supported in future computing chips.
