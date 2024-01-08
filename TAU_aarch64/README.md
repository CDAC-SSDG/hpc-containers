#  hybridapplication_tau_aarch64.sif
---

## Description

[hybridapplication_tau_aarch64.sif](https://ssdg.cdacb.in:5000/) is a [singularity](https://en.wikipedia.org/wiki/Singularity_(software)) container based on ARM (aarch64). It can be used for profiling hybrid MPI on CPU based applications. This README showcases the usage of the container. It also lists the major softwares present in the container image for use.

## Usage

In order to use [this container](https://ssdg.cdacb.in:5000/) follow the following steps:

+ Get the image from [CDAC open source page](https://ssdg.cdacb.in:5000/)

+ Once download is complete invoke the image shell using:
```bash
singularity shell hybridapplication_tau_aarch64.sif
 ```

+ Set the environment using:
```bash
source /usr/set_env.sh
```

The container is ready for use.

## Using CUDA

- Compiling cuda code
```bash
nvcc <program.cu> 
 ```
- Run the code
```bash
./a.out
```
## Using CUDA with mpi
- Compiling cuda with mpi code
```bash
nvcc -Xcompiler -fopenmp <program_name.cu> -o <program_name> -I$<OPENMPI_ROOT>/include -L$<OPENMPI_ROOT}/lib -lmpi -lgomp 
 ```
- Run the code
```bash
mpirun -np <no. of processes> ./<program_name>
```
## Using TAU for profiling CUDA with mpi code
After compiling the CUDA + mpi code run the code as follows 
```bash
mpirun -np <no. of processes> tau_exec ./<program_name>
pprof
```
## Software details

[hybridapplication_tau_aarch64.sif](https://ssdg.cdacb.in:5000/) contains the following softwares/packages:

| Category | Details |
| --- | --- |
| Architecture | ARM / aarch64 |
| Operating System | CentOS 8 |
| Linux Kernel | 4.18.0-348.el8.aarch64 |
| Network Drivers | Mellanox Infinband |
| Compiler | GCC v12.2.0 |
| MPI | OpenMPI v4.1.4 |
| CUDA | 12.3 |
| Profiler | TAU v2.33 |
| Text Editor | vim |
| Git | v2.27.0 |
| Additional softwares| wget, curl |


## Help

For any query or help regarding the usage of container users can raise an issue/discussion/query in the repository.
