<p align="center">
    <a href="https://www.asbuiltreport.com/" alt="AsBuiltReport"></a>
            <img src='https://raw.githubusercontent.com/AsBuiltReport/AsBuiltReport/master/AsBuiltReport.png' width="15%" height="15%" /></a>
</p>
<h1 style="font-size:3vw" align="center"><b>As Built Report</b></h1>

As Built Report is an open source configuration document framework which utilises Microsoft PowerShell to produce as-built documentation in multiple document formats for multiple vendors and technologies. The framework allows users to easily generate clear and consistent documentation, for any environment which supports Microsoft PowerShell and/or a RESTful API.


## **Features**

||||
|-----------------------|-----------------------|-----------------------|
| :memo: **Multiple Document Formats** | :microscope: **Granular Detail Level** | :art: **Customised Styling** |
| Generate and output reports in one or more document formats, including DOCX, HTML, and Text. | Configure the detail level for each section of a report. You have the choice of producing a summarised report, a fully comprehensive report or something in between. | Use a default style or create your own to match your corporate identity. Set page orientation, text and table formatting with fonts, colours, borders and highlighted cells and rows. |
| :package: **Modular Design** | :hearts: **Health Checks** | :email: **Email Reports** |
| Install and update the entire report library or each report individually, via the PowerShell Gallery. | Enable health checks to highlight configuration issues within a report. Toggle individual health checks on or off as required. | Attach and send reports via email to one or more recipients. |

As Built Report provides the following features;

* Modular design enables contributors a simple way to develop new reports.
* Install and update the entire report library or each report individually, via the PowerShell Gallery.
* Generate and output reports in one or more document formats, including DOCX, HTML, and Text.
* Configure the detail level for each section of a report. You have the choice of producing a summarised report, a fully comprehensive report or something in between.
* Support for custom styling. Set page orientation, text and table formatting with fonts, colours, borders and highlighted cells and rows.
* Enable health checks to highlight configuration issues within a report. Toggle individual health checks on or off as required.
* Append the time and date to reports to maintain records.
* Attach and send reports via email to one or more recipients.

## **Components**

|||
|-----------------------|-----------------------|
| **As Built Report Configuration** | **Reports Configuration** |
| A JSON configuration file used to store information relating to author’s name, company information & SMTP mail server configuration. Individual configuration files can be saved and specified also. | The report configuration is a JSON file which stores information specific to the related report. It holds information such as the report name, version, and release status. The report configuration can also provide functionality such as configurable report options, health checks and granular information levels. |
| **Reports Module** | **Styles Script (.ps1)** |
| The report module is specific to each vendor and/or technology and is used to extract information from the specific environment. The report module will be written to utilise PowerShell modules or RESTful APIs which the vendor/technology provides. | The styles script sets the default layout, fonts, colours and sizes used within the report. Style scripts can be used to layout cover pages, table of contents and other unique tables or sections. |


## **Report Modules**

<table width="100%">
    <tr>
        <td align="center" valign="middle" width="50%"><a href="https://github.com/orgs/AsBuiltReport/repositories?q=VMware&type=all&language=&sort="><img src="https://raw.githubusercontent.com/AsBuiltReport/.github/main/profile/images/VMware.png" width="75%" height="75%" /></a></td>
        <td align="center" valign="middle" width="50%"><a href="https://github.com/orgs/AsBuiltReport/repositories?q=Microsoft&type=all&language=&sort="><img src="https://raw.githubusercontent.com/AsBuiltReport/.github/main/profile/images/Microsoft.png" width="75%" height="75%" /></a></td>
    </tr>
    <tr>
        <td align="center" valign="middle" width="50%"><a href="https://github.com/orgs/AsBuiltReport/repositories?q=DellEMC&type=all&language=&sort="><img src="https://raw.githubusercontent.com/AsBuiltReport/.github/main/profile/images/Dell_EMC.png" width="75%" height="75%" /></a></td>
        <td align="center" valign="middle" width="50%"><a href="https://github.com/orgs/AsBuiltReport/repositories?q=NetApp&type=all&language=&sort="><img src="https://raw.githubusercontent.com/AsBuiltReport/.github/main/profile/images/NetApp.png" /></a></td>
    </tr>
    <tr>
        <td align="center" valign="middle" width="50%"><a href="https://github.com/orgs/AsBuiltReport/repositories?q=Nutanix&type=all&language=&sort="><img src="https://raw.githubusercontent.com/AsBuiltReport/.github/main/profile/images/Nutanix.png" /></a></td>
        <td align="center" valign="middle" width="50%"><a href="https://github.com/orgs/AsBuiltReport/repositories?q=PureStorage&type=all&language=&sort="><img src="https://raw.githubusercontent.com/AsBuiltReport/.github/main/profile/images/PureStorage.jpg" /></a></td>
    </tr>
    <tr>
        <td align="center" valign="middle" width="50%"><a href="https://github.com/orgs/AsBuiltReport/repositories?q=Veeam&type=all&language=&sort="><img src="https://raw.githubusercontent.com/AsBuiltReport/.github/main/profile/images/Veeam.png" width="50%" height="50%" /></a></td>
        <td align="center" valign="middle" width="50%"><a href="https://github.com/orgs/AsBuiltReport/repositories?q=Rubrik&type=all&language=&sort="><img src="https://raw.githubusercontent.com/AsBuiltReport/.github/main/profile/images/Rubrik.png" /></a></td>
    </tr>
</table>