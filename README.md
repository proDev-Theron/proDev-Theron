# Theron Bueno

**Site Reliability Engineer** · Kubernetes · AWS · Azure · OpenShift · Observability · AIOps · Metro Manila, Philippines

I keep production systems up for banks and SaaS platforms. SRE at a digital bank. Previously SRE and backend engineer at ING.

**Available for remote SRE contracts · UTC+8** · [Email me](mailto:prodev.theron@gmail.com)

## Highlights

- **Recovered 130,000+ stuck transactional emails in 90 minutes, with none lost,** during an SMTP outage. I tuned Postfix concurrency and worker allocation and worked through the queue in targeted batches.
- **Eliminated intermittent 504s at the production ingress.** I traced them to an ALB/Istio idle timeout mismatch and shipped a mesh-wide proxy fix through Terraform with zero downtime.
- **Upgraded EKS with zero downtime** through an automated two-phase rollout using Terraform and Karpenter disruption budgets.
- **Acknowledged 277 production alerts with a 3.7-minute median, 38% faster than the team median,** mostly on after-hours on-call for a legal tech SaaS platform.
- **Executed 69 production change requests** (38 deployments, 9 emergency changes): 88% successful, about 6% rolled back.
- **Closed 128 cloud service requests** (access grants, decommissions, database refreshes), 70% within 7 days.
- **Expanded Dynatrace coverage and proactive alerting** on critical banking services so incidents are caught earlier.
- **Made Elastic Stack upgrades safe across 100+ nodes** with Ansible tasks that check cluster health before applying changes. I also reordered shard allocation and node shutdown to stabilize DR exercises.
- **Closed security findings:** remediated flagged vulnerabilities across 100+ RHEL VMs and resolved all high-severity code-scan findings in three Go services.

## AI-assisted ops tooling I built

- **Azure DevOps pipeline watcher:** monitors multi-hour deployment pipelines, classifies failed stages (timeout, transient, data validation, fatal), and auto-retries only the safe ones. It never reruns real migration errors.
- **Salesforce ops agent:** works cases, incidents, and change requests from a pasted link. Every write needs explicit human approval, enforced by tool permissions rather than instructions.
- **Squadcast metrics pipeline:** read-only API export that works within the 1,000-incident and 6-month limits, checks attribution against raw logs, and outputs aggregates only.

## Experience

**Site Reliability Engineer, Digital bank** · Dec 2025 – present\
AWS (EKS, EC2), Kubernetes, Karpenter, Istio, Terraform, Dynatrace, AWS DevOps Agent and AI-assisted operations, Postfix, GitLab CI

**Site Reliability Engineer, ING Hubs Philippines** · Dec 2024 – Dec 2025\
Azure, RHEL, OpenShift, Elastic Stack (ELK), LGTM (Loki, Grafana, Tempo, Mimir), Ansible, disaster recovery planning and execution, capacity management, alert routing to Microsoft Teams

**Backend Engineer, ING Hubs Philippines** · Dec 2023 – Dec 2024\
Java (Spring Boot, Vaadin), Node.js, Go, REST APIs, application security remediation

**DevOps / Support Engineer (Contract), Legal tech SaaS company**\
On-call for an Azure-hosted SaaS platform used by law firms: resolved Squadcast alerts and production incidents, ran change requests in maintenance windows, deployed through Azure DevOps pipelines, managed access, and worked cases in Salesforce

**Freelance Full-Stack Developer** · Jan 2018 – Sep 2023\
Built, deployed, and maintained web apps for 30+ clients with React, Next.js, Vue/Nuxt, and Node.js

## Stack

| Area | Tools |
| --- | --- |
| Cloud and containers | Linux (RHEL), AWS (EKS, EC2), Azure, Kubernetes, OpenShift, Karpenter, Istio, Docker |
| Infrastructure as code | Terraform, Ansible |
| CI/CD | GitLab CI, GitHub Actions, Azure DevOps |
| Observability | Dynatrace, Elastic Stack (ELK), LGTM (Loki, Grafana, Tempo, Mimir) |
| Incident management | Squadcast, Salesforce |
| Languages | Python, Bash, Go, Java (Spring Boot), Node.js |
| AI and AIOps | AWS DevOps Agent, Claude, GitHub Copilot, Cursor |

## Certifications

AWS Certified Cloud Practitioner · Microsoft Azure Developer Associate (AZ-204) · Microsoft Azure Fundamentals (AZ-900) · Google IT Support Professional

## Also

- **BS Computer Engineering, Pamantasan ng Lungsod ng Maynila (2023)**
- **Mentor at ULAP.org (2024 – present).** I help early-career developers get their first engineering roles.

## Contact

[LinkedIn](https://linkedin.com/in/prodev-theron) · [Email](mailto:prodev.theron@gmail.com) · [Portfolio source](https://github.com/proDev-Theron/nextjs-portfolio-website)