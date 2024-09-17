# how-to-load-drag-view-indicator-in-.net-maui-listview.

This example demonstrates about how to load drag view indicator in .NET MAUI ListView(SfListView).

```
<ContentPage xmlns:syncfusion="clr-namespace:Syncfusion.Maui.ListView;assembly=Syncfusion.Maui.ListView"
             xmlns:data="clr-namespace:Syncfusion.Maui.DataSource;assembly=Syncfusion.Maui.DataSource"
             xmlns:local="clr-namespace:ListViewMaui;assembly=ListViewMaui"
             x:Class="ListViewMaui.MainPage">
        <syncfusion:SfListView x:Name="listView"  ScrollBarVisibility="Never" 
                           ItemSize="60"
                           BackgroundColor="#FFE8E8EC"
                           ItemsSource="{Binding ToDoList}"
                           DragStartMode="OnHold,OnDragIndicator"
                           SelectionMode="None">
            <syncfusion:SfListView.ItemTemplate>
                <DataTemplate>
                    <Grid  BackgroundColor="White">
                        ----
                        <syncfusion:DragIndicatorView Grid.Column="2" ListView="{x:Reference listView}" HorizontalOptions="Center" VerticalOptions="Center">
                            <Grid Padding="10, 20, 20, 20">
                                <Image Source="dragindicator.png" VerticalOptions="Center" HorizontalOptions="Center" />
                            </Grid>
                        </syncfusion:DragIndicatorView>
                    </Grid>
                </DataTemplate>
            </syncfusion:SfListView.ItemTemplate>
        </syncfusion:SfListView>
    </Grid>
</ContentPage>
```

## Requirements to run the demo

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) or [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/)
* Xamarin add-ons for Visual Studio (available via the Visual Studio installer).

## Troubleshooting

### Path too long exception

If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.