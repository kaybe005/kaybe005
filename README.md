# Kalash Bijukchhe

**Aspiring Junior DevOps / Cloud / Platform Engineer**  
Sydney, Australia | Kubernetes GitOps | AWS Terraform | CI/CD | Linux

I'm an IT student transitioning from full-stack development into DevOps, cloud infrastructure, platform engineering, and SRE fundamentals.

My strongest current work is focused on Kubernetes GitOps deployments, Terraform-managed AWS infrastructure, container delivery pipelines, networking, monitoring, and troubleshooting.

---

## DevOps / Cloud Focus

- **Kubernetes & GitOps:** k3s, Helm, ArgoCD, Traefik, cert-manager
- **AWS & IaC:** Terraform, VPC, EC2, ALB, NAT Gateway, IAM, SSM Session Manager
- **CI/CD & Containers:** Docker, GitHub Actions, GHCR, immutable Git SHA image tags
- **Operations:** Linux, DNS, TLS, PostgreSQL, Prometheus, Grafana, debugging and documentation

---

## Featured Projects

### [ERP Lite GitOps Homelab Platform](https://github.com/kaybe005/erp-lite)

Full-stack ERP-style app deployed through a production-style Kubernetes GitOps workflow in a homelab environment.

**Relevant stack:** Next.js, Prisma, PostgreSQL, Docker, GitHub Actions, GHCR, Helm, ArgoCD, k3s, Traefik, cert-manager, Prometheus, Grafana

**DevOps/platform work:**

- Built a CI/CD path from GitHub Actions to GHCR using `linux/amd64` Docker Buildx images and immutable Git SHA tags
- Deployed the app to k3s with Helm and ArgoCD
- Configured Traefik ingress, cert-manager TLS, and PVC-backed PostgreSQL
- Added Prometheus/Grafana monitoring for the homelab stack
- Worked through real deployment issues: ARM64/AMD64 image mismatch, image pull policy behavior, PVC drift, Prisma migration separation, DNS, ingress, and Grafana troubleshooting

---

### [AWS Secure Web Infrastructure with Terraform](https://github.com/kaybe005/aws-terraform-web-infra)

Terraform-managed AWS learning architecture: public ALB to private EC2 running Nginx, with NAT outbound access and SSM-based administration.

**Relevant stack:** Terraform, AWS VPC, EC2, ALB, NAT Gateway, IAM, SSM Session Manager, Nginx, security groups, user data

**Cloud/infrastructure work:**

- Built a VPC with 2 public subnets, 2 private subnets, Internet Gateway, NAT Gateway, ALB, target group, and security groups
- Kept EC2 private with no public IP and used AWS Systems Manager Session Manager instead of SSH
- Controlled traffic flow from public ALB to private EC2 using security groups
- Automated Nginx bootstrap with `user_data`
- Practiced ALB target group and health check debugging

---

## Supporting Full-Stack Background

I also have application development experience with React, Next.js, Node.js, Express, TypeScript, PostgreSQL, MongoDB, Prisma, and Tailwind.

That background helps me understand the application, database, and runtime concerns behind the infrastructure I deploy and support.

---

## Currently Learning

- Deeper AWS networking and IAM
- Terraform modules, remote state, and reusable infrastructure design
- Kubernetes operations and multi-node cluster management
- Monitoring, alerting, incident response, and runbook-style troubleshooting
- Secrets management, backup/restore workflows, and recovery basics

---

## Connect

- Portfolio: [kalashbijukchhe.com](https://kalashbijukchhe.com)
- LinkedIn: [linkedin.com/in/kayb05](https://linkedin.com/in/kayb05)
- Email: [kalashbijukchhe74@gmail.com](mailto:kalashbijukchhe74@gmail.com)
