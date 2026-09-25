# Ethan Puyaubreau

**I build research software that measures what scientific computing costs.**

Research software engineer in high-performance computing. M.Eng.-equivalent from Polytech Paris-Saclay (September 2026) after three years of work-study at EDF R&D and a research stay at Oak Ridge National Laboratory.

**Available early 2027** for research software engineer roles in HPC and scientific computing, at national labs, universities or research institutes, in the US or in France. For US roles I need visa sponsorship (J-1 or H-1B).

[Portfolio](https://ethan-puyaubreau.github.io) · [LinkedIn](https://www.linkedin.com/in/ethan-puyaubreau/) · [Google Scholar](https://scholar.google.com/citations?user=VH9ZyxYAAAAJ) · [ORCID](https://orcid.org/0009-0003-1770-8830) · [ethan.puyaubreau@gmail.com](mailto:ethan.puyaubreau@gmail.com)

---

## Oak Ridge National Laboratory, summer 2025

Graduate Research Fellow (GRO program). I built GPU energy-measurement tooling for **Kokkos**, the C++ performance-portability library behind many US Department of Energy codes: a sampling daemon and connectors that read power through NVML or Variorum every 20 ms, plus an AMD path through ROCm SMI, not public yet, which is the version that ran on Frontier. They attach at run time through Kokkos Tools, so an application is measured without a rebuild.

- **Ran on Frontier**, the first exascale supercomputer (the ROCm SMI version), and on production SLURM clusters.
- **Found a cost a timer understates.** On the same input and result, ArborX's dense DBSCAN takes 19% less time than the default one but 25% less energy, because it also draws 9% less power (medians of 64 runs on an H100 NVL, [re-analysed in 2026](https://ethan-puyaubreau.github.io/blog/kokkos-gpu-energy); [traces and script](https://github.com/ethan-puyaubreau/smc2025-gpu-energy-poster#data-and-reproduction) are public).
- **Went through public review.** 9 PRs, [8 to kokkos-tools](https://github.com/kokkos/kokkos-tools/pulls?q=is%3Apr+author%3Aethan-puyaubreau) and [1 to LAMMPS](https://github.com/lammps/lammps/pull/4624): 3 merged: the sampling daemon I started ([kokkos-tools #300](https://github.com/kokkos/kokkos-tools/pull/300), reworked through review by my ORNL mentor after my stay) and two build fixes. The core ([#299](https://github.com/kokkos/kokkos-tools/pull/299)), the NVML connector ([#301](https://github.com/kokkos/kokkos-tools/pull/301), changes requested) and the Variorum connector with its unit tests ([#302](https://github.com/kokkos/kokkos-tools/pull/302), draft) are still open.
- **Presented.** Poster at the 2025 Smoky Mountains Conference and at an ORNL internal session ([*Understanding GPU energy dynamics in HPC applications*](https://github.com/ethan-puyaubreau/smc2025-gpu-energy-poster)), and invited to present at SC25 (declined, apprenticeship schedule). Cited in ORNL's [S4PST 2024-2025 report](https://www.osti.gov/biblio/3016977).

The analysis side is open source and archived on Zenodo ([DOI 10.5281/zenodo.22943410](https://doi.org/10.5281/zenodo.22943410)): [energy-dashboard-for-kokkos](https://github.com/ethan-puyaubreau/energy-dashboard-for-kokkos), rewritten in September 2026 as a single Rust binary that attributes measured energy to Kokkos regions and kernels, with a console table, a Perfetto trace and a standalone HTML report.

## EDF R&D, work-study (2023-2026)

On the C++ platform that simulates EDF's nuclear reactor cores (500k+ lines, 30+ engineers):

- **Wrote the memory and compute-time profilers** (C++, Python bindings). The memory profiler pinned down a memory blow-up the team had been chasing for days.
- **Developed the prototype of a new modular architecture for the neutronics solvers** and measured it with those tools: bit-for-bit identical results, **up to 12% faster** on the compute core, **38% lower peak memory**.
- **Automated the test and delivery chain**: cluster runs, result validation, PostgreSQL ingestion, Debian packaging (Jenkins, GitLab CI/CD).
- **Worked in the team's process**: code reviews given and received, five internal technical notes, Sphinx documentation for the tools.

## Infrastructure I run

A [5-node Proxmox cluster](https://ethan-puyaubreau.github.io/cluster) I have designed and operated alone since 2020, for about twenty services and ~60 regular users. Over the years it has run Ceph, Ansible and GitLab CI; today Gitea and Coolify carry the CI/CD and a Kubernetes (K3s) VM runs alongside, behind Traefik, Authelia SSO and a VyOS-segmented network, watched by Gatus and Uptime Kuma. Every incident is mine.

**[proxmox-ops-mcp](https://github.com/ethan-puyaubreau/proxmox-ops-mcp)** lets an AI assistant operate that cluster. Every command goes through a deny-by-default classifier; destructive ones wait for my approval on a separate channel and land in an append-only audit log, so a prompt injection cannot approve itself.

## Side project

**[nbody-webgpu](https://github.com/ethan-puyaubreau/nbody-webgpu)**: up to 65,536 bodies in a WGSL compute shader, tiled through workgroup shared memory, leapfrog integrator. [Run it in your browser](https://ethan-puyaubreau.github.io/nbody-webgpu/).

<a href="https://ethan-puyaubreau.github.io/nbody-webgpu/"><img src="galaxy.webp" alt="Spiral galaxy simulated in real time with WebGPU compute shaders" width="560"></a>

## Stack

**HPC:** C++17/20 · CUDA · Kokkos · MPI · OpenMP · SLURM · NVML · ROCm-SMI\
**Research software:** Python · PyBind11 · CMake · Rust · Git · GitHub Actions · GitLab CI · Sphinx\
**Infra:** Proxmox · K3s · Ceph · Docker · Traefik · Ansible\
**Also:** PostgreSQL · TypeScript · WebGPU

---

**Hiring a research software engineer for early 2027? [Email me](mailto:ethan.puyaubreau@gmail.com).**
