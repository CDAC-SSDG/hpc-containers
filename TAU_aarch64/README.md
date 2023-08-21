# TAU_aarch64 

**Description:** This README explains how to use the [tau_aarch64.sif](singularity-link) container. It also describes the major softwares present in the image for the use of user.

---

## Usage

In order to use [this](singularity-link) container follow the following steps:

+ Get the image from singularity library using:
```bash
singularity pull <image_link>
```

+ Once download is complete invoke the image shell using:
```bash
singularity shell tau_openmpi_aarch64.sif
 ```

+ Once inside the container shell set the environment using:
```bash
source /usr/set_env.sh
```

The container is ready for use. 


## Software details

[tau_openmpi_aarch64](singularity-link) contains the following softwares/packages:

| Category | Details |
| --- | --- |
| Architecture | ARM / aarch64 |
| Operating System | CentOS 8 |
| Linux Kernel | 4.18.0-348.el8.aarch64 |
| Network Drivers | Mellanox Infinband |
| Compiler | GCC v12.2.0 |
| Python | v2.7.18 & v3.6.8|
| MPI | OpenMPI v4.1.4 |
| Profiler | TAU v2.32 |
| Text Editor | vim |
| Git | v2.27.0 |
| Additional softwares| wget, curl |



