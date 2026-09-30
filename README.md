# Theron Bueno

**Site Reliability Engineer · Platform** · AWS · EKS · Terraform · Networking · Observability · UTC+8

I find the actual failure mechanism in production problems, then change the system so it's less likely to recur. SRE at a digital bank, with a software engineering background and 7+ years building and running production systems.

**Open to senior SRE and platform roles, employee or long-term contract** · [Email me](mailto:prodev.theron@gmail.com)

## Selected evidence

- **Cut ELB 504s by >99%** (from ~22/hour to ~0.06/hour) after analyzing ~13.6M load-balancer log lines and finding an ALB↔Envoy idle-timeout mismatch. Later rounds found Istio retry behavior and frontend resource limits. A September regression is still under investigation, and its leading hypothesis is not yet proven.
- **Owned a Sev-2 I caused.** A stale Terraform branch auto-applied to production and destroyed 16 network resources. I wrote the postmortem and drove approvals and branch protection across 5 IaC repos, taking peer-approved merges from 25% (7/28) to 100% (13/13).
- **Migrated release publishing for 8 services to ECR.** Tag validation caught 6 release defects before release, and 23 non-production workloads were cut over with digest checks and automatic rollback. Production cutover is in progress.
- **Upgraded MySQL 8.0 → 8.4** across test, staging, and production, with pre-checks, runbooks, and a snapshot rollback plan. **Upgraded four EKS clusters 1.32 → 1.34** and wrote the runbook.
- **Mail relays (~1.2M requests/day):** traced a 22 GB disk exhaustion to ~15M deferred-message log entries, added hourly rotation, and rolled out DKIM/SPF-signed relays with weighted DNS.
- **Contract on-call (legal tech SaaS):** 3.7-minute median alert acknowledgement vs the team's 6.0 across 277 alerts, and 69 production changes run through change requests.

## How I think

I use mental models, Charlie Munger's latticework, as everyday tools. Each one changed a real decision:

| Principle | Model | Where it paid off |
| --- | --- | --- |
| Evidence before certainty | Map is not the territory | Stated a latency regression's leading cause as a hypothesis after ruling out deploys, routing, DB, Redis, and node pools. No production change on an unproven cause. |
| Find the mechanism | First principles | 504s came from mismatched load-balancer and proxy idle timeouts. ELB 504s fell >99%. |
| Ask how it happens again | Inversion | After my own incident, I built controls, not just a fix: 5 repos protected, 100% peer-approved merges. |
| Leave a way back | Margin of safety | Registry cutovers with digest checks and automatic rollback; one rollback, then a clean retry. |
| And then what? | Second-order thinking | ~$22.5k/year of tagged cost in a decommission, but $0 realizable compute savings given scheduler and Karpenter behavior. No overstated business case. |
| Fix the system, not the symptom | Feedback loops | Replaced queue purging with a root-cause fix and hourly log rotation on the mail relays. |

## What colleagues noticed

- Pairs technical analysis with a **recommended next step** for customers, which a teammate proposed making a team standard.
- Fixed the **underlying mail relay issue** instead of the usual queue purging (internal "Achiever" recognition).
- Solves problems **with little context, quickly** (internal "Quick Thinker" recognition).

> "I'm incredibly grateful to my mentor, Theron Bueno, for an insightful and inspiring six-month mentorship." **Christian Ortiz**, mentored through ULAP.org

## Experience

**Site Reliability Engineer, Digital bank** · Dec 2025 – present\
AWS, EKS, Karpenter, Istio/Envoy, Terraform, ECR, RDS MySQL, ElastiCache Redis, Transit Gateway, Dynatrace, Postfix

**DevOps / Support Engineer (Contract), Legal tech SaaS company**\
Azure, Azure DevOps, Squadcast, Salesforce. Built a pipeline watcher that only retries safe failure classes and a ticketing agent where every write needs human approval.

**Site Reliability Engineer, ING Hubs Philippines** · Dec 2024 – Dec 2025\
Azure, RHEL, OpenShift, Elastic Stack, LGTM, Ansible

**Backend Engineer, ING Hubs Philippines** · Dec 2023 – Dec 2024\
Java, Spring Boot, Node.js, Go

**Freelance Full-Stack Developer** · 2018 – 2023\
Web applications for 30+ clients with React, Next.js, Node.js, and Nuxt

## Writing

Two production postmortems (one for an incident I caused), the team RCA template, EKS and MySQL upgrade runbooks, a Flagger progressive-delivery guide, and critical user journey docs.

## Side project

**[tugtogbytes](https://tugtogbytes.vercel.app)**, a live set-prep app for gigging musicians. I build it with AI coding agents and own the reliability layer myself:

- Every pull request is gated by browser tests against a production build. I cut CI from 5m50s to under 4 minutes after tracing a stall to a package mirror serving 105 kB/s.
- **Production probe with AI triage:** synthetic checks against two SLOs every 3 hours and after each deploy. On failure, Claude reads the failed checks, recent deploys, and commits, and writes a likely cause into one incident issue. It's advisory only and never rolls back or changes anything.

## Certifications

AWS Certified Cloud Practitioner · Microsoft Azure Developer Associate (AZ-204) · Microsoft Azure Fundamentals (AZ-900) · Google IT Support Professional

BS Computer Engineering, Pamantasan ng Lungsod ng Maynila (2023) · ULAP.org cloud scholar, now a mentor

[LinkedIn](https://linkedin.com/in/prodev-theron) · [Email](mailto:prodev.theron@gmail.com) · [Portfolio source](https://github.com/proDev-Theron/nextjs-portfolio-website)
