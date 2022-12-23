# azautomodule
Imports a PowerShell-based GitHub Repo module into Azure Automation

## DESCRIPTION
This action wraps the command **New-AzAutomationModule**, which, according to Microsoft:

..imports a module into Azure Automation.

This command accepts a compressed file that has a .zip file name extension.

The file contains a folder that includes a file that is one of the following types:
- Windows PowerShell module, which has a .psm1 or .dll file name extension
- Windows PowerShell module manifest, which has a .psd1 file name extension

The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.

Specify the .zip file as a URL that the Automation service can access.

If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.
The command finishes whether the import succeeds or fails.
To check whether it succeeded, run the following command:
`PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName
Check the **ProvisioningState** property for a value of Succeeded.