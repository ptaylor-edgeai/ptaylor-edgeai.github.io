---
layout: page
title: Edge AI Research Cluster
description: A physical Raspberry Pi Zero 2 W cluster for decentralised federated learning research
img: assets/img/cluster_photo.jpg
importance: 1
category: research
---

## The Hardware

This is a purpose-built physical testbed for researching **Decentralised Federated Learning (DFL)** on genuinely constrained hardware. Currently configured with **6 Raspberry Pi Zero 2 W** nodes — expanding to 10 — each node runs on a quad-core Cortex-A53 processor at 1GHz with 512MB RAM.

This is not a simulation. Every result is measured on real hardware under real resource pressure.

<div class="row justify-content-center">
  <div class="col-sm-10">
    {% include figure.liquid loading="eager" path="assets/img/projects/cluster_photo.jpg" title="Edge AI Research Cluster" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  6 Raspberry Pi Zero 2 W nodes (red cases) mounted on a hardwood board,
  communicating over WiFi. Currently expanding to 10 nodes.
</div>

## Why Physical Hardware Matters

Most federated learning research runs on cloud instances or simulated environments where memory, compute, and network are treated as abundant. That assumption breaks down at the edge.

Each node in this cluster operates under constraints that matter in real deployments:

- **512MB RAM** — model footprint, runtime, and monitoring overhead must all fit
- **No GPU** — all training runs on ARM CPU only
- **WiFi-only networking** — TCP/IP over 802.11, no dedicated interconnect
- **~2W per node** — total cluster draw under 15W at peak

These constraints are not obstacles to work around. They are the research conditions. The cluster exists to produce empirical results that reflect what federated learning actually costs on sub-watt devices.

## What I'm Researching

The cluster is the empirical foundation for my PhD research into decentralised federated learning and machine unlearning on constrained edge hardware. The focus is on what these techniques actually cost in practice — compute, memory, and time — and how they behave in peer-to-peer systems with no central coordinator.

More details to come as the research progresses.
