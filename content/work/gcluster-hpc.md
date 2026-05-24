---
title: 'gCluster: Research HPC Built from the Ground Up at UC Irvine'
date: 2019-06-01T00:00:00+00:00
draft: false
featured: true
weight: 7
heroHeading: 'gCluster HPC'
heroSubHeading: 'UC Irvine, Gaut Lab'
heroBackground: ''
---

### Challenge

The lab needed a high-performance computing cluster capable of handling large-scale genomic analyses, population genetics simulations, and machine learning workloads, without relying on shared university resources with long queue times and limited customization.

### Approach

Designed, built, and administered gCluster, a dedicated research HPC at UC Irvine. The system consists of 10 compute nodes (48 cores each), a login node, a SLURM management node, and 2 storage nodes providing 180TB of networked storage over InfiniBand. Configured SLURM for job scheduling across CPU, RAM, and GPU resources. Implemented Access Control Lists (ACLs) for secure multi-user file sharing, and deployed Singularity containers for reproducible software environments across the cluster.

### Result

A fully operational, multi-user research cluster supporting genomic assembly, population genetics, and deep learning workloads. Eliminated queue wait times that previously delayed analyses by days to weeks on shared university resources. The cluster supported 10+ concurrent users, processed terabyte-scale genomic datasets, and served as the computational backbone for multiple funded projects and peer-reviewed publications.

**Specifications:**
- 10 compute nodes, 48 cores each (480 total cores)
- 180TB networked storage over InfiniBand
- SLURM job scheduler with CPU, RAM, and GPU resource management
- Singularity containerization for reproducible environments
- ACL-based file sharing and security
- Dedicated login node and SLURM management node
