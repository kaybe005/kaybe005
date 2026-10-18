# Kalash Bijukchhe

**DevOps / Cloud / Platform Engineer**  
Adelaide, SA, Australia | Kubernetes GitOps | AWS & Terraform | CI/CD | Linux

I am a Master of IT student specializing in cloud infrastructure, GitOps automation, container orchestration, and platform reliability. 

My work focuses on declarative Kubernetes deployments, Terraform-managed AWS environments, hybrid CI/CD pipelines, and local AI infrastructure.

---

## 🧰 Technical Capabilities

- **Kubernetes & GitOps:** k3s, Helm, ArgoCD, Traefik, cert-manager, Custom Readiness Probes
- **AWS & Cloud IaC:** Terraform, VPC, EC2, ECR, ALB, NAT Gateway, IAM, SSM Session Manager, S3
- **CI/CD & Containers:** Docker, Docker Buildx, GitHub Actions, GHCR, AWS ECR, Immutable SHA Tagging
- **Platform & Runtime:** Linux (Ubuntu/Proxmox VE), FastAPI, Python, Node.js/Next.js, PostgreSQL, Ollama (Local LLM Runtime)
- **Observability & Operations:** Prometheus, Grafana, Systemd, Reverse Proxies, DNS & TLS Management

---

## 🚀 Featured Projects

### [Self-Hosted GitOps AI Inference Platform](https://github.com/kaybe005/ai-inference-gitops)

A zero-downtime, hybrid-cloud GitOps AI inference platform hosted on a local Kubernetes (`k3s`) cluster on Proxmox, integrated with AWS ECR and GitHub Actions.

**Tech Stack:** FastAPI, Python, Ollama (`llama3.2:1b`), Docker, GitHub Actions, AWS ECR, Helm, ArgoCD, k3s, Open WebUI

**Platform & Engineering Work:**
- Engineered an automated CI/CD pipeline using GitHub Actions to build FastAPI proxy images and push them to private AWS ECR.
- Configured ArgoCD and Helm for declarative continuous deployment to an on-premises `k3s` cluster.
- Implemented custom `/readyz` probes and systemd network bindings (`0.0.0.0`) to verify Ollama model availability before routing traffic.
- Optimized model runtime performance for CPU-only hardware by executing a GitOps rollout to step down to a lightweight 1B quantized LLM.

---

### [AWS Secure Web Infrastructure with Terraform](https://github.com/kaybe005/aws-terraform-web-infra)

Declarative AWS cloud architecture provisioning a public ALB to private EC2 running Nginx, with NAT outbound access and SSM-based administration.

**Tech Stack:** Terraform, AWS VPC, EC2, ALB, NAT Gateway, IAM, SSM Session Manager, Nginx, Security Groups

**Cloud & Infrastructure Work:**
- Provisioned an isolated VPC with public/private subnets, Internet Gateway, NAT Gateway, ALB, and strict security groups.
- Enforced zero-public-IP architecture on compute nodes using AWS Systems Manager (SSM) Session Manager instead of SSH.
- Automated Nginx bootstrapping via EC2 `user_data` and established ALB target group health checks.

---

### [ERP Lite GitOps Homelab Platform](https://github.com/kaybe005/erp-lite)

Full-stack ERP application deployed through a production-style Kubernetes GitOps workflow in a homelab environment.

**Tech Stack:** Next.js, Prisma, PostgreSQL, Docker, GitHub Actions, GHCR, Helm, ArgoCD, k3s, Traefik, cert-manager, Prometheus, Grafana

**Platform & Engineering Work:**
- Built automated CI/CD with Docker Buildx multi-arch builds and immutable Git SHA container tags.
- Deployed stateful and stateless services to `k3s` using Helm charts and ArgoCD sync policies.
- Integrated Traefik ingress routing, cert-manager TLS certificates, and PVC-backed PostgreSQL with Prometheus/Grafana monitoring.

---

## 💡 Supporting Application Background

I hold a strong background in full-stack software development (TypeScript, React, Next.js, Node.js, Express, PostgreSQL, Prisma, Tailwind CSS). Understanding application runtimes, database migrations, and API contracts allows me to design better infrastructure and troubleshoot complex system boundaries.

---

## 📈 Currently Expanding

- Advanced AWS Networking (Transit Gateways, PrivateLink) & IAM Policy Scoping
- Modular Terraform State Architecture & Reusable Infrastructure Code
- Cluster Reliability, Multi-Node Kubernetes Operations, & Disaster Recovery
- Observability Stacks (Prometheus Rules, Alertmanager, Grafana Dashboards)

---

## 📫 Connect

- **Portfolio:** [kalashbijukchhe.dev](https://kalashbijukchhe.dev)
- **LinkedIn:** [linkedin.com/in/kayb05](https://linkedin.com/in/kayb05)
- **Email:** [kalashbijukchhe74@gmail.com](mailto:kalashbijukchhe74@gmail.com)
- **GitHub:** [@kaybe005](https://github.com/kaybe005)
