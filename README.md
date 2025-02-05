# HPC Containers
---

Application developers require help from multiple tools to port and fine-tune their application on the different platforms. These tools and parallel languages help them to achieve results faster than expected. 
Installing such tools on a new environment takes lot of time and it is common to see users stuck on errors during installation phase of these tools. 
Thus, providing an option of using HPC containers for users to download and use witthout much hassle.

This repo contains information on usage of these singularity containers deployed by System Sofware Development Group (SSDG), CDAC Bengaluru. These containers are available at singularity library and can be downloaded for use. 

## List of containers

Currently the following containers are supported.

+ [hybridapplication_tau_aarch64](https://ssdg.cdacb.in:5000/): This container is based on using TAU for profiling hybrid applications on ARM architecture. [More Info](TAU_aarch64/README.md)
+ [Optimized OpenBLAS](): This container leverages the OpenBLAS library optimized for ARM with SVE to perform BLAS and LAPACK operations.[More Info](math_libraries/README.md)

## Help needed?

If users are stuck with any of the containers listed above or require additional support for these containers they can raise their issues on this repository. 
