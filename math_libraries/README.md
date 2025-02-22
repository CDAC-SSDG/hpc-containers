# Openblas_arm.sif
---

## Description

The Openblas_arm.sif Singularity container offers an ARM-optimized version of the OpenBLAS library, designed to accelerate BLAS and LAPACK operations. It leverages Scalable Vector Extension (SVE) technology for improved performance on ARM-based systems. The README provides instructions on how to use the container and invoke the math library.

## Usage

In order to use [this container](https://nsmindia.in/download/Openblas_arm.sif) follow the following steps:

+ Get the image from [Openblas_arm.sif](https://nsmindia.in/download/Openblas_arm.sif) 

+ Once download is complete invoke the image shell using:
```bash
singularity shell openblas_arm.sif
 ```

+ Set the environment using:
```bash
export LD_LIBRARY_PATH=/home/user/openblas/lib/:$LD_LIBRARY_PATH
```
The container is ready for use.

### Using Math libraries for BLAS/LAPACK 

+ Compiling the code:
```bash
gcc <program.c> -I /home/user/openblas/include/ -L /home/user/openblas/lib/  -lopenblas
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

## Software details

[Openblas_arm.sif]() contains the following softwares/packages:

| Category | Details |
| --- | --- |
| Architecture | ARM / aarch64 |
| Operating System | AlmaLinux 9.4 |
| Linux Kernel | 5.14.0-362.8.1.el9_3.aarch64 |
| BLAS/LAPACK Library |  OpenBLAS v0.3.26 |
| Compiler | GCC v12.2.0 |

## Help

Any query or help regarding the container usage needed? Raise an issue/discussion on the repository.

