| Description: | Adds an empty row to an editable data grid in WPF. See method summary for full info. |
| :----------- | :--------------------------------------- |
| **Source:**  |                                          |

```c#
/// <summary>
/// Adds an empty row to an editable data grid.
/// The scenario is when an ObservableCollection that is binded to the DataGrid
/// has one of its elements removed and the underlying ItemsView is refreshed, the last
/// empty row will be deleted. Call this method to add the last empty row again.
/// </summary>
/// <param name="dataGrid">DataGrid where the empty row will be added.</param>
private void addEmptyRowToEditableDataGrid(DataGrid dataGrid)
{
    // Set the 'CanUserAddRows' to 'false' first and then
    // set it to 'true'. This will add a new empty row.
    dataGrid.CanUserAddRows = false;
    dataGrid.CanUserAddRows = true;
}
```

