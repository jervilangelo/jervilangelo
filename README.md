<div align="center">

<img src="assets/jervil-angelo-banner.svg" alt="Jervil Angelo De Leon — HRIS Technical Support, 2x AWS Certified and 2x OCI Certified. AWS services orbit a floating cloud." width="100%" />

### HRIS Technical Support · 2x AWS Certified & 2x OCI Certified · Cloud & Infrastructure Projects

[![View my portfolio](https://img.shields.io/badge/VIEW_MY_PORTFOLIO-8FA68E?style=for-the-badge&logo=googlechrome&logoColor=1C1C1C)](https://jervilangelo.github.io/de-leon-portfolio/)
[![LinkedIn](https://img.shields.io/badge/LINKEDIN-303030?style=for-the-badge&logo=linkedin&logoColor=F1F1EF)](https://www.linkedin.com/in/jervilangelo/)
[![Email](https://img.shields.io/badge/GET_IN_TOUCH-303030?style=for-the-badge&logo=gmail&logoColor=F1F1EF)](mailto:deleonangelojervil@gmail.com)

**Building my way into the cloud.**

Hands-on projects. Documented decisions. Learning through deployment and recovery.

</div>

## About me

I'm **Jervil Angelo De Leon**, a Philippines-based HRIS Technical Support professional building practical experience in **cloud infrastructure, serverless applications, security, and automation**. I turn real support scenarios and community needs into projects I can deploy, test, and improve.

I'm working toward a **Cloud / Infrastructure Engineering** role, with a focus on **AWS, Terraform, CI/CD, Linux, and reliable operations**.

- 🔭 **Currently shipping:** [Opsentra](https://github.com/jervilangelo/opsentra), an AWS incident response platform with audited, approval-gated recovery
- 🌱 **Learning:** CloudOps, incident management, observability, and least-privilege IAM
- 🛠️ **Also building:** Silong, a Filipino literary refuge for poetry and stories (Next.js + Supabase)

## Latest projects

### Opsentra · CloudOps and incident response for AWS

**Monitor. Detect. Respond. Recover.** A web app that lets an operations team watch AWS workloads, detect an outage, investigate it, and run an approved, audited recovery, with no terminal and no console hopping. An incident closes only when independent health checks prove the service works again, not when a command reports "Success".

- **Event-driven detection:** a probe Lambda feeds a CloudWatch alarm → EventBridge → deduplicated incidents with one SNS alert each, plus a reconciler for missed events.
- **Guarded remediation:** operators request an allowlisted, SHA-256-pinned Systems Manager runbook; an admin approves; it runs exactly once. Roles come from Cognito groups, and every action lands in an append-only audit trail.
- **Least privilege, tested:** Terraform tests pin every IAM policy, IAM Access Analyzer reports no findings, and a live false-success test proves that a "successful" fix which leaves the service down gets escalated.
- **Two modes, never mixed:** a public Demo Mode with labelled synthetic data and zero AWS calls, and an authenticated Live AWS Mode that fails closed.

**AWS:** Lambda · API Gateway · DynamoDB · EventBridge · CloudWatch · SNS · Systems Manager · Cognito · EC2 · S3 · IAM

**Tools:** Terraform · Python · React · TypeScript · pytest · Vitest · Playwright · GitHub Actions

[**Try the live demo →**](https://jervilangelo.github.io/opsentra/) · [Source code and architecture](https://github.com/jervilangelo/opsentra)

### BayanihanDR · Terraform-powered disaster recovery

A disaster recovery proof of concept for Philippine small businesses. It verifies database backups, stores encrypted copies off-site, and uses **Terraform** to provision a temporary AWS recovery environment after operator approval.

- **Infrastructure as code:** Terraform manages standby resources and temporary recovery servers in AWS Singapore.
- **CI/CD:** GitHub Actions checks application code, backup integrity, Terraform, and the dashboard, and deploys the public demo.
- **Measured recovery:** a real AWS drill recovered the sample application in **5 min 29 sec**, with **26 sec of potential data loss**. These are single-run results on synthetic data; off-site uploads currently require an operator session.

**AWS:** EC2 · S3 · IAM · IAM Identity Center · Systems Manager · CloudWatch · AWS Budgets

**Tools:** Terraform · Python · FastAPI · PostgreSQL · Docker · React · GitHub Actions

[![BayanihanDR CI](https://github.com/jervilangelo/bayanihan-dr/actions/workflows/ci.yml/badge.svg)](https://github.com/jervilangelo/bayanihan-dr/actions/workflows/ci.yml)
[![BayanihanDR public site check](https://github.com/jervilangelo/bayanihan-dr/actions/workflows/public-site.yml/badge.svg)](https://github.com/jervilangelo/bayanihan-dr/actions/workflows/public-site.yml)

[**Explore the demo →**](https://jervilangelo.github.io/bayanihan-dr/) · [Source code](https://github.com/jervilangelo/bayanihan-dr) · [Recovery drill evidence](https://github.com/jervilangelo/bayanihan-dr/blob/main/docs/evidence/phase7-disaster-drill.md)

### Teolohiya.site · A serverless book-listing platform

A live platform that helps Filipino readers discover and list Christian theological books. Sellers submit listings and photos; moderators review them before publication; readers contact sellers directly.

- **Serverless backend:** Amplify Gen 2 provisions authentication, a GraphQL API, storage, and backend functions.
- **Access control:** Cognito roles, scoped IAM permissions, and Lambda-controlled moderation protect listings and administrative actions.
- **Delivery:** GitHub-connected Amplify deployments serve the Next.js application over HTTPS.

**AWS:** Amplify · Cognito · AppSync · DynamoDB · S3 · Lambda · CloudFront · ACM · IAM · CDK / CloudFormation

**Tools:** Next.js · TypeScript · Tailwind CSS

[**Visit Teolohiya.site →**](https://teolohiya.site) · [Source code and architecture](https://github.com/jervilangelo/teolohiya-repo)

### PinansyalPH · Financial literacy tools for Filipinos

**Worth it ba sa Pilipinas?** Free, open-source calculators that show the arithmetic behind everyday money decisions, using the same figures the PSA, DOE, Pag-IBIG, BIR, and banks publish.

- **Eight focused pages:** take-home pay (Sweldo), 13th month pay under PD 851, Pag-IBIG MP2, digital bank savings, side-by-side comparison, inflation, and weekly fuel prices.
- **Sourced, dated data:** every figure shows its source, reference period, and retrieval date. Money is computed with decimal.js and rounded only where a real institution would round.
- **Automated data pipeline:** a scheduled GitHub Actions workflow refreshes and validates economic data, commits only real changes, and triggers a fresh deploy.

**Tools:** React 19 · TypeScript · Vite · Tailwind CSS v4 · Vitest · Playwright · GitHub Actions · GitHub Pages

[**Explore PinansyalPH →**](https://jervilangelo.github.io/pinansyalph-v2/) · [Source code and methodology](https://github.com/jervilangelo/pinansyalph-v2)

## AWS services I've used

| Area | Services | Where I applied them |
|---|---|---|
| Compute and networking | **EC2, VPC, Systems Manager** | Recovery infrastructure, Opsentra's lab server and approved runbooks, and a hardened Linux/Nginx web server |
| Serverless APIs | **Lambda, API Gateway, AppSync** | Opsentra's control plane, the HRIS ticketing API, and Teolohiya's listing and moderation workflows |
| Event-driven automation | **EventBridge, SNS** | Alarm-to-incident routing in Opsentra and critical-ticket alerts |
| Data and storage | **S3, DynamoDB** | Verified off-site backups, Terraform state, incidents and audit logs, book photos, listings, and support tickets |
| Identity and access | **IAM, IAM Identity Center, Cognito, IAM Access Analyzer** | Scoped permissions, temporary operator access, role-based approvals, and policy verification |
| Hosting and delivery | **Amplify, CloudFront, ACM** | Teolohiya hosting, content delivery, and managed HTTPS |
| Monitoring and cost | **CloudWatch, AWS Budgets** | Health probes, alarms, operations dashboards, recovery logs, and budget notifications |
| Infrastructure as code | **Terraform, CDK / CloudFormation** | Opsentra and BayanihanDR infrastructure, and Amplify Gen 2 backend resources |

Amplify manages several of Teolohiya's underlying AWS resources. The service list reflects their roles in the deployed application.

## More projects

| Project | What I built |
|---|---|
| [Schedrift](https://github.com/jervilangelo/schedrift) | A local-first tool that turns Microsoft Project (.mpp, .xml, .mpx) files into presentation-ready Gantt charts with critical-path analysis and "what if this task slips?" delay simulation. |
| [ECCM Liturgy Planning](https://github.com/jervilangelo/scheduling-liturgy-system) · [live](https://jervilangelo.github.io/scheduling-liturgy-system/) | A Sunday order-of-worship planner that reads songs live from the church's song list, warns about recently sung songs, applies special-Sunday rules, and keeps versioned plans. |
| [AWS Serverless Ticketing API](https://github.com/jervilangelo/aws-serverless-ticketing-api) | An HRIS support API with ticket tracking, critical-ticket notifications, and monitoring using Lambda, API Gateway, DynamoDB, SNS, and CloudWatch. |
| [Secure EC2 Web Server](https://github.com/jervilangelo/secure-ec2-web-server) | A Linux/Nginx server in a custom VPC with security groups, IAM, and EBS snapshots. |
| [HRIS Template Tracker Automation](https://github.com/jervilangelo/hris-template-tracker-automation-) | Completion tracking across business units using Power Automate, Excel, and Power BI. |
| [ECCM Church Website](https://github.com/jervilangelo/eccm-web) · [live](https://ecc-manila.org/) | A responsive nonprofit website with a custom domain, visitor resources, and SEO essentials. |

## Certifications

<div align="center">

**2x AWS Certified**

<img src="assets/badges/aws-ccp.png" width="125" alt="AWS Certified Cloud Practitioner" /> <img src="assets/badges/aws-ai-practitioner.png" width="125" alt="AWS Certified AI Practitioner" />

**2x Oracle Cloud Infrastructure Certified**

<img src="assets/badges/oci-associate.png" width="125" alt="OCI Foundations Associate" /> <img src="assets/badges/oci-ai.png" width="125" alt="OCI AI Foundations Associate" />

[Explore my certifications and learning journey →](https://jervilangelo.github.io/de-leon-portfolio/certifications)

</div>

Additional training includes Cisco networking and cybersecurity, Google IT Support and System Administration, and IT Specialist: Databases.

## Tools I build with

![AWS](https://img.shields.io/badge/AWS-303030?style=flat-square&logo=amazonwebservices&logoColor=A9BFA8)
![Terraform](https://img.shields.io/badge/Terraform-303030?style=flat-square&logo=terraform&logoColor=A9BFA8)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-303030?style=flat-square&logo=githubactions&logoColor=A9BFA8)
![Docker](https://img.shields.io/badge/Docker-303030?style=flat-square&logo=docker&logoColor=A9BFA8)
![Linux](https://img.shields.io/badge/Linux-303030?style=flat-square&logo=linux&logoColor=A9BFA8)
![Python](https://img.shields.io/badge/Python-303030?style=flat-square&logo=python&logoColor=A9BFA8)
![TypeScript](https://img.shields.io/badge/TypeScript-303030?style=flat-square&logo=typescript&logoColor=A9BFA8)
![React](https://img.shields.io/badge/React-303030?style=flat-square&logo=react&logoColor=A9BFA8)
![Next.js](https://img.shields.io/badge/Next.js-303030?style=flat-square&logo=nextdotjs&logoColor=A9BFA8)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-303030?style=flat-square&logo=postgresql&logoColor=A9BFA8)
![Supabase](https://img.shields.io/badge/Supabase-303030?style=flat-square&logo=supabase&logoColor=A9BFA8)
![Playwright](https://img.shields.io/badge/Playwright-303030?style=flat-square&logo=playwright&logoColor=A9BFA8)
![Git](https://img.shields.io/badge/Git-303030?style=flat-square&logo=git&logoColor=A9BFA8)

## Building in public

[![Jervil Angelo's GitHub contribution activity](https://ghchart.rshah.org/8fa68e/jervilangelo)](https://github.com/jervilangelo?tab=repositories)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/jervilangelo/jervilangelo/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/jervilangelo/jervilangelo/output/github-snake.svg" />
  <img alt="A snake eating my GitHub contribution graph" src="https://raw.githubusercontent.com/jervilangelo/jervilangelo/output/github-snake.svg" width="100%" />
</picture>

<div align="center">

**Explore the projects, architecture decisions, and lessons behind the code.**

[![View my portfolio](https://img.shields.io/badge/EXPLORE_MY_PORTFOLIO-8FA68E?style=for-the-badge&logo=googlechrome&logoColor=1C1C1C)](https://jervilangelo.github.io/de-leon-portfolio/)

[LinkedIn](https://www.linkedin.com/in/jervilangelo/) · [Email](mailto:deleonangelojervil@gmail.com) · [All repositories](https://github.com/jervilangelo?tab=repositories)

</div>
