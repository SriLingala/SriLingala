```mermaid
flowchart TD
    A[Users / Internet] --> B[Azure Front Door<br/>WAF + DDoS]
    B --> C[Application Gateway (WAF)<br/>DMZ Subnet]
    C --> D[Azure Firewall (Hub)]
    D --> E[AKS Cluster<br/>Private Subnet<br/>Managed Identity<br/>Autoscaling]
    E --> F[Azure SQL DB<br/>Private Endpoint<br/>TDE + Geo-Replication]
    E --> G[Azure Key Vault<br/>Secrets / Keys / Certificates]
    E --> H[Azure Monitor<br/>Log Analytics<br/>App Insights<br/>Defender for Cloud]
    F --> H
