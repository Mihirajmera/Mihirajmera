# Hi, I'm Mihir Ajmera 👋

<p align="left">
  <a href="https://linkedin.com/in/mihirajmera" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:majmera1@umbc.edu"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://postura.dev" target="_blank"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" /></a>
</p>

### 🛠️ Cloud Security Engineer | AWS Security Architecture | Infrastructure-as-Code | Zero Trust

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

    %% Source Infrastructure Cloud Layer
    subgraph Cloud_Layer [Target Multi-Cloud Environment]
        GD[AWS GuardDuty Alerts] -->|Event Stream| SH[AWS Security Hub]
        CT[CloudTrail Logs] --> SH
    end

    %% Postura Platform Layer
    subgraph Postura_Core [Postura Core Engine]
        SH -->|Webhook Ingestion| Ingest[Ingestion Pipeline]
        Ingest --> Engine[Risk Scoring Engine]
        
        subgraph Compliance_Mapping [Framework Mapping]
            Engine --- NIST[NIST CSF 2.0]
            Engine --- MITRE[MITRE ATT&CK]
        end
        
        Engine -->|State Analysis| Drift[Terraform Patch Generator]
    end

    %% Human in the loop & DevOps Layer
    subgraph Governance [Human-In-The-Loop Flow]
        Drift -->|Webhook Alert| Intercept{UI / Slack Approval}
        Intercept -->|Approved| GH[GitHub Actions CI/CD]
        Intercept -->|Rejected| Drop[Log & Drop Event]
    end

    %% Execution
    GH -->|Terraform Apply| AWS[Remediated AWS Infrastructure]

    %% Class Assignments
    class GD,SH,CT,AWS cloud;
    class Ingest,Engine,Drift engine;
    class NIST,MITRE framework;
    class Intercept,GH,Drop pipeline;
🛡️ Professional Experience & WorkflowsMaryland Public Service Commission — GRC Engineer & AnalystDesigning and driving compliance automation across NIST CSF 2.0, SOC 2, and ISO 27001 frameworks.Achieved a 25% reduction in compliance gaps via automated vulnerability scanning and targeted technical controls.🔄 Continuous GRC & Engineering LifecycleCode snippetgraph LR
    Scan[Vulnerability & Drift Scanning] -->|Identify Gaps| Assess[Risk Evaluation & Framework Mapping]
    Assess -->|Generate Remediation| Orchestrate[Automated Orchestration]
    Orchestrate -->|Deploy Fixes| Verify[Remediation Verification]
    Verify -->|Update Metrics Dashboard| Scan

    style Scan fill:#eceff1,stroke:#455a64,stroke-width:2px
    style Assess fill:#fff9c4,stroke:#fbc02d,stroke-width:2px
    style Orchestrate fill:#ffe0b2,stroke:#f57c00,stroke-width:2px
    style Verify fill:#c8e6c9,stroke:#388e3c,stroke-width:2px
🔧 Technical EcosystemDomainCore Competencies & ToolsCloud & InfrastructureIAM · GuardDuty · Security Hub · VPC Architecture · AWS Lambda · CloudTrail · Systems Manager (SSM) · CloudFormationBackend & Distributed SystemsCelery Task Queues · Event-Driven ArchitecturesFrontend Platform  Security & GRC FrameworksNIST CSF 2.0 · MITRE ATT&CK Matrix · CIS Benchmarks · SOC 2 Type II · ISO 27001DevOps & Engineering OperationsCI/CD Pipelines · Infrastructure Drift Management · GitOps Workflow Implementation🎓 Education & BackgroundMS in CybersecurityUniversity of Maryland, Baltimore County (UMBC) | NSA Center of Academic Excellence (CAE-R/CD)📅 Aug 2024 - May 2026B.Tech in Computer Engineering (Honors in Cybersecurity)St. Francis Institute of Technology📅 2020 - 2024📊 Engineering Activity📫 Connect With MeIf you want to discuss multi-cloud automation architectures, zero-trust infrastructure engineering, or SaaS security patterns, reach out via LinkedIn or send an Email.
