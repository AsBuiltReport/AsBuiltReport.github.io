To start using As Built Report, you will need to perform the following;

1.  Check the version of PowerShell you are running;

    Open a PowerShell console;

    ```powershell
    $PSVersionTable
    ```

2.  Install any 3rd party PowerShell modules / cmdlets. Please check the installation pre-requisites for each AsBuiltReport module.
    e.g. VMware PowerCLI, Cisco UCS PowerTool, Pure Storage PowerShell SDK;

    ```powershell
    Install-Module -Name VMware.PowerCLI
    Install-Module -Name Cisco.UCS.Core
    Install-Module -Name Cisco.UCSManager
    Install-Module -Name PureStoragePowerShellSDK
    ```

3.  For an online installation, install AsBuiltReport modules using the PowerShell Gallery;

    To install individual report modules;

    ```powershell
    Find-Module -Name AsBuiltReport.* -Repository PSGallery
    Install-Module -Name AsBuiltReport.Vendor.Product
    e.g. Install-Module -Name AsBuiltReport.VMware.vSphere
    ```

4.  For an offline installation, perform the following steps from a machine with internet connectivity;
    Save the required modules to a specified folder

    ```powershell
    Save-Module -Name AsBuiltReport.VMware.vSphere -Path 'C:\Path\To\Specified\Folder'
    ```

    Copy the downloaded module folders to a location that can be made accessible to the offline system.
    e.g. USB Flash Drive, Internal File Share etc.
    On the offline system, open a PowerShell command window and run the following command to determine the PowerShell Module Path

    ```powershell
    $env:PSModulePath -Split ';'
    ```

    Copy the downloaded module folders to a folder specified in the PSModulePath output.
