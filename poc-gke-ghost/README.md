# GKE Cluster

This module creates a GKE Cluster and its dependencies including VPC, Servcice Account & Node Pools.

- Node Pools are created with Autoscaling enabled from 1 to 5 as 4x scalability is required.
- Worker Nodes are created with Private IPs to avoid visible security flaws.
- Logs and Metrics are enabled and exported to GCP (former Stackdriver).
- Ghost PoC cluster is regional so it remains online even in case of a significant geographical (zonal) failure.

## How to Deploy

[Configure the GCP Provider.](https://registry.terraform.io/providers/hashicorp/google/latest/docs/guides/getting_started)

Fill up the Values in `poc.tfvars`

```
terraform init
terraform plan -var-file="poc.tfvars"
terraform apply -var-file="poc.tfvars"
```
