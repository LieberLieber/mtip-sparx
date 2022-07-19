# mtip-sparx-plugin

> The MTIP Sparx Plugin allows exporting and importing of SysML v1.5 models to the HUDS XML format to and from Cameo Systems Modeler via the mtip-cameo-plugin.

## Modeling Tool Integration Plugin for Sparx Enterprise Architect (MTIP-Sparx EA)

## Description

MTIP-Sparx EA plugin is developed by The Aerospace Corporation to create an exchange standard that enables a nearly  1-to-1 translation of Model Based Systems Engineering (MBSE) models to and from Cameo Systems Modeler using principles derived in the Systems Modeling Language (SysML). The developed plugin enables a way for SysML v1.5 models to be exchanged freely between the tools and includes elements, relationships, and diagrams. Object types are mapped to a common SysML metamodel and exported/imported using the Huddle Unified Data Schema (HUDS) V2 Extensible Markup Language (XML) format.

Metamodel mapping implemented adheres to the to the SysML v1.5 specification which includes 9 diagram types along with the general-purpose constructs that may be shown on the multiple diagram types.

## Getting Started

### Prerequisites

* [Sparx - Enterprise Architect](https://sparxsystems.us/go/enterprise-architect-cloud/?keyword=%2Bsparx%20%2Benterprise%20%2Barchitect&creative=498008725817&gclid=CjwKCAiAp8iMBhAqEiwAJb94z-PmUa41-smzhAaqj634_Tt1h6UZBraN4dHq_1yjsy-FZh98_RWlPhoCreEQAvD_BwE)
  * The latest MTIP plugin is compatible with Version 14.x and 15.x
* Visual Studio (2017/2019)
  * .NET desktop development installed
  * Microsoft Visual Studio Installer Project Extension
  * EA Add-in Framework API written in C#
    * The EA API assembly must be added to the project references. The current project points to the Interop.EA.dll in the EA default installation folder (C:\Program Files\Sparx Systems\EA). If you installed EA at a different, location you will have to reconfigure the reference.
    * No action needs to be taken if the reference is located upon cloning the project

### System Requirements

* Windows 10

### Installation

* Download the MTIPInstaller.msi or setup.exe from repository (located under "Releases" on the right panel) and run following installer instructions
* Follow the installer to complete installation
* Once completed you can now access the MTIP-Sparx EA plugin within the "Specialized" tab in EA

### Building Instructions

To build the plugin along with the plugin installer for development environment

* Add registry key
  * See step 2 in [Create your first EA Add-in](https://sparxsystems.us/go/enterprise-architect-cloud/?keyword=%2Bsparx%20%2Benterprise%20%2Barchitect&creative=498008725817&gclid=CjwKCAiAp8iMBhAqEiwAJb94z-PmUa41-smzhAaqj634_Tt1h6UZBraN4dHq_1yjsy-FZh98_RWlPhoCreEQAvD_BwE](https://bellekens.com/2011/01/29/tutorial-create-your-first-c-enterprise-architect-add-in-in-10-minutes/))
* Open the project in Visual Studio
* Right click on the project and select the “Build” option
  * Note: MTIP Installer version in MTIPInstaller project properties must be updated for each installer build. Installer .msi and .exe will be built in &lt;MTIP Solution Directory&gt;\MTIPInstaller\Debug

### Running the Plugin in Enterprise Architect

The following section includes instructions on plugin usage once built or installed:

* Import HUDS V2 XML
  * Open existing project file or create a new project you would like to import your model/package into.
  * Select to “Specialize” tab in EA toolbar
  * Open MTIP Add-In menu from Add-Ins panel
  * Select “Launch” from Add-In dropdown menu
  * Select “Import from HUDS XML”
  * Select HUDS V2 XML(s) to import (multiple HUDS V2 XML files can be imported)
  * Select “Import”
  * Message will appear once import is complete
  * Import logs can be found in the users "Documents" directory

* Export HUDS V2 XML
  * Open existing project to export
  * In project browser select Root Node or Package you would like to export (Can only select one at a time)
  * Two options for export
    * Navigate to “Specialize” tab in EA toolbar and open MTIP AddIn menu from Add-Ins panel
    * Right click on Root Node/Package to export, hover over "Specialized" then "MTIP"
  * Select “Launch” from AddIn dropdown menu
  * Select “Export to HUDS XML”
  * Select desired export directory
  * Message will appear once export is complete
  * Exported HUDS XML and export logs can be found in selected export directory

## Authors

Karina Martinez, The Aerospace Corporation
oss@aero.org

## License

This project is licensed under the Apache Commons License 2.0 - see the LICENSE.html file for details
