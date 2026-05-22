---
title: "Distributed Compute Cluster from Old Workstations"
subtitle: "Turning retired office PCs into a practical compute cluster for simulations and infrastructure experiments."
summary: "Designed and assembled a low-cost Linux-based cluster focused on repeatable provisioning, shared storage, networking, monitoring, and practical engineering workloads."
status: "Active"
stack: [Linux, Networking, Automation, NFS, Slurm]
repo: "https://github.com/jsciotto05/REPO_NAME_HERE"
demo:
featured: true
order: 1
---

## Overview

This project explores whether a collection of retired office workstations can be turned into a useful compute cluster for engineering simulations, numerical experiments, and infrastructure learning.

The goal was not to build a high-performance supercomputer. The goal was to design a repeatable, low-cost system that could distribute workloads, share files across nodes, and provide a realistic platform for learning Linux administration, networking, and cluster computing.

## Motivation

Engineering simulations and numerical experiments can become computationally expensive quickly. Rather than relying only on a personal laptop, I wanted to experiment with a local cluster built from older hardware that would otherwise go unused.

This project gave me a way to learn practical systems engineering topics, including:

- Linux server setup
- Static networking and DNS troubleshooting
- Shared storage
- Job scheduling
- Node provisioning
- Performance limitations of mixed hardware
- Reliability and maintainability tradeoffs

## Constraints

The cluster was built around several practical constraints:

- Use mostly retired or low-cost hardware
- Keep the system local to my home network
- Prefer open-source tooling
- Make the setup repeatable across different machines
- Support engineering workloads such as simulations, scripts, and batch jobs
- Avoid unnecessary complexity where a simpler tool would work

## System Design

The system uses a head-node and worker-node model. The head node manages shared storage, network configuration, and job submission. Worker nodes connect over the local network and execute assigned jobs.

The intended architecture includes:

- A Linux head node
- Multiple Linux worker nodes
- Shared network storage
- SSH-based administration
- Job scheduling for batch workloads
- Monitoring for CPU, memory, and node status

## Implementation

Initial implementation focused on getting the basic infrastructure working before optimizing performance.

Major setup steps included:

1. Installing Linux on the head node and worker nodes
2. Configuring network access between machines
3. Setting up shared directories for project files and outputs
4. Testing SSH access between nodes
5. Installing cluster management and job scheduling tools
6. Running small workloads to validate communication and shared storage

The main technical challenge was not raw computing power; it was making the machines communicate reliably and behave like one coordinated system.

## Results So Far

The project has successfully demonstrated the core idea: older workstations can be repurposed into a useful learning and experimentation platform.

The most valuable results so far have been:

- A better understanding of Linux networking
- Experience with shared storage configuration
- Practical troubleshooting of multi-machine systems
- A clearer understanding of what makes cluster computing difficult in practice
- Identification of bottlenecks caused by mixed hardware and network limitations

## Lessons Learned

The biggest lesson is that distributed computing is more about systems integration than simply connecting many computers together. Networking, storage, authentication, repeatability, and monitoring matter just as much as CPU performance.

This project also showed that old hardware can still be useful when the workload is chosen carefully. The cluster is best suited for batch jobs, parameter sweeps, automation tasks, and educational experiments rather than tightly coupled high-performance simulations.

## Next Steps

Future improvements include:

- Automating node setup with scripts or Ansible
- Adding a cleaner monitoring dashboard
- Benchmarking different workloads
- Improving job scheduling
- Documenting setup steps for repeatability
- Testing engineering simulation workloads across multiple nodes---
title: "Distributed Compute Cluster from Old Workstations"
subtitle: "Turning retired office PCs into a useful compute cluster for simulations."
summary: "Designed and assembled a low-cost cluster, focusing on repeatable provisioning, monitoring, and practical throughput."
status: "Active"
stack: [Linux, Networking, Automation]
repo: "https://github.com/jsciotto05/REPO_NAME_HERE"
demo:
featured: true
order: 1
---

## The problem
What you wanted and why it mattered.

## Constraints
Budget, time, hardware, power, reliability.

## Design
Architecture + tradeoffs (why this approach, why not alternatives).

## Implementation
Provisioning, tooling, monitoring, what you built yourself.

## Results
Benchmarks, screenshots, costs, lessons.

## What I’d improve
What you’d change next iteration.
