# Hi, I'm Kalash Bijukchhe 👋

**Aspiring Junior DevOps / Cloud / Platform Engineer based in Sydney, Australia.**

I'm an IT student with a full-stack development background, now focused on cloud infrastructure, Kubernetes, GitOps, CI/CD, and platform engineering fundamentals.

I like building hands-on systems that force me to understand deployment, networking, automation, observability, and real troubleshooting beyond just application code.

---

## Current Focus

- Kubernetes, Helm, ArgoCD, and GitOps workflows
- AWS networking and Terraform infrastructure as code
- CI/CD pipelines and containerized deployments
- Linux, networking, monitoring, and troubleshooting
- Prometheus/Grafana observability and SRE fundamentals

---

## Featured DevOps / Cloud Projects

### [ERP Lite GitOps Homelab Platform](https://github.com/kaybe005/erp-lite)

Full-stack ERP app deployed through a Kubernetes GitOps workflow in a homelab environment.

**Stack:** Next.js, Prisma, PostgreSQL, Docker, GitHub Actions, GHCR, Helm, ArgoCD, k3s, Traefik, cert-manager, Prometheus, Grafana

**What it demonstrates:**

- Built a production-style homelab deployment workflow using immutable Git SHA image tags
- Published `linux/amd64` Docker Buildx images to GHCR through GitHub Actions
- Deployed the app with Helm and ArgoCD into a k3s Kubernetes cluster
- Configured Traefik ingress, cert-manager TLS, and PVC-backed PostgreSQL
- Monitored the stack with Prometheus and Grafana
- Debugged real platform issues including ARM64/AMD64 image mismatch, image pull policy behavior, PVC drift, Prisma migration separation, DNS, ingress, and Grafana troubleshooting

---

### [AWS Secure Web Infrastructure with Terraform](https://github.com/kaybe005/aws-terraform-web-infra)

Secure AWS web infrastructure pattern using Terraform: public ALB to private EC2 with NAT outbound and SSM access.

**Stack:** Terraform, AWS VPC, EC2, ALB, NAT Gateway, IAM, SSM Session Manager, Nginx, security groups, user data

**What it demonstrates:**

- Built a production-style learning architecture with public and private subnet separation
- Deployed 2 public subnets, 2 private subnets, Internet Gateway, NAT Gateway, ALB, target group, and private EC2
- Kept EC2 private with no public IP and managed access through AWS Systems Manager Session Manager instead of SSH
- Used security groups to control traffic between the ALB and private instance
- Automated Nginx bootstrap with `user_data`
- Practiced ALB target group and health check debugging

---

### Full-Stack Application Background

Before shifting into DevOps/cloud, I built full-stack applications with React, Next.js, Node.js, Express, MongoDB, PostgreSQL, Prisma, TypeScript, and Tailwind.

Earlier projects include finance and dashboard-style apps such as Fyntra and Coincise. That background helps me understand the application side of the systems I deploy and operate.

---

## Tech Stack

### Cloud & Infrastructure

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)

### Containers & Orchestration

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat-square&logo=argo&logoColor=white)

### CI/CD & GitOps

![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![GHCR](https://img.shields.io/badge/GHCR-181717?style=flat-square&logo=github&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitOps](https://img.shields.io/badge/GitOps-222222?style=flat-square&logo=git&logoColor=white)

### Networking & Security

![VPC](https://img.shields.io/badge/VPC-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![ALB](https://img.shields.io/badge/ALB-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![NAT Gateway](https://img.shields.io/badge/NAT_Gateway-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![IAM](https://img.shields.io/badge/IAM-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![SSM](https://img.shields.io/badge/SSM_Session_Manager-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Traefik](https://img.shields.io/badge/Traefik-24A1C1?style=flat-square&logo=traefikproxy&logoColor=white)
![cert-manager](https://img.shields.io/badge/cert--manager-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![DNS](https://img.shields.io/badge/DNS-222222?style=flat-square)
![TLS](https://img.shields.io/badge/TLS-222222?style=flat-square)

### Observability

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)

### Application Background

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

---

## What I'm Learning Next

- Deeper AWS networking and IAM patterns
- Terraform modules, remote state, and reusable infrastructure design
- Kubernetes operations and multi-node cluster management
- Monitoring, alerting, incident response, and runbook-style troubleshooting
- Secret management, backup/restore workflows, and disaster recovery basics

---

## GitHub Stats

![Kalash's GitHub stats](https://github-readme-stats.vercel.app/api?username=kaybe005&show_icons=true&hide_border=true&theme=default)

---

## Connect

- Portfolio: [kalashbijukchhe.com](https://kalashbijukchhe.com)
- LinkedIn: [linkedin.com/in/kayb05](https://linkedin.com/in/kayb05)
- Email: [kalashbijukchhe74@gmail.com](mailto:kalashbijukchhe74@gmail.com)
