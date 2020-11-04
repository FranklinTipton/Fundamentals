# Azure in PowerShell Overview

## Why use Azure in PowerShell

Having already established that PowerShell in itself is a great tool for automation and administration, that extends to the management of Azure as well. A huge benefit of using Azure in PowerShell is the ability to localize the deployment of Azure Resource Management (ARM) Templates. 

It is important to note that installing the AZ module on an account will only apply to the current user and the version of PowerShell. For example, if you try to run Azure commands in your VSCode terminal, with only have the modules installed on PowerShell, you wont succeed.

## Connecting to Azure

In our PowerShell Overview we discussed how to get Azure installed in our environment, or you can click [here](/PowerShell/Overview.md#installing-the-Az-PowerShell-module). Since Azure runs off of a subscription you want to ensure you're connected to your account. To get connected copy and paste the following:

```powershell
Connect-AzAccount
```

### Changing Subscriptions in Azure

If you are working in an evironment with several Azure subscriptions it could be confusing. Making sure you're working with the correct could be extremely important, especially when it comes time to pay the bill. You can make sure you're in the correct subscription by using this command: 

```powershell
az account set --subscription "subname"
```

While using this command change the name in quotations to your desired subscription name.