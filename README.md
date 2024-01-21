# Azure_DevOps_AKS_PROJECT_2

1. Create Infra using the file `AZURE-AKS-DEVOPS-INFRA.sh` and give peemissions `chmod 775 AZURE-AKS-DEVOPS-INFRA.sh` and execute it in the Azure CLI


2. Go to dev.azure.com portal


3. Click on New Project -> Project Name - Demo-AKS -> Click on Create


4. Now go to Repos -> Files -> Click on Import in Import a Repository

    Clone URL - `https://github.com/piyushsachdeva/MyHealthClinic-AKS`
    
    Click on Import
    
    
    Install the below from the Organization Settings -> Extensions
    
    - Replace Token
    - Kubernetes extension 


5. Now go to Pipelines -> Pipelines -> Click on Create Pipeline -> Select Azure Repos Git -> Select the Repo name -> 

    Modify the services by clicking on Settings above each task to update the Subscription and Container Registry
    
    `* dapac -Compressed form of DB objects`
    
    Click on Variable add below KV pairs

    ```
    ACR - acrpavan.azurecr.io
    SQLpassword - P2ssw0rd1234
    SQLserver - aks-sqlserver.database.windows.net
    SQLuser - sqladmin
    ```
    Click on Save    


6. Click on Save and Run - Need to give Permit

