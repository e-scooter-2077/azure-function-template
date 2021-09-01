# azure-function-template
## Quickstart
1. After using the template, replace the solution and the project files with yours.
2. Configure on [Azure Portal](https://portal.azure.com/#home) the required resources:
    1. A resource group
    2. A storage account
    3. A function app with .NET runtime and other configuration (function version required is 3)
3. Change the runtime version from `dotnet` to `dotnet-isolated` with this command, run it in the Azure CLI or **Azure Cloud Shell**:  
   `az functionapp config appsettings set --name <your-azure-app-name> --resource-group <your-resource-group> --settings FUNCTIONS_WORKER_RUNTIME=dotnet-isolated`
