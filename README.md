# Azure_DevOps_AKS_2

1. Go to dev.azure.com portal


2. Click on New Project -> Project Name - Demo-AKS -> Click on Create


3. Now go to Repos -> Files -> Click on Import in Import a Repository

    Clone URL - `https://github.com/piyushsachdeva/MyHealthClinic-AKS`
    
    Click on Import
    
    
    Install the below from the Organization Settings -> Extensions
    
    - Replace Token
    - Kubernetes extension 


4. Now go to Pipelines -> Pipelines -> Click on Create Pipeline -> Select Azure Repos Git -> Select the Repo name -> 

Modify the services by clicking on Settings above each task to update the Subscription and Container Registry

`* dapac -Compressed form of DB objects`

Click on Variable add below KV pairs

ACR - acrpavan.azurecr.io
SQLpassword - P2ssw0rd1234
SQLserver - aks-sqlserver.database.windows.net
SQLuser - sqladmin

Click on Save


5. Click on Save and Run - Need to give Permit

