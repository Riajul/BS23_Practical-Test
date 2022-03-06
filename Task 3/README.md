# Microservice App Structure and Management

**Environments:**
- Env: Azue and On-premise
- Version Control: GitHub
- CI/CD: Azure DevOps
- Automation Test: Selenium/Robot Framework
- Log Management: ELK Stack
- Monitoring: Zabbix

**Components:**
- Terraform files for IAC
- Azure DevOps for pipelines
- Azure Virtual Network
- On Premise Virtual Network
- Virtual Network Peering
- Network Security Group
- SQL database With EndPoint
- Azure Key Vault
- Azure Kubernetes Service
- Azure Application Gateway
- Azure VPN Gateway

**Implementation:**
- Modular wise Terraform Files for Infrastructure Deployment.
- In Azure DevOps create Infra pipeline to deploy infrastructure.
- After infra deploy create Virtual Network Peering.
- Azure Kubernetes and Ingress Controller installed within Azure Kubernetes Service.
- Implement Database server within End point in Azure.
- Application build in Azure pipeline and deploy using Release pipeline.
- Selenium/Robot Framework test automation script for Sanity test.
- Install a zabbix server and install zabbix agent for server and service monitoring.
- Create discovery rules zabbix.
- Install ELK stack for log management and filebeat.
- Create index pattern in ELK.

**Access Services:**
- We will use FrontEnd IP in Azure Application Gateway and User will use this IP to access the Application/Services.
- In backend Pool of Azure Application Gateway, All Microservice VM IP will be added.



