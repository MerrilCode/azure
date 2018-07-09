### Remove default powershell tenant and subscriptions (Optional) ###
`Set-AzureRmContext -Context ([Microsoft.Azure.Commands.Profile.Models.PSAzureContext]::new())`

### Log into azure account ###

`Connect-AzureRmAccount` | `Login-AzureRmAccount`

### Select the subscription to run the commands without affecting the default subscription for powershell ###

`Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"`

### Get all the roles for RBAC (Optional) ###

`Get-AzureRmProviderOperation *`

### Get all the roles specific to a resource (Optional) ###

`Get-AzureRmProviderOperation */virtualMachines/*`

Read [more](https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation?view=azurermps-6.4.0)

### Create the JSON file with the custom roles ###

Read more [here](https://docs.microsoft.com/en-us/azure/role-based-access-control/custom-roles)

### Run the powershell command to create the custom role on Azure ###

`New-AzureRmRoleDefinition -InputFile C:\path\to\file`

Read more [here](https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermroledefinition?view=azurermps-6.4.0)






