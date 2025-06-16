---
title: No License Found for Telerik UI for WPF
description: Resolving the missing/invalid license dialog issue with "No License Found" message when using Telerik UI for WPF
type: troubleshooting
page_title: No License Found for Telerik UI for WPF Dialog and Watermark Displayed
slug: kb-licensing-no-license-found-message
tags: telerik ui for wpf, license, class library, missing license
res_type: kb
ticketid: 1690062
---

## Environment

<table>
<tbody>
<tr>
<td>Product</td>
<td>Progress® Telerik® UI for WPF</td>
</tr>
<tr>
<td>Version</td>
<td>2025.1.211</td>
</tr>
</tbody>
</table>

## Description

The "No license found for Telerik UI for WPF" dialog is displayed.

The problem can occur if the licensing is not setup correctly or in some specific cases even if the license is properly installed. 

## Solutions

The following list describes known scenarios where the missing license dialog is shown:

* Incorrect license installation
* Using Telerik UI for WPF in a class library project
* Using Telerik UI for WPF in a add-in/plug-in project

### Incorrect License Installation

UI for WPF provides two licensing approaches based on the product installation method. To make sure the license is properly evaluated, you will need to match the licensing approach with the required installation method.

If you are using NuGet packages to install the Telerik product (recommended), you should use the approach with the `telerik-license.txt` file. 

If you are using assembly references to install the Telerik product, then the approach with the `telerik-license.txt` file won't work. In this case you should manually include the license script key in the project using the EvidenceAttribute (via a TelerikLicense.cs file).

Both approaches are described in the [following article]({%slug installing-license-key%}).

### Using Telerik in a Class Library Project

When using the WPF product in a class library project, you will to install the Telerik.Licensing package also in the main project that consumes the class library. This is described in the [following KB article]({%slug kb-installation-missing-license-in-class-library-setup%}).

### Using Telerik in Add-in/Plug-in Project

When using the WPF product in add-in/plugin projects that are consumed by a third party software like Excel, Revit, AutoCAD, etc., you will to manually register your script key. This is described in the [following KB article]({%slug kb-installation-missing-license-addin-project%}).



