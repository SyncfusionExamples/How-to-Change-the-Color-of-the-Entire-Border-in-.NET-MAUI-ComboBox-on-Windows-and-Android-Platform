# How-to-Change-the-Color-of-the-Entire-Border-in-.NET-MAUI-ComboBox-on-Windows-and-Android-Platform
This repository contains a sample explaining how to Change the Color of the Entire Border in .NET MAUI ComboBox on Windows and Android Platform
## Customizing ComboBox Border

To customize the border color of the .NET MAUI ComboBox (SfComboBox) on Windows and Android platforms, you can create a full border effect by wrapping the ComboBox within a Border control and setting ShowBorder="False" on the ComboBox itself. This allows full control over the ComboBox border’s color, thickness, and shape. Here’s an example:

**XAML**
```xml
<ContentPage.Resources>
    <!-- Define a Style for the ComboBox Border -->
    <Style TargetType="Border" x:Key="ComboBoxBorderStyle">
        <Setter Property="Stroke" Value="Red"/>
        <Setter Property="StrokeThickness" Value="2"/>
        <Setter Property="StrokeShape" Value="RoundRectangle 5"/>
    </Style>
</ContentPage.Resources>

<StackLayout Padding="20">
    <!-- Wrap SfComboBox in a Border to customize its appearance -->
    <Border Style="{StaticResource ComboBoxBorderStyle}">
        <editors:SfComboBox  
                ShowBorder="False"
                Placeholder="Select Here">
            <editors:SfComboBox.ItemsSource>
                <x:Array Type="{x:Type x:String}">
                    <x:String>Uganda</x:String>
                    <x:String>Ukraine</x:String>
                    <x:String>United States</x:String>
                    <x:String>United Kingdom</x:String>
                    <x:String>Uzbekistan</x:String>
                </x:Array>
            </editors:SfComboBox.ItemsSource>
        </editors:SfComboBox>
    </Border>
</StackLayout>
```

**Output:**


![ComboBoxBorder.png](https://support.syncfusion.com/kb/agent/attachment/article/17783/inline?token=eyJhbGciOiJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGRzaWctbW9yZSNobWFjLXNoYTI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjMxMTQwIiwib3JnaWQiOiIzIiwiaXNzIjoic3VwcG9ydC5zeW5jZnVzaW9uLmNvbSJ9.ALZzSGEF6GYBkaJFoODVPZp5FOJBDUs8dB5cmOPcO_A)
