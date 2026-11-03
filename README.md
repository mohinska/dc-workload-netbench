# Research Task: Data Center Network Workloads

Workload-driven black-box testing of data center networks.

## Problem

Benchmarks running on top of a network show *that* performance dropped, but not *why*.
Example: increasing the number of threads lowers throughput, and it is unclear whether
the bottleneck is CPU, storage, or the network. This project aims to make network
bottlenecks visible and identifiable.

## Approach

The network is treated as a black box: we only generate load on top of an
already configured (virtual) network and measure what we can observe from the hosts.
Every test pairs a load generator with host-side and network-side metrics,
so that a slowdown can be attributed to the network or ruled out.

## Scope

1. **Workload taxonomy**: HPC/AI, virtualized apps, cloud-native services,
   distributed storage; their traffic patterns (East-West, North-South,
   bandwidth-intensive, latency-sensitive, mixed) and network requirements.
2. **Test scenarios**: tools, traffic patterns, and metrics for throughput,
   latency, congestion, load balancing, and failure recovery.
3. **Heterogeneous workloads**: concurrent workloads under congestion and
   oversubscription; performance isolation and bandwidth sharing.

## Deliverables

- [ ] Workload taxonomy table
- [ ] Test matrix (workload → traffic pattern → tools → metrics → expected results)
- [ ] Prioritized test recommendations for realistic and mixed workloads

## Repository structure