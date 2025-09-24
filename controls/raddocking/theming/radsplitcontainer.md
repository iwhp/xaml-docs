---
title: Theming the RadSplitContainer
page_title: Theming the RadSplitContainer
description: Check our &quot;Theming the RadSplitContainer&quot; documentation article for the RadDocking {{ site.framework_name }} control.
slug: raddocking-theming-radsplitcontainer
tags: theming,the,radsplitcontainer
published: True
position: 4
---

# Theming the RadSplitContainer

To modify the appearance of the __RadSplitContainer__ you have to create a custom theme and place a style that targets the __RadSplitContainer__ control in it. The topic assumes that you have already created {% if site.site_name == 'WPF' %}a theme with {% endif %}a __ResourceDictionary__ that will host the styles and the resources for your custom theme. If not take a look at the overview section about [creating the theme](#CreatingTheme). The topic also assumes that you have already created the style that will be used for the __RadSplitContainer__ control. To learn how to style it take a look at the [Styling the RadSplitContainer]({%slug raddocking-styling-the-radsplitcontainer%}) topic.

Copy the created style with all of the resources it uses and place it in the __ResourceDictionary__ that represents the theme for your __RadDocking__ control.



```XAML
	<ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
	    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
	    <!--Paste the style and all of the resources it uses here. -->
	    <Style x:Key="RadSplitContainerStyle" TargetType="telerik:RadSplitContainer">
	        <!--...-->
	    </Style>
	</ResourceDictionary>
```

The next step is to declare the required namespaces in the resource dictionary.



```XAML
	<ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
	    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
	    xmlns:telerik="http://schemas.telerik.com/2008/xaml/presentation">
	    <!--...-->
	</ResourceDictionary>
```

{% if site.site_name == 'Silverlight' %}

Finally, in order to make the style default for all of the __RadSplitContainer__ controls you have to leave it without a key. Remove the key from the style.{% endif %}



```XAML
	<Style TargetType="telerik:RadSplitContainer">
	    <!--...-->
	</Style>
```

{% if site.site_name == 'Silverlight' %}

To apply the theme got to the UserControl that hosts your __RadDocking__ control and set it through the code-behind.{% endif %}



```C#
	public App()
	{
	    InitializeComponent();
	    StyleManager.SetTheme( this.radDocking, new RadDockingTheme());
	}
```



```VB.NET
	Public Sub New()
		InitializeComponent()
		StyleManager.SetTheme(Me.radDocking, New Theme())
	End Sub
	
	Private Property radDocking As DependencyObject
```

{% if site.site_name == 'WPF' %}

Finally in order to make the style default for all of the __RadSplitContainer__controls you have to set it to the following value.{% endif %}



```XAML
	<Style x:Key="{telerik:ThemeResourceKey ThemeType={x:Type local:RadDockingTheme}, ElementType={x:Type telerik:RadSplitContainer}}"
	TargetType="{x:Type telerik:RadSplitContainer}">
	    <!--...-->
	</Style>
```

{% if site.site_name == 'WPF' %}

To see how to apply the theme read [here](#ApplyingTheme).{% endif %}

Here is a snapshot of a sample result.

![{{ site.framework_name }} RadDocking Themed RadSplitContainer](images/RadDocking_ThemingSplitContainer_01.png)

## See Also

 * [Theming - Overview]({%slug raddocking-theming-overview%})

 * [Styling the RadSplitContainer]({%slug raddocking-styling-the-radsplitcontainer%})

 * [Split Container]({%slug raddocking-features-split-container%})
