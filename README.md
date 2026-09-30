# Theron Bueno

**Site Reliability Engineer for fintech and regulated SaaS** · AWS · Azure · Kubernetes · Observability · AIOps · Metro Manila, Philippines

I keep production systems up and make every change safe and auditable. SRE at a digital bank. Previously SRE and backend engineer at ING.

**Available for remote SRE contracts · UTC+8** · [Email me](mailto:prodev.theron@gmail.com)

## Highlights

- **Recovered 130,000+ stuck transactional emails in 90 minutes, with none lost,** during an SMTP outage. I tuned Postfix concurrency and worker allocation and worked through the queue in targeted batches.
- **Eliminated intermittent 504s at the production ingress.** I traced them to an ALB/Istio idle timeout mismatch and shipped a mesh-wide proxy fix through Terraform with zero downtime.
- **Upgraded EKS with zero downtime** through an automated two-phase rollout using Terraform and Karpenter disruption budgets.
- **Responded to production alerts in a 3.7-minute median vs the team's 6.0 minutes** across 277 alerts while on call for a legal tech SaaS platform.
- **Ran 69 production changes through change management** (38 deployments, 9 emergency changes), each with a change request and recorded outcome; about 6% rolled back safely.
- **Expanded Dynatrace coverage and proactive alerting** on critical banking services so incidents are caught earlier.
- **Made Elastic Stack upgrades safe across 100+ nodes** with Ansible tasks that check cluster health before applying changes. I also reordered shard allocation and node shutdown to stabilize DR exercises.
- **Closed security findings:** remediated flagged vulnerabilities across 100+ RHEL VMs and resolved all high-severity code-scan findings in three Go services.

## AI-assisted ops tooling I built

- **Azure DevOps pipeline watcher:** monitors multi-hour deployment pipelines, classifies failed stages (timeout, transient, data validation, fatal), and auto-retries only the safe ones. It never reruns real migration errors.
- **Salesforce ops agent:** works cases, incidents, and change requests from a pasted link. Every write needs explicit human approval, enforced by tool permissions rather than instructions.
- **Squadcast metrics pipeline:** read-only API export that works within the 1,000-incident and 6-month limits, checks attribution against raw logs, and outputs aggregates only.

## How I think

I use mental models, the latticework Charlie Munger describes, as everyday working tools. Where each one paid off:

| Model | How I applied it | Result |
| --- | --- | --- |
| **Inversion**: ask how it fails, then prevent that | Listed how customer traffic could drop during EKS upgrades and capped node disruption per workload | Zero-downtime upgrades |
| **First principles**: fix the cause, not the symptom | Traced random 504s to mismatched ALB and Istio idle timeouts, fixed at the root mesh-wide | 100% of those errors gone |
| **Second-order thinking**: ask "and then what?" | Released 130,000 queued emails in controlled batches instead of all at once | All delivered in 90 minutes, none lost |
| **Margin of safety**: leave room for being wrong | AI ops tools can't write without human approval; upgrades run only after health checks pass | 100+ nodes upgraded safely |
| **Checklists**: make the safe path the default | Every production change followed the same plan, window, rollback, and recorded outcome | 69 changes, about 6% rolled back safely |
| **The map is not the territory**: check the source | Verified on-call attribution against raw logs before publishing any number | On-call numbers checked against raw logs |

## Start here

A fixed-price **2-week reliability review**: architecture walkthrough, a look at your alerts, incidents, and change process, then a written report ranking your top risks by business impact, plus fixes for the quick wins. Continue monthly if it's useful. [Ask about a review](mailto:prodev.theron@gmail.com?subject=Reliability%20review)

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