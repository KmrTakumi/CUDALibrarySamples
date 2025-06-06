# cuBLAS Level-3 APIs - `cublas<t>trmm`

## Description

This code demonstrates a usage of cuBLAS `trmm` function to compute a triangular matrix-matrix product

```
A = | 1.0 | 2.0 |
    | 3.0 | 4.0 |

B = | 5.0 | 6.0 |
    | 7.0 | 8.0 |
```

See documentation for further details.

## Supported SM Architectures

All GPUs supported by CUDA Toolkit (https://developer.nvidia.com/cuda-gpus)  

## Supported OSes

Linux  
Windows

## Supported CPU Architecture

x86_64  
ppc64le  
arm64-sbsa

## CUDA APIs involved
- [cublas\<t>trmm API](https://docs.nvidia.com/cuda/cublas/index.html#cublas-t-trmm)

# Building (make)

# Prerequisites
- A Linux/Windows system with recent NVIDIA drivers.
- [CMake](https://cmake.org/download) version 3.18 minimum

## Build command on Linux
```
$ mkdir build
$ cd build
$ cmake ..
$ make
```
Make sure that CMake finds expected CUDA Toolkit. If that is not the case you can add argument `-DCMAKE_CUDA_COMPILER=/path/to/cuda/bin/nvcc` to cmake command.

## Build command on Windows
```
$ mkdir build
$ cd build
$ cmake -DCMAKE_GENERATOR_PLATFORM=x64 ..
$ Open cublas_examples.sln project in Visual Studio and build
```

# Usage
```
$  ./cublas_trmm_example
```

Sample example output:

```
A
1.00 2.00 
3.00 4.00 
=====
B
5.00 6.00 
7.00 8.00 
=====
C
19.00 22.00 
28.00 32.00 
=====
```
