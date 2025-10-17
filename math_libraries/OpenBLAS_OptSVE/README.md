# OpenBLAS_OptSVE_NeoverseV2.sif
---

## Description

The OpenBLAS_OptSVE_NeoverseV2.sif Singularity container provides an optimized version of the OpenBLAS library, leavering Scalable Vector Extension(SVE) to accelerate BLAS and LAPACK rountines.

## Usage

In order to use [this container](https://github.com/CDAC-SSDG/hpc-containers/blob/main/math_libraries/OpenBLAS_OptSVE/OpenBLAS_OptSVE_NeoverseV2.sif) follow the following steps:

+ Get the image from [Openblas_arm.sif](https://github.com/CDAC-SSDG/hpc-containers/blob/main/math_libraries/OpenBLAS_OptSVE/OpenBLAS_OptSVE_NeoverseV2.sif) 

+ Once download is complete invoke the image shell using:
```bash
singularity shell OpenBLAS_OptSVE_NeoverseV2.sif
 ```

+ Set the environment using:
```bash
export LD_LIBRARY_PATH=/usr/lib/:$LD_LIBRARY_PATH
```
The container is ready for use.

### Using Math libraries for BLAS/LAPACK 

+ Compiling the code:
```bash
gcc <program.c> -lopenblas
```

+ Run the code:
```bash
./a.out
```

+ OpenBLAS also supports threading:
+ setting the threads:
```bash
export OPENBLAS_NUM_THREADS= <no of threads>
```


## Help

Any query or help regarding the container usage needed? Raise an issue/discussion on the repository.


