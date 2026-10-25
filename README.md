<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,45:123B70,100:58A6FF&height=190&section=header&text=CLOUD%20%7C%20DEVOPS%20%7C%20DEVSECOPS&fontSize=27&fontColor=FFFFFF&fontAlignY=38&animation=fadeIn" alt="Animated cloud, DevOps, and DevSecOps banner" />
</p>

<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Righteous&size=35&center=true&vCenter=true&width=540&height=70&duration=2200&pause=800&color=58A6FF&lines=Hello!+%F0%9F%91%8B;I'm+Rahul+Bhatt!" alt="Animated greeting: Hello, I'm Rahul Bhatt" />
</h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&duration=2800&pause=1000&color=58A6FF&center=true&vCenter=true&width=880&height=70&lines=DevOps+%26+DevSecOps+Engineer;Azure+%7C+Terraform+%7C+Kubernetes;Automation+%7C+Security+%7C+Cloud+Operations" alt="Animated DevOps and cloud engineering headline" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Role-DevOps%20%26%20DevSecOps-6f42c1?style=for-the-badge" alt="DevOps and DevSecOps Engineer" />
  <img src="https://img.shields.io/badge/Experience-4%20Years-2ea44f?style=for-the-badge" alt="Four years of experience" />
  <img src="https://img.shields.io/badge/Focus-Azure%20%26%20Kubernetes-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" alt="Azure and Kubernetes focus" />
  <a href="https://github.com/rahulbhatt773">
    <img src="https://img.shields.io/badge/GitHub-rahulbhatt773-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub: rahulbhatt773" />
  </a>
</p>

<p align="center">
  <a href="#about-me">About</a> ·
  <a href="#delivery-map">Delivery Map</a> ·
  <a href="#technology-stack">Technology Stack</a> ·
  <a href="#portfolio-projects">Projects</a> ·
  <a href="#devsecops-approach">DevSecOps</a> ·
  <a href="#current-focus">Current Focus</a> ·
  <a href="#connect">Connect</a>
</p>

---

## 👋 About Me

I’m a **DevOps & DevSecOps Engineer** with four years of experience across cloud infrastructure, automation, and CI/CD. I work primarily with **Microsoft Azure and Terraform**, building practical infrastructure examples around networking, secure cloud resources, and Kubernetes.

I care about keeping infrastructure changes understandable, automating repeatable checks, and considering security and operations throughout delivery. I’m also exploring **Agentic AI** and **Cloud FinOps** as areas of interest.

## 🧭 Portfolio Delivery Map

An enterprise-oriented reference flow showing how my key skills fit together, from a reviewed infrastructure change to secure platform operations. This is an architecture view, not a claim that the portfolio labs deploy these systems: their workflows validate and scan Terraform; they **do not deploy cloud resources**.

```mermaid
flowchart TB
    subgraph GOV["01 · Governance and platform foundation"]
        direction LR
        OWN["Teams and workload requirements"]
        CLOUD["Azure · AWS · GCP"]
        IAC["Terraform modules<br/>Ansible automation"]
        OWN --> CLOUD --> IAC
    end

    subgraph DELIVERY["02 · Secure change and delivery"]
        direction LR
        PR["Git pull request"]
        PIPE["GitHub Actions<br/>Azure Pipelines"]
        CHECKS["Quality and security checks<br/>fmt · validate · TFLint<br/>Gitleaks · tfsec · Checkov"]
        APPROVE["Review and approval"]
        PR --> PIPE --> CHECKS --> APPROVE
    end

    subgraph PLATFORM["03 · Cloud and Kubernetes platform"]
        direction LR
        FOUNDATION["Cloud foundation<br/>network · identity · policy"]
        CONTAINERS["Docker images"]
        K8S["Kubernetes / AKS"]
        GITOPS["Argo CD<br/>GitOps reconciliation"]
        FOUNDATION --> K8S
        CONTAINERS --> K8S
        GITOPS --> K8S
    end

    subgraph OPERATE["04 · Operate, secure, and optimize"]
        direction LR
        OBS["Azure Monitor<br/>Prometheus · Grafana"]
        SECURE["DevSecOps controls<br/>Key Vault · least privilege"]
        FINOPS["Cloud FinOps<br/>cost visibility · right-sizing"]
        FEEDBACK["Operational feedback"]
        K8S --> OBS
        K8S --> SECURE
        CLOUD --> FINOPS
        OBS --> FEEDBACK
        SECURE --> FEEDBACK
        FINOPS --> FEEDBACK
    end

    IAC --> PR
    APPROVE --> FOUNDATION
    APPROVE --> GITOPS
    FEEDBACK -. "inform future changes" .-> OWN

    AI["Agentic AI exploration<br/>assistive suggestions · human review"]
    AI -. "optional, human-approved input" .-> PR

    classDef governance fill:#10243A,stroke:#58A6FF,color:#FFFFFF
    classDef delivery fill:#172554,stroke:#818CF8,color:#FFFFFF
    classDef platform fill:#123524,stroke:#34D399,color:#FFFFFF
    classDef operations fill:#2A1B3D,stroke:#C084FC,color:#FFFFFF
    classDef ai fill:#3A2A12,stroke:#FBBF24,color:#FFFFFF
    class OWN,CLOUD,IAC governance
    class PR,PIPE,CHECKS,APPROVE delivery
    class FOUNDATION,CONTAINERS,K8S,GITOPS platform
    class OBS,SECURE,FINOPS,FEEDBACK operations
    class AI ai
```

## 🧰 Technology Stack

| Area | Tools and technologies |
| --- | --- |
| ☁️ Cloud | Microsoft Azure, AWS, GCP |
| 🏗️ Infrastructure as Code | Terraform, Ansible |
| 📦 Containers and orchestration | Docker, Kubernetes, AKS |
| 🔁 CI/CD and GitOps | GitHub Actions, Azure Pipelines, Azure DevOps, Argo CD, Git |
| 🔐 Infrastructure security | Gitleaks, TFLint, tfsec, Checkov, Azure Key Vault |
| 📊 Monitoring and scripting | Prometheus, Grafana, Azure Monitor, Bash, Linux |
| 🧪 Current interests | Agentic AI, infrastructure automation, Cloud FinOps |

<p align="center">
  <img src="https://skillicons.dev/icons?i=azure,aws,gcp,terraform,ansible,docker,kubernetes,githubactions,git,prometheus,grafana,bash,linux" alt="Cloud, infrastructure, container, CI, monitoring, and scripting tools" />
</p>

## 🚀 Portfolio Projects

These projects demonstrate Terraform module composition and CI validation patterns. They are learning examples, not production deployments; review prerequisites and environment-specific requirements before adapting them.

### ☁️ Azure Foundation

A Terraform root module that composes a network child module.

- Creates a virtual network with configurable subnets.
- Associates network security groups with subnets.
- Demonstrates reusable module inputs and outputs.
- Includes CI checks for formatting, validation, linting, and IaC configuration.

### 🌐 Hub-and-Spoke Network

A modular example for connecting hub and spoke virtual networks.

- Uses reusable VNet child modules for the hub and spokes.
- Configures bidirectional network peering.
- Leaves routing, firewall, gateway, and production-specific controls to the target design.

### 🔐 Secure Data Platform

A Terraform example that composes separate Storage Account and Key Vault modules.

- Keeps storage and secrets resources in their own child modules.
- Documents secure defaults and access prerequisites.
- Requires a suitable network and access design before adaptation.

### ☸️ AKS Platform

A network and AKS module composition for a private-cluster-oriented baseline.

- Uses managed identity and Azure RBAC.
- Configures an autoscaling system node pool.
- Includes GitHub Actions and Azure Pipelines validation definitions.
- Needs environment-specific review of access, networking, and operations.

## 🔒 DevSecOps Approach

I aim to make security checks part of the normal development workflow, with results that engineers can review and act on.

- **Review infrastructure changes:** Check Terraform plans and configuration changes before applying them.
- **Run checks early:** Use formatting, validation, linting, and IaC scans during CI.
- **Protect secrets:** Use secret-scanning tools and keep credentials and state out of source control.
- **Use scoped access:** Prefer permissions appropriate to the pipeline or task.
- **Make requirements visible:** Document network access, prerequisites, and limitations.
- **Keep examples honest:** Clearly distinguish portfolio labs from production-ready platform designs.

## 🛠️ How I Work

1. **Understand the requirement** — clarify the environment, constraints, and intended outcome.
2. **Model the change** — keep infrastructure definitions version-controlled and modular where useful.
3. **Validate automatically** — run repeatable checks before a change is considered ready.
4. **Review the impact** — look for unexpected changes and security or access implications.
5. **Improve from feedback** — use operational lessons to make modules and workflows clearer.

## 🎯 Current Focus

- Building a stronger portfolio of Azure and Terraform infrastructure examples.
- Improving reusable module patterns and CI validation workflows.
- Learning more about Kubernetes platform operations and observability.
- Exploring safe, reviewable uses of Agentic AI in DevOps workflows.
- Keeping cloud cost awareness alongside reliability and security considerations.

## 📈 GitHub Activity

<p align="center">
  <img width="49%" src="https://github-readme-stats.vercel.app/api?username=rahulbhatt773&show_icons=true&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=58A6FF&text_color=C9D1D9" alt="GitHub activity statistics" />
  <img width="49%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=rahulbhatt773&layout=compact&hide_border=true&bg_color=0D1117&title_color=58A6FF&text_color=C9D1D9" alt="Most-used programming languages" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=rahulbhatt773&bg_color=0D1117&color=58A6FF&line=58A6FF&point=FFFFFF&area=true&hide_border=true" alt="GitHub contribution activity graph" width="95%" />
</p>

## 🤝 Connect

Interested in cloud infrastructure, DevOps, DevSecOps, or automation? Explore my repositories and connect on [GitHub](https://github.com/rahulbhatt773).

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:58A6FF,50:1F6FEB,100:0D1117&height=100&section=footer" alt="Blue wave footer" />
</p>
