# Agnes L3 KV-Cache Pool

## Cluster-Shared KV Cache for Production Inference

This repository publishes a technical architecture and validation specification for a cluster-shared L3 KV-cache pool for Agnes inference. The design combines SGLang HiCache, MoonCake Store, registered host memory, and RDMA on PCIe GPU infrastructure.

## Report

- [Download the technical report](./agnes-l3-kv-cache-report.pdf)

## Architecture

- A three-tier cache path: private GPU L1, private host-memory L2, and cluster-shared Store DRAM L3.
- Benefit-gated recovery of the longest usable contiguous prefix.
- Read-priority asynchronous write-through for reusable KV pages.
- A topology-aware deployment and evidence plan for TP=2 and FP8 E4M3 KV.

## Evidence Boundary

This report is a design synthesis and validation specification. It does not present workload gains as measured Agnes production results. Release requires cold, warm, cross-instance, concurrent, and fault-injection validation with token-level cache metrics, TTFT, ITL, and cluster throughput.

## Publication

Prepared by Agnes AI Research. The PDF is the canonical publication.
