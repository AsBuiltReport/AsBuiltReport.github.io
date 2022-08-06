
### Description

Creates JSON configuration files for individual As Built Reports.
Parameters

### Parameters

#### Report

Specifies the type of report configuration to create.
This is a mandatory parameter.

#### Folderpath

Specifies the folder path to create the report JSON configuration file.
This is a mandatory parameter.

#### Filename

Specifies the filename of the report JSON configuration file. If a filename is not specified, a JSON configuration file will be created with a default filename AsBuiltReport.Vendor.Product.json
This is an optional parameter.

#### Force

Specifies to overwrite an existing JSON configuration.
This is an optional parameter.

### Examples

Creates a new report JSON for VMware vSphere in the C:\Reports folder.

```powershell linenums="1"
New-AsBuiltReportConfig -Report VMware.vSphere -Folderpath 'C:\Reports'
```

Creates a new report JSON named ‘MyCompany.Cisco.UCS’ in C:\AsBuiltReport folder.

```powershell
New-AsBuiltReportConfig -Report Cisco.UcsManager -Filename 'MyCompany.Cisco.UCS' -Folderpath 'C:\AsBuiltReport'
```

Creates a new report JSON file for VMware NSX-v in C:\Reports folder, overwriting the existing file.

```powershell
New-AsBuiltReportConfig -Report VMware.NSXv -Folderpath 'C:\Reports' -Force
```