
# Kalash Bijukchhe

**Junior DevOps / Cloud Engineer** · Adelaide, SA, Australia

Master of Information Technology student · Graduating **2028** · Available for full-time roles from **08/2028**

---

## Summary

I build and operate Kubernetes, Terraform and CI/CD systems end to end, in a homelab and on AWS. I prefer declarative state in Git, automated delivery and least-privilege defaults, and I document the trade-offs I make along the way.

---

## Core Tech Stack

| Area | Tools |
| --- | --- |
| **Cloud and IaC** | AWS (VPC, EC2, ALB, NAT Gateway, IAM, SSM Session Manager, ECR, RDS), Terraform |
| **Kubernetes and Containers** | k3s, Helm, ArgoCD, Traefik, cert-manager, Docker, Docker Buildx, readiness/liveness probes, PersistentVolumeClaims |
| **CI/CD** | GitHub Actions, GHCR, AWS ECR, Git-SHA image tags, GitOps (Git as the source of truth) |
| **Dev and Ops** | Linux (Ubuntu), Proxmox VE, systemd, Nginx, Python (FastAPI), TypeScript, PostgreSQL, Prometheus metrics, Grafana |

---

## Featured Projects

### [AI Inference GitOps](https://github.com/kaybe005/ai-inference-gitops)

A self-hosted LLM inference stack on a CPU-only Proxmox homelab, delivered through Git. GitHub Actions builds the image, and ArgoCD reconciles the Helm chart onto a k3s cluster.

- **Delivery:** GitHub Actions builds the FastAPI proxy image and pushes it to a private AWS ECR repository. ArgoCD syncs the Helm chart to k3s, which pulls from ECR with an image pull secret.
- **Availability:** rolling-update deployment strategy to maintain availability (2 replicas, `maxUnavailable: 0`, `maxSurge: 1`).
- **Health checks:** separate `/healthz` (liveness) and `/readyz` (readiness) endpoints. The pod only receives traffic once the Ollama backend is available.
- **Pod hardening:** non-root user, seccomp `RuntimeDefault`, read-only root filesystem, all capabilities dropped, resource requests and limits.
- **Observability:** the proxy exposes a Prometheus metrics endpoint with request count and latency.
- **Troubleshooting:**
  - Fixed readiness `503`s caused by Ollama listening only on `127.0.0.1`.
  - Moved the model from 3B to 1B through a Git-driven config change after CPU-only latency proved unusable.
  - Documented the switch to static IAM credentials for ECR pulls after an AWS Organizations SCP blocked GitHub OIDC federation.

`FastAPI` `Python` `Ollama` `Open WebUI` `Docker` `GitHub Actions` `AWS ECR` `Helm` `ArgoCD` `k3s` `Proxmox`

*Scope: single-node homelab cluster. Next steps are scraping the proxy metrics with Prometheus/Grafana and moving ECR authentication to OIDC.*

---

### [ERP Lite GitOps](https://github.com/kaybe005/erp-lite)

A full-stack inventory and order-management app (Next.js, Prisma, PostgreSQL) deployed to k3s through an automated pipeline for `linux/amd64` deployments.

- **CI:** GitHub Actions with Docker Buildx builds a `linux/amd64` image and pushes it to GHCR using the workflow's `GITHUB_TOKEN`. The image is tagged with the full commit SHA, and the new tag is committed back into the Helm values.
- **GitOps:** an ArgoCD Application with automated sync, prune and self-heal reconciles the Helm chart (app, PostgreSQL, PVC, Services, Ingress, probes).
- **Networking and data:** Traefik ingress with a cert-manager-issued internal TLS certificate and AdGuard DNS rewrites. PostgreSQL is reachable only through a ClusterIP Service and persists to a PVC.
- **Observability:** workload health inspected through Grafana dashboards (kube-prometheus-stack, installed at cluster level and not yet managed from this repo).
- **Troubleshooting:**
  - Resolved an ARM64/AMD64 image mismatch between an Apple Silicon dev machine and an AMD64 node.
  - Resolved PVC size drift between the cluster and the Helm values.
  - Separated Prisma migrations from the rollout (currently a manual step).

`Next.js` `TypeScript` `Prisma` `PostgreSQL` `Docker Buildx` `GitHub Actions` `GHCR` `Helm` `ArgoCD` `k3s` `Traefik` `cert-manager`

*Scope: single-node homelab cluster. Next steps are a migration Job, Sealed Secrets or SOPS for secrets, resource requests and limits, and test, lint and image-scan gates in CI.*

---

### [AWS Terraform Web Infrastructure](https://github.com/kaybe005/aws-terraform-web-infra)

A Terraform-defined AWS network and web tier: a public Application Load Balancer in front of an Nginx instance with no public IP, administered through SSM instead of SSH.

- **Network:** custom VPC with two public and two private subnets across availability zones, an Internet Gateway, a NAT Gateway and separate route tables per tier.
- **Isolation:** the instance security group accepts HTTP only from the ALB security group. There is no public IP and no inbound SSH.
- **Access:** IAM role and instance profile with `AmazonSSMManagedInstanceCore` for Session Manager.
- **Automation:** Nginx is bootstrapped through `user_data`, with ALB target-group health checks, consistent resource naming and tagging, and the provider lock file committed.

`Terraform` `AWS VPC` `ALB` `EC2` `NAT Gateway` `IAM` `SSM Session Manager` `Nginx`

*Scope: single-instance lab in `ap-southeast-2`. Next steps are reusable modules, S3 remote state with locking, HTTPS through ACM, and `terraform plan` checks in CI.*

---

## Application Background

I come from full-stack development (React, Next.js, TypeScript, Node.js, PostgreSQL, Prisma). Having built and shipped application code, I can reason about the workloads I deploy, including migrations, environment configuration, health endpoints and API behaviour under load.

---

## Contact

[Portfolio](https://kalashbijukchhe.dev) · [LinkedIn](https://www.linkedin.com/in/kayb05) · [Email](mailto:kalashbijukchhe74@gmail.com)
