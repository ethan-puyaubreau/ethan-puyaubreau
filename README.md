# Ethan Puyaubreau

**I measure what GPU code really costs, and I keep the production cluster that runs it healthy.**

HPC and infrastructure engineer, Polytech Paris-Saclay (2026). **Available January 2027** for HPC or infra/DevOps roles, Paris or Bay Area.

[Portfolio](https://ethan-puyaubreau.github.io) · [LinkedIn](https://www.linkedin.com/in/ethan-puyaubreau/) · [Google Scholar](https://scholar.google.com/citations?user=VH9ZyxYAAAAJ) · [ORCID](https://orcid.org/0009-0003-1770-8830) · [ethan.puyaubreau@gmail.com](mailto:ethan.puyaubreau@gmail.com)

---

## Oak Ridge National Laboratory, summer 2025

I built GPU energy-measurement tooling for **Kokkos**, the US Department of Energy's performance-portability framework.

- **Merged upstream.** My periodic-sampling daemon is in [kokkos-tools (PR #300)](https://github.com/kokkos/kokkos-tools/pull/300).
- **Presented.** Poster at the 2025 Smoky Mountains Conference: [*Understanding GPU energy dynamics in HPC applications*](https://github.com/ethan-puyaubreau/smc2025-gpu-energy-poster).
- **On the record.** Cited in ORNL's [S4PST 2024-2025 project report](https://www.osti.gov/biblio/3016977).
- **Open source.** [energy-dashboard-for-kokkos](https://github.com/ethan-puyaubreau/energy-dashboard-for-kokkos) turns Kokkos Tools output into per-kernel energy analysis.

## EDF Lab Paris-Saclay, HPC apprenticeship (2023-2026)

C++ memory-profiling and CPU-timing tooling for COCAGNE, EDF's ~500k-line reactor-core simulation code.

## Production infrastructure I run

A 5-node Proxmox cluster serving about 20 public services behind Traefik and Let's Encrypt, deployed through CI/CD with image scanning and automatic rollback. I handle uptime, backups and certificates myself.

**[proxmox-ops-mcp](https://github.com/ethan-puyaubreau/proxmox-ops-mcp)** lets an AI agent operate that cluster safely. Destructive commands are blocked until I approve them out-of-band on Telegram, so a prompt injection cannot approve itself.

## Side projects

**[nbody-webgpu](https://github.com/ethan-puyaubreau/nbody-webgpu)** is a real-time N-body galaxy simulation running on WebGPU compute shaders.

<img src="galaxy.gif" alt="Spiral galaxy simulated in real time with WebGPU compute shaders" width="560">

**[isochrone-app](https://github.com/ethan-puyaubreau/isochrone-app)** is an offline isochrone explorer built on a self-hosted Valhalla routing engine.

## Stack

**HPC:** C++17 · CUDA · Kokkos · MPI · OpenMP · NVML\
**Infra:** Proxmox · Docker · K3s · Traefik · WireGuard · GitLab CI\
**Also:** Python · TypeScript · WebGPU

---

**Hiring for HPC or infra from January 2027? [Email me](mailto:ethan.puyaubreau@gmail.com).**
