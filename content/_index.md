---
title: "Netsy — Replicated Key-Value Database"
description: "Netsy is a replicated key-value database which stores data in object storage. A drop-in etcd replacement for Kubernetes."
layout: hextra-home
---

{{< hextra/hero-badge >}}
  Open Source, Apache 2.0 licensed
{{< /hextra/hero-badge >}}

{{< hextra/hero-headline style="margin-top: 1.5rem; margin-bottom: 0.5rem;" >}}
  KV Database using Object Storage
{{< /hextra/hero-headline >}}

{{< hextra/hero-subtitle style="font-size: 2rem; color: #4b5563; margin-bottom: 0.75rem;" >}}
  Netsy is a durable, replicated key-value database which stores data in object storage.
{{< /hextra/hero-subtitle >}}

{{< hextra/hero-subtitle style="margin-bottom: 2.5rem; max-width: 50rem;" >}}
  A drop-in etcd replacement for Kubernetes, or a general-purpose KV store — with durable, low-latency persistence and no operational complexity.
{{< /hextra/hero-subtitle >}}

{{< hextra/hero-button text="Learn More" link="/docs/motivation" style="margin-bottom: 2rem;" >}}

{{< hextra/feature-grid >}}
  {{< hextra/feature-card
    title="Compatible with etcd API"
    subtitle="Implements Range, Txn, and Watch — supporting all options used by Kubernetes. A drop-in replacement."
  >}}
  {{< hextra/feature-card
    title="Object Storage Persistence"
    subtitle="Data is durably stored in object storage via snapshots and chunked deltas. No local disks to manage."
  >}}
  {{< hextra/feature-card
    title="Multi-Node Replication"
    subtitle="Quorum-based replication inspired by PostgreSQL, with automatic leader election."
  >}}
  {{< hextra/feature-card
    title="Automatic Failover"
    subtitle="Built-in leader election via s3lect with graceful failover and automatic recovery from node failures."
  >}}
  {{< hextra/feature-card
    title="Backfill & Recovery"
    subtitle="Start a fresh node and Netsy automatically restores from object storage snapshots and chunks."
  >}}
  {{< hextra/feature-card
    title="Cluster-Wide Compaction"
    subtitle="Coordinated compaction can remove historical revision data across all nodes to reclaim storage."
  >}}
{{< /hextra/feature-grid >}}
