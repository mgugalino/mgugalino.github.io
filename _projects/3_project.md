---
layout: page
title: Performance portable code for simulations of type Ia supernovae
description: 
img: assets/img/ares.png
importance: 1
category: Past
related_publications: false
---

Ares (Github: [https://github.com/lanl/AresPK](https://github.com/lanl/AresPK)) is a high-performance, performance-portable simulation code developed to model the complex physics of Type Ia supernovae on modern heterogeneous computing architectures. Built on the Parthenon-Hydro adaptive mesh refinement (AMR) framework and leveraging the Kokkos programming model, Ares can run efficiently across diverse CPU and GPU platforms. It includes critical physical components such as a nuclear statistical equilibrium (NSE) solver, a degenerate equation of state, and a monopole gravity solver, enabling realistic modeling of thermonuclear burning in white dwarfs.

In benchmark tests on LANL’s Chicoma system, Ares demonstrated excellent scalability and performance. GPU-enabled runs achieved nearly ideal strong scaling and outperformed CPU-only configurations by around 50% per rank, maintaining high efficiency even across 64 GPUs. These results show that Ares is well-positioned for use on current and future high-performance computing systems. The project lays the groundwork for future full 3D simulations of supernovae and highlights the importance of performance-portable, modular code design in computational astrophysics.

This project was developed as part of the [Co-Design Summer School](https://lanl.github.io/cdss/) (consider applying, it was a really fun experience!) at Los Alamos National Laboratory, under the supervision of Julien Loiseau and Hyun Lim. (LA-UR-23-29154)

### Related publications / presentations
1. Landon Dyken, Alexander Holas, Mark Ivan Ugalino, and Md Nageeb Bin Zaman. 2023. "Ares – Simulating Type Ia Supernovae on Heterogeneous HPC Architectures" ([LA-UR-23-29154](https://sc23.supercomputing.org/proceedings/tech_poster/poster_files/rpost180s3-file3.pdf)) The International Conference for High Performance Computing, Networking, Storage, and Analysis (September 2023)
