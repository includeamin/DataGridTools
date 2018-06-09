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
# change color of datagrid row depend on cell value
 ```
  <DataGrid Grid.Row="1"  x:Name="DataGrid"  SelectionChanged="DataGrid_SelectionChanged" AreRowDetailsFrozen="True">
                        <DataGrid.RowStyle>
                            <Style TargetType="DataGridRow">
                                <Style.Triggers>
                                    <DataTrigger Binding="{Binding State}" Value="LOW">
                                        <Setter Property="Background" Value="Red"></Setter>
                                    </DataTrigger>
                                   
                                </Style.Triggers>
                            </Style>
                        </DataGrid.RowStyle>
                    </DataGrid>
 ```
