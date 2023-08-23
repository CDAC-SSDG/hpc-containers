#  hybridapplication_tau_aarch64.sif
---

## Description

[hybridapplication_tau_aarch64.sif](https://cloud.sylabs.io/library/cdac_ssdg/aarch64_container/hybridapplication_tau_aarch64) is a [singularity](https://en.wikipedia.org/wiki/Singularity_(software)) container based on ARM (aarch64). It can be used for profiling hybrid MPI on CPU based applications. This README showcases the usage of the container. It also lists the major softwares present in the container image for use.

## Usage

In order to use [this container](https://cloud.sylabs.io/library/cdac_ssdg/aarch64_container/hybridapplication_tau_aarch64) follow the following steps:

+ Get the image from singularity library using:
```bash
singularity pull --arch arm64 library://cdac_ssdg/aarch64_container/hybridapplication_tau_aarch64:v1
```

+ Once download is complete invoke the image shell using:
```bash
singularity shell hybridapplication_tau_aarch64.sif
 ```

+ Set the environment using:
```bash
source /usr/set_env.sh
```

The container is ready for use.


## Software details

[hybridapplication_tau_aarch64.sif]([singularity-link](https://cloud.sylabs.io/library/cdac_ssdg/aarch64_container/hybridapplication_tau_aarch64)) contains the following softwares/packages:

| Category | Details |
| --- | --- |
| Architecture | ARM / aarch64 |
| Operating System | CentOS 8 |
| Linux Kernel | 4.18.0-348.el8.aarch64 |
| Network Drivers | Mellanox Infinband |
| Compiler | GCC v12.2.0 |
| MPI | OpenMPI v4.1.4 |
| Profiler | TAU v2.32 |
| Text Editor | vim |
| Git | v2.27.0 |
| Additional softwares| wget, curl |



