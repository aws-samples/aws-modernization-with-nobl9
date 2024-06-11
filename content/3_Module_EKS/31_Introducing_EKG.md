---
title: "Introducing EKG" # MODIFY THIS TITLE
chapter: true
weight: 1 # MODIFY THIS VALUE TO REFLECT THE ORDERING OF THE MODULES IF APPLICABLE
---

## Introducing EKG -- Essential Kubernetes Gauges

GitHub repo: https://github.com/nobl9/ekg

### What is EKG?
EKG (Essential Kubernetes Gauges) is a set of starter SLOs, provisioned with Terraform, that comes in a
batteries-included package, including plumbing of Kubernetes metrics into Amazon Managed Service for Prometheus via
Amazon Distro for Open Telemetry. All of this is provisioned and managed via Terraform, which Nobl9 encounters very
frequently in use among platform engineering and SRE teams to manage infrastructure, including EKS.

These SLOs are based on best practices and interesting techniques that we have learned through working with our
customers to monitor both Kubernetes infrastructure and application workloads running in EKS.

![TargetGroup Monitoring tab location](/images/EKG_Intro.png)

### What are the SLOs?
The SLOs cover a variety of aspects of cluster and workload health.
A [detailed explanation](https://github.com/nobl9/ekg/tree/main/modules/nobl9) is available in the repo.