# Ethan Puyaubreau

HPC and infrastructure engineer, finishing my degree at Polytech Paris-Saclay (Sept 2026), open to roles from January 2027 in HPC or infra/DevOps, Paris or Bay Area. I make a GPU kernel fast and keep the production cluster that runs it healthy.

Name on the record: ORCID [0009-0003-1770-8830](https://orcid.org/0009-0003-1770-8830).

---

## Flagship: Oak Ridge National Laboratory (summer 2025)

GPU energy-measurement tooling for Kokkos, the US Department of Energy's performance-portability framework. The periodic-sampling daemon is merged upstream ([kokkos-tools PR #300](https://github.com/kokkos/kokkos-tools/pull/300)); the work was presented as a poster at the 2025 Smoky Mountains Conference and written up in an [ORNL report](https://www.osti.gov/biblio/3016977).

[energy-dashboard-for-kokkos](https://github.com/ethan-puyaubreau/energy-dashboard-for-kokkos)

## Experience

**EDF Lab Paris-Saclay**, HPC apprenticeship (2023-2026). C++ memory-profiling and CPU-timing tooling for COCAGNE, a ~500k-line reactor-core simulation codebase.

**Self-hosted production infrastructure.** A 5-node Proxmox cluster, about 20 public services behind one Traefik and Let's Encrypt TLS, deployed with Docker and CI/CD with image scanning and automatic rollback. On call for uptime, backups and certificates.

## Selected projects

| | |
|---|---|
| [energy-dashboard-for-kokkos](https://github.com/ethan-puyaubreau/energy-dashboard-for-kokkos) | Per-kernel GPU energy analysis on Kokkos Tools output (ORNL) |
| [isochrone-app](https://github.com/ethan-puyaubreau/isochrone-app) | Offline isochrone explorer over a self-hosted Valhalla routing engine |
| [nbody-webgpu](https://github.com/ethan-puyaubreau/nbody-webgpu) | Real-time N-body galaxy simulation, compute shaders in WebGPU |

## Stack

**HPC**: C++17, CUDA, MPI, OpenMP, Kokkos, Variorum, NVML; finite-difference, symplectic/IMEX integrators, von Neumann stability
**Infra**: Proxmox, Docker, K3s, Traefik, VyOS, WireGuard, GitLab CI/CD, Jenkins
**Web**: Vue 3, Nuxt 3, TypeScript, Astro, WebGPU
**Other**: Python, PyBind11, Rust (learning)

---

[LinkedIn](https://www.linkedin.com/in/ethan-puyaubreau/) · [Google Scholar](https://scholar.google.com/citations?user=VH9ZyxYAAAAJ) · [ethan.puyaubreau@gmail.com](mailto:ethan.puyaubreau@gmail.com)
