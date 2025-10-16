---
title: Theming Support for WPF Native Controls
page_title: Setting a Theme on MS Controls
description: Telerik themes define styles also for few {{ site.framework_name }} native controls like TextBox, Button, ScrollViewer and more.
slug: styling-apperance-themes-mscontrols
tags: setting,a,theme,on,ms,controls
published: True
position: 9
---

# Theming Support for WPF Native Controls

The [Telerik themes]({%slug common-styling-appearance-available-themes%}) provide styling for the Telerik controls and also several native WPF controls. 

This article lists all the native WPF controls supporting Telerik theming, and shows how to enable the theming using the [Style Manager]({%slug styling-apperance-implicit-styles-overview%}#setting-a-theme-using-stylemanager) and [Implicit Styles]({%slug styling-apperance-implicit-styles-overview%}#setting-a-theme-using-implicit-styles) mechanisms. 

When using the __Implicit Styles__ theming mechanism, the native controls are themed automatically when the Telerik's __System.Windows.xaml__ file gets merged in the application resources.

When using the __StyleManager__ theming, only the native controls used in the templates of the Telerik controls are automatically themed. All external WPF controls use their default theming.

## Native controls supported by the Telerik theming mechanism

Below is the full control list of native WPF controls supported by the Telerik theming mechanism:		

* `System.Windows.Controls.Button`

* `System.Windows.Controls.ScrollViewer`

* `System.Windows.Controls.CheckBox`

* `System.Windows.Controls.TextBox`

* `System.Windows.Controls.RadioButton`

* `System.Windows.Controls.ListBox`

* `System.Windows.Controls.PasswordBox`

* `System.Windows.Controls.Primitives.RepeatButton`

* `System.Windows.Controls.Tooltip`

* `System.Windows.Documents.Hyperlink`

* `System.Windows.Controls.Primitives.StatusBar`

* `System.Windows.Controls.GridSplitter`

* `System.Windows.Controls.Separator`

Additionally, there are two more controls part of the Telerik UI for WPF suite which mimic the WPF native [Label](https://docs.microsoft.com/en-us/dotnet/api/system.windows.controls.label?view=netframework-4.5) and [GroupBox](https://docs.microsoft.com/en-us/dotnet/api/system.windows.controls.groupbox?view=netframework-4.5). There are no styles for the native versions of those controls. The reason behind this decision is a legacy related to the Silverlight framework (now outdated), which shared a common codebase with WPF. In the Silverlight framework there wasn't native Label and GroupBox controls so they were created in the Telerik suite in order to provide them to the Silverlight users and also to enable the theming support.

* `Telerik.Windows.Controls.Label`

* `Telerik.Windows.Controls.GroupBox`

>Before proceeding with this tutorial, you can check the [Setting a Theme]({%slug styling-apperance-implicit-styles-overview%}) topic.

## Setting the Theme Using Implicit Styles 

To set the theme to all controls in the application, merge the corresponding ResourceDictionary (__System.Windows.xaml__). This will ensure that the native controls used in the Telerik ones will have the correct theme applied. In this case, any instance of the native controls which is separately defined will also get the Telerik theme.		

__Merging the System.Windows.xaml file__ 
```XAML
	<Application.Resources>
		<ResourceDictionary>
			<ResourceDictionary.MergedDictionaries>
				<ResourceDictionary Source="/Telerik.Windows.Themes.Office2013;component/Themes/System.Windows.xaml"/>
				<!-- the other Telerik resource here -->
			</ResourceDictionary.MergedDictionaries>
		</ResourceDictionary>
	</Application.Resources>
```

To set the theme seprately per control, you can merge the System.Windows.xaml resource in the `Resources` dictionary of the corresponding control.

__Setting a theme per control using implicit styles__ 
```XAML
	<CheckBox Content="CheckBox">	
		<CheckBox.Resources>
			<ResourceDictionary Source="/Telerik.Windows.Themes.Office2013;component/Themes/System.Windows.xaml"/>
		</CheckBox.Resources>
	</CheckBox>
```

To avoid applying the theme to a specific native control after the global theming setting (in the App.xaml `Resources`), you can set its Style property to an `Style` object without any `Setters`.

__Disabling the default theming__ 
```XAML
	<CheckBox Content="CheckBox">	
		<CheckBox.Style>
			<Style TargetType="CheckBox"/>
		</CheckBox.Style>
	</CheckBox>
```

## Setting the Theme Using StyleManager

To set the theme per control, use the `StyleManager.Theme` attached property.

__Setting a theme per control using StyleManager__ 
```XAML
 	<CheckBox Content="CheckBox" telerik:StyleManager.Theme="Windows11" />
```

There is no global setting in the __StyleManager__ that will apply the theme to all WPF native controls in the view. But this can be done by defining an implicit Style definitions for the needed types and setting the `StyleManager.Theme` property there. 

__Setting the Telerik theme globally for all CheckBox controls in the view__ 
```XAML
	<Application.Resources>
	 	<Style TargetType="CheckBox">
			<Setter Property="telerik:StyleManager.Theme" Value="Windows11" />
		</Style>
   	</Application.Resources>
```

## See Also  
 * [Use StyleManager to Apply Theme on MS Controls]({%slug common-styling-themes-mscontrols%})
 * [Setting a Theme (Using  Implicit Styles)]({%slug styling-apperance-implicit-styles-overview%})
 * [Switching Themes at Runtime]({%slug styling-apperance-themes-runtime%})
