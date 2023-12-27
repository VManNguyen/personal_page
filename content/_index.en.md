+++
title = "Van Man Nguyen"
author = "Van Man Nguyen"
description = "Personal page of Van Man Nguyen, R&D engineer and techhnical expert in HPC and MPI at Eviden. PhD in computer science on compile-time analysis and optimization of MPI codes"
template = "page-cv-en.html"

+++
## Abstract
My research interest is on the analysis and optimization of MPI codes at
compile-time. It allows us to detect programming errors as soon as possible
in the development cycle of an HPC simulation. These analyses enable us the
static detection of race conditions and deadlocks. The results from these
analyses can then be leveraged to optimize MPI programs. For instance, we can
use the matching information of MPI nonblocking calls and their dependencies to
expose overlapping potential, thus helping in reducing the execution time of
HPC simulations.

I defended my PhD in december 2022. It is about the analysis and optimization of
MPI nonblocking calls in HPC codes.

I am now an *R&D engineer* and *technical expert* at Eviden. More precisely, I work
on MPI implementations and the analysis of MPI One-Sided communications.

**Keywords**: Compilation, MPI, Static Analysis, Code optimization

## Contact
- email : van-man [point] nguyen [arobase] eviden [point] com
- [github](https://github.com/VManNguyen), mostly snippets of personal projects
- [linkedin](https://www.linkedin.com/in/van-man-nguyen-126893140/)


## Supervision
- 2023 - Now: Radjasouria Vinayagame, *PhD student*, with Emmanuelle Saillard 
    (co-director, Inria Bordeaux), Samuel Thibault (co-director, Inria Bordeaux), 
    and Marc Sergent (co-supervisor, Eviden).

## Teaching
- 2020 - 2023, Teacher assistant: **Advanced Compilation**, *3rd year ENSIIE (M2 equivalent)*.
    Building a GCC compilation pass to detect potential deadlocks related to an erroneous use 
    of MPI collective calls. Handling of the CFG, and the concept of dominators and post-dominators
    of a vertex.

## Publications
### PhD
> [Compile-time Validation and Optimization of MPI Nonblocking Communications](https://www.theses.fr/2022BORD0415)

> High-Performance Computation (HPC) clusters are made of multiple computing 
    and memory storage units (or nodes) interconnected with a high performance 
    network. Such architecture is called”distributed”. Computations are spread 
    over these nodes which each work on a subset of the whole simulation, 
    leading to increased performance thanks to parallelism. The results then 
    needs to be shared between the nodes to carry out the computations, which 
    is source of latencies. The Message Passing Interface (MPI) is the most 
    widely used solution in HPC to implement these exchanges. It defines 
    multiple flavors of communications, including point-to-point and collective 
    communications. They exist in three versions: blocking, nonblocking, and 
    persistent. Nonblocking communications allow the overlapping of 
    communications by computations, thus leading to a better use of computing 
    resources and reduced time to results. Yet this version of the 
    communications, whose collective forms were added to the interface by its 
    third major version in 2012, are harder to use because of their composition 
    and offer less security mechanisms. Developers are more prone to commit 
    programming errors which can lead to deadlocks or data corruption. 
    Consequently, nonblocking communications, and more specifically the 
    collective forms, are still not widely used to create overlapping 
    opportunities. The goal of this study is the development of methods to help 
    developers in using these communications. First, we propose a method to 
    match nonblocking calls at compile-time and to detect programming errors 
    involving those using information on the control flow and the data flow. 
    Secondly, we propose a method to automatically transform existing blocking 
    calls into their nonblocking versions. This method then reorganizes the code 
    of a function by moving the dependencies of communications in order to 
    maximize the length of overlapping intervals. It is also applied on existing 
    nonblocking calls using the matching information found by the verification 
    process. Finally, we build upon the limitations of the automatic approach to 
    propose a method to improve the overlapping potential of MPI programs by 
    identifying the boundaries of overlapping intervals and suggesting code 
    modification to developers. The three processes we proposed have been tested 
    on several benchmarks, including miniapps and CORAL codes.

- PhD prepared between november 2019 and december 2022, at CEA and Inria Bordeaux.
- Co-directed by Denis Barthou (Inria Bordeaux), and Patrick Carribault (CEA).
- Co-supervised by Emmanuelle Saillard (Inria Bordeaux), and Julien Jaeger (CEA).
- Defended on the 16th of december 2022, at the University of Bordeaux.

### Main author
- Compas 2021 (poster), *Van Man Nguyen, Emmanuelle Saillard, Julien Jaeger, Patrick Carribault, and Denis Barthou*: **Tools for Efficient MPI Nonblocking Communications**
- [Correctness 2020](https://dx.doi.org/10.1109/Correctness51934.2020.00009), *Van Man Nguyen, Emmanuelle Saillard, Julien Jaeger, Patrick Carribault, and Denis Barthou*: **PARCOACH Extension for Static MPI Nonblocking and Persistent Communication Validation** [[hal](https://hal.science/cea-03014171v1)]
- [C3PO 2020](https://dx.doi.org/10.1007/978-3-030-59851-8_4), *Van Man Nguyen, Emmanuelle Saillard, Julien Jaeger, Patrick Carribault, and Denis Barthou*: **Automatic Code Motion to Extend MPI Nonblocking Overlap Window** [[hal](https://hal.science/cea-03010533v1)]

### Co-author
- [Correctness 2023](https://dx.doi.org/10.1145/3624062.3624086), *Radjasouria Vinayagame, Van Man Nguyen, Marc Sergent, Samuel Thibault, and Emmanuelle Saillard*: **Rethinking Data Race Detection in MPI-RMA Programs** [[hal](https://hal.science/hal-04272399v1)]
- [Parallel Computing 2020](https://dx.doi.org/10.1016/j.parco.2021.102859), *Joachim Protze, Marc-André Hermanns, Matthias S Müller, Van Man Nguyen, Emmanuelle Saillard, Julien Jaeger, Patrick Carribault, and Denis Barthou*: **MPI detach — Towards automatic asynchronous local completion** [[hal](https://hal.science/cea-03537990v1)]

## Academic curriculum
- 2016 - 2019: Ecole Nationale Supérieure d'Informatique pour l'Industrie et 
    l'Entreprise (ENSIIE), specialization in Intensive Computations and Big Data (CIDM - HPC).
- 2016: Degree in Applied Mathematics, at the University of Evry, France.
- 2014 - 2016: Classe Préparatoire aux Grandes Ecoles, MPSI/MP, at Lycée du Parc des Loges, Evry, France.
- 2014: Baccalauréat scientifique.
