# Awesome-Enterprise-Security-Compliance-Center

## Top Enterprise Security & Compliance Center Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on CSPM, CNAPP, Runtime Protection & Self-Hosted Security Dashboards*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Enterprise Security & Compliance Centers**. These tools help organizations continuously monitor cloud configurations, detect threats at runtime, and maintain audit-ready compliance across multi-cloud environments—covering everything from native CSPM services to agentless CNAPP platforms and command-line open-source scanners.

**Examples** include Microsoft Defender for Cloud, AWS Security Hub, Google Security Command Center, Wiz, Orca Security, Palo Alto Prisma Cloud, Lacework, Prowler, Trivy, and Falco (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted cloud security posture management, open-source vulnerability scanning, and community-driven runtime protection—ideal for organizations seeking data sovereignty and avoiding per-vCPU or per-resource pricing that compounds at scale. The open-source landscape is genuinely functional: **Prowler** provides a multi-cloud CSPM scanner with 500+ checks under Apache 2.0 [citation:1], **Trivy** covers container and IaC vulnerability scanning [citation:8], and **Falco** delivers eBPF-based runtime threat detection with CNCF graduation [citation:4][citation:9].

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Microsoft Defender for Cloud](https://azure.microsoft.com/en-us/products/defender-for-cloud/)** | **Widest hybrid and multicloud coverage** (Azure, AWS, GCP, and on-premises via Azure Arc) with a functional free foundational CSPM layer . | Foundational CSPM: **free**; Defender CSPM: paid per resource | **Free**: foundational CSPM; paid plans for advanced protection . |
| **[AWS Security Hub](https://aws.amazon.com/security-hub/)** | **Natural choice for AWS-heavy footprints**—deep integration with GuardDuty, Inspector, and Config. **No free tier**; 30-day trial per account . | **No free tier**; usage-priced. Median ~$500–$1,500/month for 50 accounts . | **30-day free trial** per account . |
| **[Google Security Command Center](https://cloud.google.com/security-command-center)** | **Best for Kubernetes-heavy GCP workloads**—specialized detection per workload type in Premium. Standard tier is genuinely useful and free . | Standard: **free**; Premium: ~**$35/project/month** . | **Standard (free)**: useful baseline; **Premium** for advanced detection . |
| **[Wiz](https://www.wiz.io/)** | **Agentless CNAPP with the cleanest UI and fastest setup.** Security graph prioritizes misconfigurations into attack paths. **Trade-off**: runtime protection is still thin, and it is **SaaS-only**—regulated or EU shops needing self-hosted hit a wall . | Quote-only (premium pricing) | No free tier; demo via sales . |
| **[Orca Security](https://orca.security/)** | **Agentless side-scanning for fast, wide coverage from day one.** Reachability filtering shrinks CVE noise instead of just re-sorting it . | AWS Marketplace: Small-Medium tier **$124,440/yr** | No free tier; demo via sales . |
| **[Palo Alto Prisma Cloud](https://www.paloaltonetworks.com/prisma/cloud)** | **Broadest toolset on paper** with mature compliance content and custom policy support. **Trade-off**: operational weight—agents on everything, long rollout, multiple consoles . | Quote-only (enterprise contract) | No free tier; demo via sales . |
| **[Lacework FortiCNAPP](https://www.lacework.com/)** | **Mature behavioral detection via Polygraph** and native integration with the Fortinet portfolio. **Trade-off**: **Lacework's valuation collapsed from $8.3B to $152.3M** before Fortinet acquisition . | AWS Marketplace: **$25,000/12 months** (Standard: 500 vCPU; Pro: 334; Enterprise: 250) . **Higher tiers cost more per vCPU** . | No free tier; demo via sales . |
| **[CrowdStrike Falcon Cloud Security](https://www.crowdstrike.com/)** | Cloud workload protection extending Falcon's endpoint detection to cloud compute, containers, and Kubernetes. | Flex License: **$233.99** (3-year, per license via CDW) | No free tier; trial via sales . |
| **[Datadog Cloud Security](https://www.datadoghq.com/)** | Security monitoring integrated into Datadog's observability platform—CSM Pro, CWS, and Cloud SIEM. | CSM Pro: **$120/host/year**; CWS: **$180/host/year** | No free tier; trial via Datadog . |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Prowler](https://github.com/prowler-cloud/prowler)** | [![Stars](https://img.shields.io/github/stars/prowler-cloud/prowler?style=social&color=white)](https://github.com/prowler-cloud/prowler/stargazers) | **The leading open-source CSPM scanner for multi-cloud environments.** Apache 2.0 licensed, **500+ checks** covering AWS, Azure, GCP, Kubernetes, M365, GitHub, and more. Maps to **CIS, NIST, PCI-DSS, GDPR, HIPAA, SOC 2, and ISO 27001**. Runs with a single command (`pip install prowler && prowler aws`) [citation:1]. **Best for teams wanting a free, auditable CSPM baseline across multiple providers** without per-resource fees. |
| **[Trivy](https://github.com/aquasecurity/trivy)** | [![Stars](https://img.shields.io/github/stars/aquasecurity/trivy?style=social&color=white)](https://github.com/aquasecurity/trivy/stargazers) | **The most widely adopted open-source vulnerability scanner for containers, Kubernetes, code, and cloud.** Detects vulnerabilities, misconfigurations, secrets, and licenses. Apache 2.0. **Scans for vulnerabilities and secrets by default**; license and misconfiguration scanning opt-in [citation:8]. **Best for shift-left security**—scan container images before deploy and catch CVEs early. |
| **[Falco](https://github.com/falcosecurity/falco)** | [![Stars](https://img.shields.io/github/stars/falcosecurity/falco?style=social&color=white)](https://github.com/falcosecurity/falco/stargazers) | **CNCF-graduated runtime security for Kubernetes and containers.** eBPF-based detection of suspicious network connections, file writes, and process executions. **Largest community rule library** among open-source runtime tools; graduated CNCF in February 2024 [citation:4][citation:9]. **Trade-off**: observation-first—requires separate response wiring for blocking actions . **Best for broad, customizable detection coverage** with the most battle-tested starting point . |
| **[Scout Suite](https://github.com/nccgroup/ScoutSuite)** | [![Stars](https://img.shields.io/github/stars/nccgroup/ScoutSuite?style=social&color=white)](https://github.com/nccgroup/ScoutSuite/stargazers) | **Open-source multi-cloud security auditing tool.** CLI with HTML report covering AWS, Azure, and GCP. **Best for quick security assessments** without a full CSPM platform—generates readable reports for audit or initial posture review [citation:1]. |
| **[CloudSploit](https://github.com/aquasecurity/cloudsploit)** | [![Stars](https://img.shields.io/github/stars/aquasecurity/cloudsploit?style=social&color=white)](https://github.com/aquasecurity/cloudsploit/stargazers) | Open-source cloud security scanning for AWS, Azure, GCP, Oracle, and GitHub. Detects misconfigurations and compliance risks. **Best as a lightweight CSPM alternative** for organizations already using Aqua's ecosystem [citation:6]. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[ThreatMapper (Deepfence)](https://github.com/deepfence/ThreatMapper)** | [![Stars](https://img.shields.io/github/stars/deepfence/ThreatMapper?style=social&color=white)](https://github.com/deepfence/ThreatMapper/stargazers) | **Open-source CNAPP** (4,910 stars, Apache-2.0) covering vulnerability scanning, secrets detection, malware scanning, and cloud security posture across containers, hosts, and Kubernetes [citation:10][citation:15]. **Best for teams wanting a broader CNAPP** beyond pure CSPM. |
| **[Tetragon](https://github.com/cilium/tetragon)** | [![Stars](https://img.shields.io/github/stars/cilium/tetragon?style=social&color=white)](https://github.com/cilium/tetragon/stargazers) | **eBPF-native runtime security with in-kernel enforcement.** Can block or kill processes before syscalls complete—unlike Falco's observation-first model. **Best for environments where "stop this action" matters more than "tell me about it"** [citation:4][citation:9]. |
| **[Kubescape](https://github.com/kubescape/kubescape)** | [![Stars](https://img.shields.io/github/stars/kubescape/kubescape?style=social&color=white)](https://github.com/kubescape/kubescape/stargazers) | Open-source Kubernetes security platform covering configuration, vulnerability, compliance, policy, and runtime security [citation:11]. **Best for Kubernetes-specific posture management**. |

**Frameworks for building custom systems**: Choose **Prowler** for multi-cloud CSPM scanning with 500+ compliance-mapped checks [citation:1], **Trivy** for container and IaC vulnerability scanning [citation:8], and **Falco** for eBPF-based runtime threat detection [citation:4][citation:9]—creating a free, self-hosted security stack that covers posture, vulnerabilities, and runtime without per-vCPU licensing.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cloud security platforms require broad read access to cloud APIs and workload metadata; enforce least-privilege IAM roles and audit data access.
- **Pricing models vary dramatically and hidden costs compound.** **Lacework's $25,000/12-month AWS Marketplace floor** has a perverse structure: the vCPU cap **shrinks** as tiers rise (Standard 500, Pro 334, Enterprise 250)—so Enterprise on a 500-vCPU fleet requires **two packs, doubling the annual line** . **AWS Security Hub has no free tier** and costs scale unpredictably with finding volume . **Wiz is SaaS-only**—regulated or EU shops needing self-hosted cannot use it . **Open-source tools are genuinely viable but require assembly**: Prowler covers CSPM across clouds [citation:1], Trivy handles vulnerabilities [citation:8], and Falco catches runtime threats that bypass static scanners [citation:4]. **Validate multi-cloud coverage, runtime detection depth, and total cost of ownership** before committing.

---

**Made for cloud security engineers, SOC analysts, and organizations building multi-cloud defense.**  
Let's make enterprise security and compliance centers more open, observable, and cost-predictable.
