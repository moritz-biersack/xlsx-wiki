# Freeze Panes

By freezing panes, one can lock rows and columns while scrolling to another
area of a sheet:

```go
pane := xlsx.Pane{
    XSplit: 1, // lock rows
    YSplit: 1, // lock columns
    TopLeftCell: "B2", // Cell shown in the scrollable area
    ActivePane: "topRight",
    State: "frozen",
}
sheetView := xlsx.SheetView{Pane: &pane}

// Set the SheetViews of an existing xlsx.Sheet
sheet.SheetViews = []xlsx.SheetView{sheetView}
```
