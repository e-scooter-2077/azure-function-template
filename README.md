# azure-function-template
## Quickstart
1. After using the template, rename the solution with the name of your Function.
2. Setup on [Azure Portal](https://portal.azure.com/#home) the required resources:
    1. A resource group
    2. A storage account
    3. A function app with .NET runtime and other configuration (function version required is 3)
3. Change the runtime version from `dotnet` to `dotnet-isolated` with this command, run it in the Azure CLI or **Azure Cloud Shell**:
   ```
   az functionapp config appsettings set --name <your-azure-app-name> --resource-group <your-resource-group> --settings FUNCTIONS_WORKER_RUNTIME=dotnet-isolated
   ```
4. Setup the `AZURE_CREDENTIALS` secret, either as a repository secret or as an organization secret. 
5. Setup the CI `env` parameters `RELEASE_PREFIX` (any string will do) and `AZURE_FUNCTIONAPP_NAME` (the name of the function app on Azure)

# Launch CI
To trigger the CI for a release, run the following commands inside the repository's directory:

```
git tag -a v#.#.# -m "v#.#.#"
git push origin v#.#.#>
```

Alternatively, you can use the [git-release](https://github.com/francescodente/git-release) tool.