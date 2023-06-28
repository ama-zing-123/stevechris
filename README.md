# Appservice Deployment  
Deployment my-app-service 
## Create Resource Group  
- az group create --name goldrg --location eastus
## Create AppService Plan  
- az appservice plan create stevechrisappplan --resource-group goldrg
## Create a Web App  
- az webapp create --name stevechriswebapp --resource-group goldrg --plan stevechrisappplan
## Deploy Code to the Webapp  
- az webapp deployment source config --name stevechrisdeployment --resource-group goldrg repo-url https://github.com/ama-zing-123/stevechris.git --branch master --manual-integration
