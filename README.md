# Azureinventory-Powershell
Azureinventory Collection


To get the Azure inventory details from powershell you need to install the excel modules in your powershell. 

1.Run the following command to install Excel Modules:

Import-Module -Name PowerShellGet -Force
Install-Module -Name ImportExcel -Scope CurrentUser -Force



 It will download all the required Modules for the Azure inventory and Resources



2.Install Azure CLI
Run the following commands : 

Invoke-WebRequest -Uri https://aka.ms/installazurecliwindows -OutFile AzureCLI.msi
Start-Process msiexec.exe -Wait -ArgumentList '/I AzureCLI.msi /quiet'

3.Install Azure CLI Account Extension
    
      az extension add --name account


If it's already Present it displays the version, if not it  will install the extension.

4. Install Azure CLI Resource-Graph Extension

     az extension add --name resource-graph





5. Copy and paste below “ps1” file in local drive where Azure CLI is installed.

https://drive.google.com/file/d/1rPWPb35Bx0VOti77Nn3Kbaq83FGvD_gD/view?usp=drive_link

Run "AzureResourceInventory.ps1". In Azure CloudShell you're already authenticated. In PowerShell Desktop you will be redirected to Azure sign-in page

Run the following command

.\AzureResourceInventory.ps1 -TenantId ********************* -IncludeTags -Diagram -SecurityCenter -Quotesage

Note:Plz change the tenant id as specific to your account


 
It will start exporting as below 
 
After the successful completion the exported sheets are placed in the directory as mentioned below : 
Excel file saved at: C:\AzureResourceInventory\AzureResourceInventory_Report_2023-08-216.xlsx

Draw.io Diagram file saved at: C:\AzureResourceInventory\AzureResourceInventory_Diagram_2023-08-21.xml

 



Now open the file where all the Azure inventory has been imported in excel format and Diagram format as below .
 



