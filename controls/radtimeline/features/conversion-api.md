---
title: Conversion API
page_title: Conversion API
description: Check our &quot;Conversion API&quot; documentation article for the RadTimeline {{ site.framework_name }} control.
slug: radtimeline-features-conversion-api
tags: conversion,api,convertpointtodatetime
published: True
position: 13
---

# Conversion API 

__RadTimeline__ allows you to convert a screen coordinates (a Point), to a DateTime value plotted on the timebar control. You can do that via the __ConvertPointToDateTime__ method of RadTimeline. The method excepts an argument of type __Point__ and it returns a __DateTime__ object.

__Example 1: Getting the DateTime under the mouse__ 
```C#
	private void UIElement_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
	{
		Point mousePosition = e.GetPosition(radTimeline);
		DateTime date = radTimeline.ConvertPointToDateTime(mousePosition);
	}
```

## See Also
 * [Getting Started]({%slug radtimebar-mvvm-support%})
 * [Properties]({%slug radtimebar-properties%})
