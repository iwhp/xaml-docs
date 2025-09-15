---
title: Getting Started
page_title: Getting Started
description: Check our &quot;Getting Started&quot; documentation article for the RadSpreadsheet {{ site.framework_name }} control.
slug: radspreadsheet-getting-started
tags: getting,started
published: True
position: 2
---

# Getting Started with {{ site.framework_name }} Spreadsheet

This article explains how to add a __RadSpreadsheet__ control to a page in your application.

It contains the following sections:

* [Adding Telerik Assemblies Using NuGet](#adding-telerik-assemblies-using-nuget)
* [Adding Assembly References Manually](#adding-assembly-references-manually)

* [Namespaces](#namespaces)

* [Spreadsheet and RibbonView](#spreadsheet-and-ribbonview)

* [Open/Save Documents](#opensave-documents)

## Adding Telerik Assemblies Using NuGet

To use __RadSpreadsheet__ when working with NuGet packages, install the `Telerik.Windows.Controls.Spreadsheet.for.Wpf.Xaml` package. The [package name may vary]({%slug nuget-available-packages%}) slightly based on the Telerik dlls set - [Xaml or NoXaml]({%slug xaml-vs-noxaml%})

Read more about NuGet installation in the [Installing UI for WPF from NuGet Package]({%slug nuget-installation%}) article.

>tip With the 2025 Q1 release, the Telerik UI for WPF has a new licensing mechanism. You can learn more about it [here]({%slug installing-license-key%}).

## Adding Assembly References Manually

If you are not using NuGet packages, you can add a reference to the following assemblies:
        
* __Telerik.Licensing.Runtime__
* __Telerik.Windows.Controls.dll__
* __Telerik.Windows.Controls.GridView.dll__
* __Telerik.Windows.Controls.Input.dll__
* __Telerik.Windows.Controls.Navigation.dll__
* __Telerik.Windows.Controls.Spreadsheet.dll__
* __Telerik.Windows.Data.dll__
* __Telerik.Windows.Documents.Core.dll__
* __Telerik.Windows.Documents.Spreadsheet.dll__

For export and import to __XLSX__:

* __Telerik.Windows.Zip.dll__
* __Telerik.Windows.Documents.Spreadsheet.FormatProviders.OpenXml.dll__

To export a document to __PDF__, you will need to add a reference to the corresponding assembly:

* __Telerik.Windows.Documents.Spreadsheet.FormatProviders.Pdf.dll__

Note that in order to import/export in XLSX or export to PDF, the format provider must be registered manually. More information on Import/Export can be found [here]({%slug radspreadsheet-import-export%}).

If you want to use the sample UI provided in our demos you should add this reference as well:        

* __Telerik.Windows.Controls.RibbonView.dll__
{% if site.site_name == 'WPF' %}* __Telerik.Windows.Controls.SpreadsheetUI.dll__{% endif%}

## Namespaces

For a bare-bone Spreadsheet control, you only need a declaration of the telerik schema:

#### __XAML__

```XAML

	xmlns:telerik="http://schemas.telerik.com/2008/xaml/presentation" 
```



For the UI that enables the full-featured use of the control, you should also declare:

#### __XAML__

```XAML

	xmlns:spreadsheetControls="clr-namespace:Telerik.Windows.Controls.Spreadsheet.Controls;assembly=Telerik.Windows.Controls.Spreadsheet"
	xmlns:spreadsheet="clr-namespace:Telerik.Windows.Controls.Spreadsheet;assembly=Telerik.Windows.Controls.Spreadsheet"
	```


Then, all that is left is to add the __Spreadsheet__ component to the page:
      

#### __XAML__

```XAML

	<telerik:RadSpreadsheet x:Name="radSpreadsheet" />
```



## Spreadsheet and RibbonView


__RadSpreadsheet__ is easy to integrate with all kinds of UI thanks to the commanding mechanism that it employs. If you would like to use the control with a [RadRibbonView]({%slug radribbonview-overview%}), which shows the full potential of the control, you can refer to the {% if site.site_name == 'Silverlight' %}[SDK repository](https://github.com/telerik/xaml-sdk/tree/master/Spreadsheet/SL/FirstLook).{% endif %}{% if site.site_name == 'WPF' %} [Spreadsheet UI]({%slug radspreadsheet-getting-started-spreadsheet-ui%}) topic that describes how you can take advantage of __RadSpreadsheetRibbon__.{% endif %}        

## Open/Save Documents

To open a document, you need to import it and the export functionalities will help you to save one. To work with documents of the formats supported by __RadSpreadsheet__, you should use the format provider classes. For more information on the matter, please check the [Import/Export]({%slug radspreadsheet-import-export%}) topic.

{% if site.site_name == 'WPF' %}
## Telerik UI for WPF Learning Resources

* [Telerik UI for WPF Spreadsheet Component](https://www.telerik.com/products/wpf/spreadsheet.aspx)
* [Getting Started with Telerik UI for WPF Components]({%slug getting-started-first-steps%})
* [Telerik UI for WPF Installation]({%slug installation-installing-which-file-do-i-need%})
* [Telerik UI for WPF and WinForms Integration]({%slug winforms-integration%})
* [Telerik UI for WPF Visual Studio Templates]({%slug visual-studio-templates%})
* [Setting a Theme with Telerik UI for WPF]({%slug styling-apperance-implicit-styles-overview%})
* [Telerik UI for WPF Virtual Classroom (Training Courses for Registered Users)](https://learn.telerik.com/learn/course/external/view/elearning/16/telerik-ui-for-wpf) 
* [Telerik UI for WPF License Agreement](https://www.telerik.com/purchase/license-agreement/wpf-dlw-s)
{% endif %}

## See Also

* [Import/Export]({%slug radspreadsheet-import-export%})
* [Spreadsheet UI]({%slug radspreadsheet-getting-started-spreadsheet-ui%})
* [SpreadProcessing](https://docs.telerik.com/devtools/document-processing/libraries/radspreadprocessing/overview)