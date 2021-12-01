# GKE Cluster

This module creates a GKE Cluster and its dependencies including VPC, Servcice Account & Node Pools.

- Node Pools are created with Autoscaling enabled from 1 to 5 as 4x scalability is required.
- Worker Nodes are created with Private IPs to avoid visible security flaws.
- Logs and Metrics are enabled and exported to GCP (former Stackdriver).
