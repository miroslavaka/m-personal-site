Firstly let me show on following picture which part of the pivot table is pivot item and pivot field.

![Excel1](/images/blog/excel-1.jpg)

Pivot item contains all items within one pivot field.
Pivot field contains data which create vertical and horizontal layout of pivot table.

When creating and working with pivot table, pivot cache becomes important. A PivotCache is invisible object, working behind scenes when a new pivot table is created directly from the source data. PivotCache holds a static copy of the source data in memory, so pivot table takes data from pivot cache container then directly from source data. If you change anything from existing data in the source data, the pivot table report does not reflect that change until you click the Refresh button. Holding data in cache causes that pivot table recalculation is quicker. Negative aspect is higher workbook size and less memory for other tasks.

AUTOMATIC CHANGE OF PIVOT ITEM AND REFRESH PIVOT TABLE
Folowing example demonstrates how to automaticly change filter in pivot item and then refresh pivot table. In the excel file I selected one cell where I created drop down list with all months (from 1 till 12) and I named this cell MonthToFilter.

![Excel2](/images/blog/excel-2.jpg)

Then my pivot table looks like:

![Excel3](/images/blog/excel-3.jpg)

I created the macro that changes actual Month in pivot table to Month selected in the cell MonthToFilter. Practically I changed Month 4 which is currently in the pivot table to Month 3 (selected in MonthToFilter) and then I refreshed pivot table.
Code looks like:

```
Sub RefreshPivot()
Dim sh As Worksheet
Dim pt As PivotTable
Dim pf As PivotField
Dim pi As PivotItem
Dim MonthToFilter As String

MonthToFilter = ThisWorkbook.Worksheets("Sheet2").Range("A2")
For Each sh In ThisWorkbook.Worksheets
For Each pt In sh.PivotTables
    Set pf = pt.PivotFields("Month")
    pf.PivotItems(MonthToFilter).Visible = True
        For Each pi In pf.PivotItems
            If Not pi = MonthToFilter Then
                pi.Visible = False
            End If
        Next pi
    Next pt
Next sh
End Sub
```

Result:
![Excel4](/images/blog/excel-4.jpg)

<div style="text-align: center;">
Thank you for stopping by and happy studying :)
</div>
