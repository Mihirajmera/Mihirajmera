<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0288d1,100:388e3c&height=200&section=header&text=Mihir%20Ajmera&fontSize=48&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=GRC%20Engineer%20%7C%20Cloud%20Security%20%7C%20NIST%20CSF%20%7C%20Zero%20Trust&descAlignY=55&descSize=18" width="100%"/>
</p>

<p align="center">
  <a href="https://linkedin.com/in/mihirajmera" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:majmera1@umbc.edu"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://postura.dev" target="_blank"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" /></a>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=0288D1&center=true&vCenter=true&width=700&lines=GRC+Engineer+%40+American+Express;Founder+%26+CTO+of+Postura;NIST+CSF+2.0+%7C+SOX+ITGC+%7C+PCI-DSS+Compliance+Automation;AWS+Security+Architecture+%7C+Zero+Trust+%7C+IaC" alt="Typing SVG" />
</p>

I am a Cybersecurity Graduate Student and the **Founder & CTO of Postura**. I specialize in building autonomous multi-cloud security remediation platforms, orchestrating event-driven AWS security automation, and implementing continuous compliance lifecycles.

> *"Securing systems isn't just about detecting threats — it's about automating remediation at scale."*

---

## 🚀 Featured Project: Postura
**Autonomous Multi-Cloud Security Remediation Platform**
*Real-time threat ingestion, risk scoring mapped to industry frameworks, and human-in-the-loop automated IaC drift repair.*

### 📐 System Architecture & Remediation Workflow

```mermaid
graph TD
    %% Styling Definitions
    classDef cloud fill:#fdf6e2,stroke:#ff9900,stroke-width:2px;
    classDef engine fill:#e1f5fe,stroke:#0288d1,stroke-width:2px;
    classDef framework fill:#efebe9,stroke:#5d4037,stroke-width:2px;
    classDef pipeline fill:#e8f5e9,stroke:#388e3c,stroke-width:2px;

    subgraph Cloud_Layer [Target Multi-Cloud Environment]
        GD[AWS GuardDuty Alerts] -->|Event Stream| SH[AWS Security Hub]
        CT[CloudTrail Logs] --> SH
    end

    subgraph Postura_Core [Postura Core Engine]
        SH -->|Webhook Ingestion| Ingest[Ingestion Pipeline]
        Ingest --> Engine[Risk Scoring Engine]

        subgraph Compliance_Mapping [Framework Mapping]
            Engine --- NIST[NIST CSF 2.0]
            Engine --- MITRE[MITRE ATT&CK]
        end

        Engine -->|State Analysis| Drift[Terraform Patch Generator]
    end

    subgraph Governance [Human-In-The-Loop Flow]
        Drift -->|Webhook Alert| Intercept{UI / Slack Approval}
        Intercept -->|Approved| GH[GitHub Actions CI/CD]
        Intercept -->|Rejected| Drop[Log & Drop Event]
    end

    GH -->|Terraform Apply| AWS[Remediated AWS Infrastructure]

    class GD,SH,CT,AWS cloud;
    class Ingest,Engine,Drift engine;
    class NIST,MITRE framework;
    class Intercept,GH,Drop pipeline;
```

## 📌 Featured Projects

<p align="center">
  <a href="https://github.com/Mihirajmera/control-gap-analyzer"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Mihirajmera&repo=control-gap-analyzer&theme=tokyonight&hide_border=true" /></a>
  <a href="https://github.com/Mihirajmera/grc-risk-dashboard"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Mihirajmera&repo=grc-risk-dashboard&theme=tokyonight&hide_border=true" /></a>
</p>
<p align="center">
  <a href="https://github.com/Mihirajmera/itgc-evidence-automation"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Mihirajmera&repo=itgc-evidence-automation&theme=tokyonight&hide_border=true" /></a>
  <a href="https://github.com/Mihirajmera/guardduty-siem-automation"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Mihirajmera&repo=guardduty-siem-automation&theme=tokyonight&hide_border=true" /></a>
</p>
<p align="center">
  <a href="https://github.com/Mihirajmera/iam-zero-trust-security"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Mihirajmera&repo=iam-zero-trust-security&theme=tokyonight&hide_border=true" /></a>
  <a href="https://github.com/Mihirajmera/secure-vpc-architecture"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Mihirajmera&repo=secure-vpc-architecture&theme=tokyonight&hide_border=true" /></a>
</p>

## 🛡️ Professional Experience & Workflows

**American Express — GRC Engineer** *(Jun 2025 – Present)*
- Run technology risk and security control assessments across payment and enterprise platforms using ServiceNow GRC and NIST CSF 2.0, reducing high-risk findings through prioritized remediation.
- Test and validate controls against NIST SP 800-53 Rev. 5 and PCI-DSS v4.0, improving audit readiness across 120+ security controls.
- Maintain enterprise risk registers in RSA Archer; partnered with technology teams to cut overdue risk items by 20%.
- Built executive risk/compliance dashboards in SQL and Power BI for KRI, control health, and remediation visibility.

**KPMG — GRC Engineer** *(Jan 2022 – Jul 2024)*
- Monitored 200+ security controls across banking operations against FFIEC, SOX, PCI-DSS, and NIST CSF using ServiceNow GRC.
- Conducted ITGC testing (SailPoint, Active Directory) covering access reviews, change management, and segregation of duties for SOX compliance.

### 🔄 Continuous GRC & Engineering Lifecycle

```mermaid
graph LR
    Scan[Vulnerability & Drift Scanning] -->|Identify Gaps| Assess[Risk Evaluation & Framework Mapping]
    Assess -->|Generate Remediation| Orchestrate[Automated Orchestration]
    Orchestrate -->|Deploy Fixes| Verify[Remediation Verification]
    Verify -->|Update Metrics Dashboard| Scan

    style Scan fill:#eceff1,stroke:#455a64,stroke-width:2px
    style Assess fill:#fff9c4,stroke:#fbc02d,stroke-width:2px
    style Orchestrate fill:#ffe0b2,stroke:#f57c00,stroke-width:2px
    style Verify fill:#c8e6c9,stroke:#388e3c,stroke-width:2px
```

## 🔧 Technical Ecosystem

| Domain | Core Competencies & Tools |
|---|---|
| GRC & Risk Tools | ServiceNow GRC · RSA Archer · Qualys · SailPoint IdentityIQ · Jira · Confluence |
| Security Frameworks & Standards | NIST CSF 2.0 · NIST SP 800-53 Rev. 5 · PCI-DSS v4.0 · ISO 27001 · SOX ITGC · FFIEC · CIS Controls |
| Cloud & Infrastructure | IAM · GuardDuty · Security Hub · VPC Architecture · AWS Lambda · CloudTrail · AWS Config · Azure Policy |
| Data & Reporting | SQL · Power BI · Microsoft Excel · Risk Dashboards · KRI/KPI Analysis |
| DevOps & Engineering Operations | CI/CD Pipelines · Infrastructure Drift Management · GitOps Workflow Implementation |

### 🎖️ Certifications

- Google Cybersecurity Professional
- CompTIA Security+ (SY0-701)
- AWS Certified Solutions Architect – Associate *(in progress)*

<p align="left">
  <img src="https://skillicons.dev/icons?i=aws,terraform,py,ts,react,js,docker,githubactions,linux,git" />
</p>

## 🎓 Education & Background

**MS in Cybersecurity**
University of Maryland, Baltimore County (UMBC) | NSA Center of Academic Excellence (CAE-R/CD)
📅 Aug 2024 - May 2026

**B.Tech in Computer Engineering (Honors in Cybersecurity)**
St. Francis Institute of Technology
📅 2020 - 2024

## 📊 Engineering Activity

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Mihirajmera&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" height="165"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Mihirajmera&layout=compact&theme=tokyonight&hide_border=true" height="165"/>
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Mihirajmera&theme=tokyonight&hide_border=true" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Mihirajmera&theme=tokyo-night&hide_border=true" width="100%"/>
</p>

<!--START_SECTION:waka-->
<!-- snake animation renders here once the .github/workflows/snake.yml action runs -->
<p align="center">
  <img src="https://raw.githubusercontent.com/Mihirajmera/Mihirajmera/output/github-contribution-grid-snake-dark.svg" width="100%" alt="contribution snake animation"/>
</p>
<!--END_SECTION:waka-->

## 🏆 Trophies

<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=Mihirajmera&theme=tokyonight&no-frame=true&column=7&margin-w=8" />
</p>

## 📫 Connect With Me

If you want to discuss multi-cloud automation architectures, zero-trust infrastructure engineering, or SaaS security patterns, reach out via LinkedIn or send an Email.

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:388e3c,100:0288d1&height=100&section=footer" width="100%"/>
</p>
