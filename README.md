# Azure_DevOps_AKS_PROJECT_2 
  
1. Create Infra using the file `AZURE-AKS-DEVOPS-INFRA.sh` and give peemissions `chmod 775 AZURE-AKS-DEVOPS-INFRA.sh` and execute it in the Azure CLI

![AKS](https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/assets/32020205/85f60772-3a4d-4880-ac57-39e31c983714)

![AKS-CONNECT](https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/assets/32020205/b1f0b673-2979-4bee-b8bc-6b8545b8e827)


2. Go to dev.azure.com portal


3. Click on New Project -> Project Name - Demo-AKS -> Click on Create


4. Now go to Repos -> Files -> Click on Import in Import a Repository

    Clone URL - `https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2.git` & go to the path `https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/tree/main/MyHealthClinic-AKS`
    
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

![BUILD-PIPELINE](https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/assets/32020205/277bf1cb-7fbd-4497-85d8-8631b9ed7780)

![BUILD-PIPELINE-ARTIFACT](https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/assets/32020205/f1bcbbbc-2390-4a1e-a7cf-fe0c5601d615)

![BUILD-PIPELINE-JOB](https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/assets/32020205/063bf917-86a6-42f0-bb17-1aab5aa7bedd)

![KUBECTL-NODES](https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/assets/32020205/563a34ba-2b73-4d8b-93ab-ae88eda2d67a)

![KUBECTL-PODS](https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/assets/32020205/833461d9-be8b-4e0f-9d70-33d82b05cbbd)

![KUBECTL-SERVICES](https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/assets/32020205/b5c2273b-d866-48e0-b713-57831861669c)


7. Create a release pipeline and run it

![RELEASE-PIPELINE-BLOCK](https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/assets/32020205/0986a0be-b1c3-41ce-a5ba-623b4ec1c519)

![RELEASE-VARIABLES](https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/assets/32020205/39755c9a-4d54-4ae6-9b26-2c830694b035)

![RELEASE-PIPELINE](https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/assets/32020205/603d27f9-30ee-419b-950a-69ef9d345b89)

![APP](https://github.com/Pavan-1997/Azure_DevOps_AKS_PROJECT_2/assets/32020205/c1d392c6-7eb7-45de-b108-134f7464d843)


8. Now delete the Infra using the file `AZURE-AKS-DEVOPS-INFRA-DELETE.sh` and give peemissions `chmod 775 AZURE-AKS-DEVOPS-INFRA-DELETE.sh` and execute it in the Azure CLI

