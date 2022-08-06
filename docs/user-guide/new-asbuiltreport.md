
### Description

New-AsBuiltReport creates ‘as built’ configuration reports for one or more target systems and exports the report in to one or more supported document formats, such as DOCX, HTML and Text.

New-AsBuiltReport provides additional parameters, allowing users to generate and customise a report to their requirements.

### Parameters

#### Report

Specifies the type of report that will be generated.
This is a mandatory parameter.

#### Target

Specifies the IP/FQDN of the system to connect.
This is a mandatory parameter.

#### Credential

Specifies the stored credential of the target system.
This is a mandatory parameter.

#### Username

Specifies the username of the target system.
This is a mandatory parameter.

#### Password

Specifies the password of the target system.
This is a mandatory parameter.

#### Format

Specifies the output format of the report.
The supported output formats are Word, HTML & Text.
Multiple output formats may be specified, separated by a comma.
This is an optional parameter.
If the parameter is not specified, the document format will default to Word.

#### Orientation

Sets the page orientation of the report to Portrait or Landscape.
This is an optional parameter.
If the parameter is not specified, page orientation will be set to Portrait.

#### StyleFilePath

Specifies the file path to a custom style .ps1 script for the report to use.
This is an optional parameter and does not have a default value.

#### OutputFolderPath

Specifies the folder path to save the report.
This is a mandatory parameter.

#### AsBuiltConfigFilePath

Specifies the file path to the As Built Report configuration JSON file.
This is an optional parameter.
If this parameter is not specified, the user will be prompted for this configuration information on first run, with the option to save the configuration to a file.

#### ReportConfigFilePath

Specifies the file path to a report JSON configuration file.
This is an optional parameter.
If this parameter is not specified, a default report configuration JSON is copied to the specified user folder.
If this parameter is specified and the path to a JSON file is invalid, the script will terminate.

#### Timestamp

Specifies whether to append a timestamp string to the report filename.
This is an optional parameter.
By default, the timestamp string is not added to the report filename.

#### EnableHealthcheck

Highlights certain issues within the system report.
Some reports may not provide this functionality.
This is an optional parameter.
If the parameter is not specified, health checks are not enabled.
SendEmail

Sends report to specified recipients as email attachments.
This is an optional parameter.

### Examples

Creates an as-built report for a VMware vSphere environment. Report is generated in Word and Text formats and saved to the C:\Reports folder. Health checks will be enabled.

```powershell
New-AsBuiltReport -Report VMware.vSphere -Target vcenter.domain.local -Username administrator@vsphere.local -Password VMware1! -Format Word,Text -OutputFolderPath 'C:\Reports' -EnableHealthCheck
```

Creates an as-built report for two Pure Storage FlashArrays. Report is generated in HTML format, saved to the C:\Reports folder and sent via email.

```powershell
New-AsBuiltReport -Report PureStorage.FlashArray -Target 192.168.10.100,192.168.10.110 -Credential (Get-Credential) -Format HTML -OutputFolderPath C:\Reports -SendEmail
```

Creates an as-built report for a Cisco UCS environment. Authentication to UCS Manager uses stored credentials. The report is generated in Word format (by default) with landscape page orientation. A customised stylesheet is specified to style the report in the company’s brand colours and fonts. The report is saved to the user’s documents folder with a timestamp added to the filename to identify when the report was generated. The AsBuiltConfig parameter is specified to bypass the menu driven questionnaire.

```powershell
New-AsBuiltReport -Report Cisco.UcsManager -Target melucs01 -Credential $creds -OutputFolderPath "$env:USERPROFILE\Documents" -StyleFilePath 'C:\AsBuiltReport\MyCompanyStyle.ps1' -AsBuiltConfigFilePath 'C:\AsBuiltReport\MyCompanyConfig.json' -Timestamp
```
