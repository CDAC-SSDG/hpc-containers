# mathlibrary_aarch64.sif
---

## Description

[mathlibrary_aarch64.sif](https://cloud.sylabs.io/library/cdac_ssdg/aarch64_container/mathlibrary_aarch64) is a [singularity](https://en.wikipedia.org/wiki/Singularity_(software)) container based on ARM (aarch64). This container is used for solving the BLAS, LAPACK operations using OpenBLAS math library and FFT operations using FFTW math library. We can also profile these operations using [TAU Profiler](https://www.cs.uoregon.edu/research/tau/) which is available within the container. This README showcases the usage of the container, invoking math libraries and TAU profiling . It also lists the major softwares present in the container image for use.

## Usage

In order to use [this container](https://cloud.sylabs.io/library/cdac_ssdg/aarch64_container/mathlibrary_aarch64) follow the following steps:

+ Get the image from singularity library using:
```bash
singularity pull --arch arm64 library://cdac_ssdg/aarch64_container/mathlibrary_aarch64:v1
```

+ Once download is complete invoke the image shell using:
```bash
singularity shell mathlibrary_aarch64.sif
 ```

+ Set the environment using:
```bash
source /usr/setvars.sh
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

### Using Math libraries for FFT
+ Compiling the code:
```bash
1) Without Threading :
        gcc <program.c> -lm -lfftw3f
2) With Threading :
        gcc <program.c> -lm -lfftw3f_threads -lfftw3f -lpthread 
```
+ Run the code:
```bash
./a.out
```
### Using TAU for profiling
+ Compiling the code:
```bash
tau_CC.sh <program.c> -optCompInst
```
+ Run the code and check profile
```bash
./a.out
pprof
```


## Software details

[hybridapplication_tau_aarch64.sif]([singularity-link](https://cloud.sylabs.io/library/cdac_ssdg/aarch64_container/mathlibrary_aarch64)) contains the following softwares/packages:

| Category | Details |
| --- | --- |
| Architecture | ARM / aarch64 |
| Operating System | CentOS 8 |
| Linux Kernel | 4.18.0-348.el8.aarch64 |
| BLAS/LAPACK Library |  OpenBLAS v0.3.23 |
| FFT Library | FFTW-3.3.10 |
| Compiler | GCC v12.2.0 |
| Profiler | TAU v2.32.1 |
| Text Editor | vim |
| Git | v2.27.0 |
| Additional softwares| wget, curl |




