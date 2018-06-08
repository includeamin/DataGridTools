# DataGridTools
Action on Datagrid
# Get value of selected Cell in dataGrid WPF
```
  private void DataGrid_SelectionChanged(object sender, SelectionChangedEventArgs e)
        {
            if (sender is DataGrid grid && grid.CurrentCell.Item is StockClass data)
            {
                UpdatePrice.Text = data.BasePrice;
                Title.Text = data.Name;
                UpdateCapacity.Text = data.Capacity.ToString();
                MinCountAlert.Text = data.MinCountAlert.ToString();

            }

            DialogHost.IsOpen = true;
        }
```
