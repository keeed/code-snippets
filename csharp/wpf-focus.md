| **Description:** | Checks if the given control is currently in focus. |
| :--------------- | ---------------------------------------- |
| **Source:**      | https://social.msdn.microsoft.com/Forums/vstudio/en-US/e0512848-076b-464b-856c-70fcbf60489c/determine-if-datagrid-is-focused?forum=wpf |

```c#
private bool hasFocus(Control control, bool checkChildren)
{
    var oFocused = System.Windows.Input.FocusManager.GetFocusedElement(this) as DependencyObject;
    if (!checkChildren)
        return oFocused == control;

    while (oFocused != null)
    {
        if (oFocused == control)
            return true;
        oFocused = System.Windows.Media.VisualTreeHelper.GetParent(oFocused);
    }

    return false;
}
```

