# Check Function App Deployment Status

Determine if Azure Function Apps from this repository have been deployed to the user's Azure tenant.

## Task

1. **Check Azure Login**
   - Verify user is logged into Azure CLI
   - Display current tenant and subscription

2. **Identify Function Apps**
   - Search the repository for Function App projects
   - List the function app names that would be deployed

3. **Check Deployment Status**
   - Query Azure to see if function apps exist
   - For each function app found in the repo, check if it's deployed
   - Report on deployment status, resource group, and location

4. **Generate Report**
   - List all function apps expected from this repository
   - Show which ones are deployed (with details)
   - Show which ones are not deployed
   - Include resource group and region information for deployed apps

## Commands to Use

```bash
# Check login
az account show

# List function apps in subscription
az functionapp list --output table

# Check specific function app
az functionapp show --name <app-name> --resource-group <rg-name>
```

Please execute this analysis and provide a clear report of the deployment status.
