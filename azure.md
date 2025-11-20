flowchart TD

    A[Users / Internet] --> B[Azure Front Door]

    B --> C[Application Gateway WAF  
    DMZ Subnet]

    C --> D[Azure Firewall  
    Hub VNet]

    D --> E[AKS Cluster  
    Private Subnet  
    Managed Identity  
    Autoscaling]

    E --> F[Azure SQL Database  
    Private Endpoint  
    TDE + Geo-Replication]

    E --> G[Azure Key Vault  
    Secrets and Keys]

    E --> H[Azure Monitor  
    Log Analytics  
    App Insights  
    Defender for Cloud]

    F --> H
