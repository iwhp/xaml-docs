---
title: Performance Tips
page_title: Performance Tips
description: Check our &quot;Performance Tips&quot; documentation article for the RadSpreadsheet WPF control.
slug: spreadsheet-performance-tips
tags: ui,performance,tips,tricks
published: True
position: 9
---

# Performance Tips

The RadSpreadsheet control is optimized to bring a great performance, but this can be improved even further by keeping in mind the following tips and tricks.

* The  RadSpreadsheet control uses the document model of [RadSpreadProcesing](https://docs.telerik.com/devtools/document-processing/libraries/radspreadprocessing/overview). Check the [Performance Tips and Tricks](https://docs.telerik.com/devtools/document-processing/libraries/radspreadprocessing/performance) article of the library to see how to optimize the document model.

* Use the [NoXaml]({%slug xaml-vs-noxaml%}) Telerik dlls. This will improve the initial loading performance. 

* The usability of the control can be improved also by preloading the view that will display the RadSpreadsheet. This won't boost the general performance, but will move the WPF resources loading behavior before the view is displayed, thus improving the later interactions with the application. To preload the control, you should add it (but hidden) to the visual tree of the application at some point around startup. The exact place will depend on the specific application setup.

* If using [RadSpreadsheetRibbon]({%slug radspreadsheet-getting-started-spreadsheet-ui%}), remove the tabs or other elements that are not necessary in the application. To do this, you can use the [ChildrenOfType]({%slug common-visual-tree-helpers%}) extension method, or you can [modify the ControlTemplate]({%slug styling-apperance-editing-control-templates%}) of RadSpreadsheetRibbon.

	#### __[C#] Using the ChildrenOfType method to remove the first tab from the ribbon control__
	{{region spreadsheet-performance-tips-0}}
		this.spreadsheetRibbon.ChildrenOfType<RadRibbonView>().FirstOrDefault().Items.RemoveAt(0);  
	{{endregion}}

* If using [RadSpreadsheetRibbon]({%slug radspreadsheet-getting-started-spreadsheet-ui%}), set its `IsMinimized` property to `true`.
	
	#### __[XAML] Minimizing the ribbon control__
	{{region spreadsheet-performance-tips-1}}
		<telerik:RadSpreadsheetRibbon IsMinimized="True" />
	{{endregion}}

## See Also  

* [UI Virtualization]({%slug radspreadsheet-ui-virtualization%})
