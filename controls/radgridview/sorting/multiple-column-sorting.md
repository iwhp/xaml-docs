---
title: Multiple-Column Sorting
page_title: Multiple-Column Sorting
description: Learn how you can sort data in Telerik's WPF DataGrid ascending by the Est. column and then sort again by the Stadium column without removing previous sorting.
slug: gridview-multiple-column-sorting
tags: multiple-column,sorting
published: True
position: 3
---

# Multiple-Column Sorting

The `RadGridView` control allows you to sort multiple columns. To do this at run-time, hold the __Shift__ key when clicking on the column headers. To change this, refer to the [Specify Multiple-Column Sorting Modifier Keys]({%slug gridview-multiple-column-sorting%}#specify-multiple-column-sorting-modifier-keys) section of this article.

On the snapshot below, the data in RadGridView is sorted ascending by the Est. column and then sorted again by the Stadium column, without removing the previous sorting.
       
![Telerik WPF DataGrid MultiColumnSorting 1](images/RadGridView_MultiColumnSorting_1.png)

To learn how to implement programmatic sorting in your RadGridView, read on this [article]({%slug gridview-sorting-programmatic%}).

## Column Sort Sequence Indicator

The RadGridView control allows you to display sequence indicators for the sorting operations. To enable this, set the `ShowColumnSortIndexes` property of RadGridView to __True__. 

You can check how the column headers will look like after the user has sorted on multiple columns.

![Telerik WPF DataGrid MultiColumnSorting 2](images/RadGridView_MultiColumnSorting_2.png)

## Specify Multiple-Column Sorting Modifier Keys

RadGridView provides the option to specify the modifier keys when performing multi-column sorting. This is done via the `MultipleColumnSortModifiers` property of RadGridView and it is of the type of [ModifierKeys](https://learn.microsoft.com/en-us/dotnet/api/system.windows.input.modifierkeys?view=windowsdesktop-8.0). The default value of the MultipleColumnSortModifiers property is `ModifierKeys.Shift`.

__Setting the modifier key to the Ctrl key for the multi-column sorting__
```XAML
    <telerik:RadGridView ItemsSource="{Binding Clubs}" MultipleColumnSortModifiers="Ctrl"/>
```

You can specify multiple modifier keys that will have to be held when clicking on the column headers, in order to execute the multi-column sorting. To specify them, separate them with the __+__ sign when setting the MultipleColumnSortModifiers property.

__Setting multiple modifier keys to the MultipleColumnSortModifiers property__
```XAML
    <telerik:RadGridView ItemsSource="{Binding Clubs}" MultipleColumnSortModifiers="Ctrl+Shift"/>
```

__Setting multiple modifier keys to the MultipleColumnSortModifiers property__
```C#
    this.gridView.MultipleColumnSortModifiers = ModifierKeys.Control | ModifierKeys.Shift;
```

>tip Setting the MultipleColumnSortModifiers property to an empty value will allow you to sort multiple columns without holding a modifier key.

## See Also
 * [RadGridView Overview]({%slug gridview-overview2%})
 * [Basic Sorting]({%slug gridview-sorting-basics%})
 * [Programmatic Sorting]({%slug gridview-sorting-programmatic%})
 * [Custom Sorting]({%slug gridview-sorting-custom%})
