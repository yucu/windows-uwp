---
author: Jwmsft
Description: Provides a list by function of some of the controls that you can use in your apps.
title: Controls by function
ms.assetid: 8DB4347B-91D6-4659-91F2-80ECF7BBB596
label: Controls by function
template: detail.hbs
ms.author: jimwalk
ms.date: 05/19/2017
ms.topic: article


keywords: windows 10, uwp
ms.localizationpriority: medium
---
# Controls by function

The XAML UI framework for Windows provides an extensive library of controls that support UI development. Some of these controls have a visual representation; others function as the containers for other controls or content, such as images and media. 

You can see many of the Windows UI controls in action by downloading the [XAML UI Basics sample](http://go.microsoft.com/fwlink/p/?LinkId=619992).

<table>
<th align="left">XAML Controls Gallery<th>
<tr>
<td><img src="images/xaml-controls-gallery-sm.png" alt="XAML controls gallery"></img></td>
<td>
    <p>If you have the <strong style="font-weight: semi-bold">XAML Controls Gallery</strong> app installed, click here to <a href="xamlcontrolsgallery:/item/NavigationView">open the app and see the NavigationView in action</a> </p>
    <ul>
    <li><a href="https://www.microsoft.com/store/productId/9MSVH128X2ZT">Get the XAML Controls Gallery app (Microsoft Store)</a></li>
    <li><a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/XamlUIBasics">Get the source code (GitHub)</a></li>
    </ul>
</td>
</tr>
</table>


Here's a list by function of the common XAML controls you can use in your app.

## Appbars and commands

### App bar
A toolbar for displaying application-specific commands. See Command bar.

Reference: [AppBar](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.appbar.aspx) 

### App bar button
A button for showing commands using app bar styling.

![App bar button icons](images/controls/app-bar-buttons.png) 

Reference: [AppBarButton](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.appbarbutton.aspx), [SymbolIcon](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.symbolicon.aspx), [BitmapIcon](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.bitmapicon.aspx), [FontIcon](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.fonticon.aspx), [PathIcon](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.pathicon.aspx) 

Design and how-to: [App bar and command bar control guide](app-bars.md) 

Sample code: [XAML Commanding sample](http://go.microsoft.com/fwlink/p/?LinkId=620019)

### App bar separator
Visually separates groups of commands in a command bar.

Reference: [AppBarSeparator](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.appbarseparator.aspx) 

Sample code: [XAML Commanding sample](http://go.microsoft.com/fwlink/p/?LinkId=620019)

### App bar toggle button
A button for toggling commands in a command bar.

Reference: [AppBarToggleButton](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.appbartogglebutton.aspx) 

Sample code: [XAML Commanding sample](http://go.microsoft.com/fwlink/p/?LinkId=620019)

### Command bar
A specialized app bar that handles the resizing of app bar button elements.

![Command bar control](images/command-bar-compact.png)

```xaml
<CommandBar>
    <AppBarButton Icon="Back" Label="Back" Click="AppBarButton_Click"/>
    <AppBarButton Icon="Stop" Label="Stop" Click="AppBarButton_Click"/>
    <AppBarButton Icon="Play" Label="Play" Click="AppBarButton_Click"/>
</CommandBar>
```
Reference: [CommandBar](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.commandbar.aspx) 

Design and how-to: [App bar and command bar control guide](app-bars.md)

Sample code: [XAML Commanding sample](http://go.microsoft.com/fwlink/p/?LinkId=620019)

## Buttons

### Button
A control that responds to user input and raises a **Click** event.

![A standard button](images/controls/button.png)

```xaml
<Button x:Name="button1" Content="Button" 
        Click="Button_Click" />
```

Reference: [Button](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.button.aspx) 

Design and how-to: [Buttons control guide](buttons.md) 

### Hyperlink
See Hyperlink button.

### Hyperlink button
A button that appears as marked up text and opens the specified URI in a browser.

![Hyperlink button](images/controls/hyperlink-button.png)

```xaml
<HyperlinkButton Content="www.microsoft.com" 
                 NavigateUri="http://www.microsoft.com"/>
```

Reference: [HyperlinkButton](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.hyperlinkbutton.aspx) 

Design and how-to: [Hyperlinks control guide](hyperlinks.md)

### Repeat button
A button that raises its **Click** event repeatedly from the time it's pressed until it's released. 

![A repeat button control](images/controls/repeat-button.png) 

```xaml
<RepeatButton x:Name="repeatButton1" Content="Repeat Button" 
              Click="RepeatButton_Click" />
```

Reference: [RepeatButton](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.primitives.repeatbutton.aspx) 

Design and how-to: [Buttons control guide](buttons.md) 

## Collection/data controls

### Flip view
A control that presents a collection of items that the user can flip through, one item at a time.

```xaml
<FlipView x:Name="flipView1" SelectionChanged="FlipView_SelectionChanged">
    <Image Source="Assets/Logo.png" />
    <Image Source="Assets/SplashScreen.png" />
    <Image Source="Assets/SmallLogo.png" />
</FlipView>
```

Reference: [FlipView](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.flipview.aspx) 

Design and how-to: [Flip view control guide](flipview.md) 

### Grid view
A control that presents a collection of items in rows and columns that can scroll vertically.

```xaml
<GridView x:Name="gridView1" SelectionChanged="GridView_SelectionChanged">
    <x:String>Item 1</x:String>
    <x:String>Item 2</x:String>
</GridView>
```

Reference: [GridView](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.gridview.aspx) 

Design and how-to: [Lists](lists.md) 

Sample code: [ListView sample](http://go.microsoft.com/fwlink/p/?LinkId=619900)

### Items control
A control that presents a collection of items in a UI specified by a data template. 

```xaml
<ItemsControl/>
```

Reference: [ItemsControl](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.itemscontrol.aspx) 

### List view
A control that presents a collection of items in a list that can scroll vertically.

```xaml
<ListView x:Name="listView1" SelectionChanged="ListView_SelectionChanged">
    <x:String>Item 1</x:String>
    <x:String>Item 2</x:String>
</ListView>
```

Reference: [ListView](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.listview.aspx) 

Design and how-to: [Lists](lists.md) 

Sample code: [ListView sample](http://go.microsoft.com/fwlink/p/?LinkId=619900)

## Date and time controls

### Calendar date picker
A control that lets a user select a date using a drop-down calendar display.

![A calendar date picker with open calendar view](images/controls/calendar-date-picker-open.png)

```xaml
<CalendarDatePicker/>
```

Reference: [CalendarDatePicker](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.calendardatepicker.aspx) 

Design and how-to: [Calendar, date, and time controls](date-and-time.md)
 
### Calendar view
A configurable calendar display that lets a user select single or multiple dates.

```xaml
<CalendarView/>
```

Reference: [CalendarView](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.calendarview.aspx) 

Design and how-to: [Calendar, date, and time controls](date-and-time.md) 

### Date picker
A control that lets a user select a date.

![Date picker control](images/controls/date-picker.png)

```xaml
<DatePicker Header="Arrival Date"/>
```

Reference: [DatePicker](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.datepicker.aspx) 

Design and how-to: [Calendar, date, and time controls](date-and-time.md)
 
### Time picker
A control that lets a user set a time value.

![TimePicker control](images/controls/time-picker.png) 

```xaml
<TimePicker Header="Arrival Time"/>
```

Reference: [TimePicker](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.timepicker.aspx) 

Design and how-to: [Calendar, date, and time controls](date-and-time.md)

## Flyouts

### Context menu
See Menu flyout and Popup menu.

### Flyout
Displays a message that requires user interaction. (Unlike a dialog, a flyout does not create a separate window, and does not block other user interaction.)

![Flyout control](images/controls/flyout.png)

```xaml
<Flyout>
    <StackPanel>
        <TextBlock Text="All items will be removed. Do you want to continue?"/>
        <Button Click="DeleteConfirmation_Click" Content="Yes, empty my cart"/>
    </StackPanel>
</Flyout>
```

Reference: [Flyout](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.flyout.aspx) 

Design and how-to: [Flyouts](dialogs-and-flyouts/flyouts.md) 

### Menu flyout
Temporarily displays a list of commands or options related to what the user is currently doing.

![Menu flyout control](images/controls/menu-flyout.png) 

```xaml
<MenuFlyout>
    <MenuFlyoutItem Text="Reset" Click="Reset_Click"/>
    <MenuFlyoutSeparator/>
    <ToggleMenuFlyoutItem Text="Shuffle" 
                          IsChecked="{Binding IsShuffleEnabled, Mode=TwoWay}"/>
    <ToggleMenuFlyoutItem Text="Repeat" 
                          IsChecked="{Binding IsRepeatEnabled, Mode=TwoWay}"/>
</MenuFlyout>
```

Reference: [MenuFlyout](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.menuflyout.aspx), [MenuFlyoutItem](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.menuflyoutitem.aspx), [MenuFlyoutSeparator](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.menuflyoutseparator.aspx), [ToggleMenuFlyoutItem](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.togglemenuflyoutitem.aspx) 

Design and how-to: [Menus and context menus](menus.md) 

Sample code: [XAML Context Menu sample](http://go.microsoft.com/fwlink/p/?LinkId=620021)

### Popup menu
A custom menu that presents commands that you specify.

Reference: [PopupMenu](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.popups.popupmenu.aspx) 

Design and how-to: [Dialogs](dialogs-and-flyouts/dialogs.md) 

### Tooltip
A pop-up window that displays information for an element. 
 
![Tool tip control](images/controls/tool-tip.png)

```xaml
<Button Content="Button" Click="Button_Click" 
        ToolTipService.ToolTip="Click to perform action" />
```

Reference: [ToolTip](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.tooltip.aspx), [ToolTipService](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.tooltipservice.aspx) 

Design and how-to: Guidelines for tooltips 

## Images

### Image
A control that presents an image.

```xaml
<Image Source="Assets/Logo.png" />
```

Reference: [Image](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.image.aspx) 

Design and how-to: [Image and ImageBrush](images-imagebrushes.md) 

Sample code: [XAML images sample](http://go.microsoft.com/fwlink/p/?linkid=226867)

## Graphics and ink

### InkCanvas
A control that receives and displays ink strokes.

```xaml
<InkCanvas/>
```

Reference: [InkCanvas](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.inkcanvas.aspx) 

### Shapes
Various retained mode graphical objects that can be presented like ellipses, rectangles, lines, Bezier paths, etc.

![A polygon](images/controls/shapes-polygon.png) 
![A path](images/controls/shapes-path.png) 

```xaml
<Ellipse/>
<Path/>
<Rectangle/>
```

Reference: [Shapes](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.shapes.shape.aspx) 

How to: [Drawing shapes](../../graphics/drawing-shapes.md) 

Sample code: [XAML vector-based drawing sample](http://go.microsoft.com/fwlink/p/?linkid=226866)

## Layout controls

### Border
A container control that draws a border, background, or both, around another object.

![A border around 2 rectangles](images/controls/border.png) 

```xaml
<Border BorderBrush="Blue" BorderThickness="4" 
        Height="108" Width="64" 
        Padding="8" CornerRadius="4">
    <Canvas>
        <Rectangle Fill="Orange"/>
        <Rectangle Fill="Green" Margin="0,44"/>
    </Canvas>
</Border>
```

Reference: [Border](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.border.aspx)

### Canvas
A layout panel that supports the absolute positioning of child elements relative to the top left corner of the canvas.
 
![Canvas layout panel](images/controls/canvas.png) 

```xaml
<Canvas Width="120" Height="120">
    <Rectangle Fill="Red"/>
    <Rectangle Fill="Blue" Canvas.Left="20" Canvas.Top="20"/>
    <Rectangle Fill="Green" Canvas.Left="40" Canvas.Top="40"/>
    <Rectangle Fill="Orange" Canvas.Left="60" Canvas.Top="60"/>
</Canvas>
```

Reference: [Canvas](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.canvas.aspx)
 
### Grid
A layout panel that supports the arranging of child elements in rows and columns.

![Grid layout panel](images/controls/grid.png) 

```xaml
<Grid>
    <Grid.RowDefinitions>
        <RowDefinition Height="50"/>
        <RowDefinition Height="50"/>
    </Grid.RowDefinitions>
    <Grid.ColumnDefinitions>
        <ColumnDefinition Width="50"/>
        <ColumnDefinition Width="50"/>
    </Grid.ColumnDefinitions>
    <Rectangle Fill="Red"/>
    <Rectangle Fill="Blue" Grid.Row="1"/>
    <Rectangle Fill="Green" Grid.Column="1"/>
    <Rectangle Fill="Orange" Grid.Row="1" Grid.Column="1"/>
</Grid>
```

Reference: [Grid](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.grid.aspx)
 
### Panning scroll viewer
See Scroll viewer.

### RelativePanel
A panel that lets you position and align child objects in relation to each other or the parent panel.

![Relative panel layout panel](images/controls/relative-panel.png) 

```xaml
<RelativePanel>
    <TextBox x:Name="textBox1" RelativePanel.AlignLeftWithPanel="True"/>
    <Button Content="Submit" RelativePanel.Below="textBox1"/>
</RelativePanel>
```

Reference: [RelativePanel](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.relativepanel.aspx)

### Scroll bar
See scroll viewer. (ScrollBar is an element of ScrollViewer. You don't typically use it as a stand-alone control.)

Reference: [ScrollBar](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.primitives.scrollbar.aspx)
 
### Scroll viewer
A container control that lets the user pan and zoom its content.

```xaml
<ScrollViewer ZoomMode="Enabled" MaxZoomFactor="10" 
              HorizontalScrollMode="Enabled" 
              HorizontalScrollBarVisibility="Visible"
              Height="200" Width="200">
    <Image Source="Assets/Logo.png" Height="400" Width="400"/>
</ScrollViewer>
```

Reference: [ScrollViewer](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.scrollviewer.aspx)

Design and how-to: [Scroll and panning controls guide](scroll-controls.md) 

Sample code: [XAML scrolling, panning and zooming sample](http://go.microsoft.com/fwlink/p/?linkid=238577)

### Stack panel
A layout panel that arranges child elements into a single line that can be oriented horizontally or vertically.

![Stack panel layout control](images/controls/stack-panel.png) 

```xaml
<StackPanel>
    <Rectangle Fill="Red"/>
    <Rectangle Fill="Blue"/>
    <Rectangle Fill="Green"/>
    <Rectangle Fill="Orange"/>
</StackPanel>
```

Reference: [StackPanel](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.stackpanel.aspx)
 
### VariableSizedWrapGrid
A layout panel that supports the arranging of child elements in rows and columns. Each child element can span multiple rows and columns.

![Variable sized wrap grid layout panel](images/controls/variable-sized-wrap-grid.png) 

```xaml
<VariableSizedWrapGrid MaximumRowsOrColumns="3" ItemHeight="44" ItemWidth="44">
    <Rectangle Fill="Red"/>
    <Rectangle Fill="Blue" Height="80" 
               VariableSizedWrapGrid.RowSpan="2"/>
    <Rectangle Fill="Green" Width="80" 
               VariableSizedWrapGrid.ColumnSpan="2"/>
    <Rectangle Fill="Orange" Height="80" Width="80" 
               VariableSizedWrapGrid.RowSpan="2" 
               VariableSizedWrapGrid.ColumnSpan="2"/>
</VariableSizedWrapGrid>
```

Reference: [VariableSizedWrapGrid](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.variablesizedwrapgrid.aspx)

### Viewbox
A container control that scales its content to a specified size.

![Viewbox control](images/controls/view-box.png) 

```xaml
<Viewbox MaxWidth="25" MaxHeight="25">
    <Image Source="Assets/Logo.png"/>
</Viewbox>
<Viewbox MaxWidth="75" MaxHeight="75">
    <Image Source="Assets/Logo.png"/>
</Viewbox>
<Viewbox MaxWidth="150" MaxHeight="150">
    <Image Source="Assets/Logo.png"/>
</Viewbox>
```

Reference: [Viewbox](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.viewbox.aspx)
 
### Zooming scroll viewer
See Scroll viewer.

## Media controls

### Audio
See Media element.

### Media element
A control that plays audio and video content.

```xaml
<MediaElement x:Name="myMediaElement"/>
```

Reference: [MediaElement](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.mediaelement.aspx) 

Design and how-to: [Media element control guide](media-playback.md)

### MediaTransportControls
A control that provides playback controls for a MediaElement.

![Media element with transport controls](images/controls/media-transport-controls.png) 

```xaml
<MediaTransportControls MediaElement="myMediaElement"/>
```

Reference: [MediaTransportControls](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.mediatransportcontrols.aspx) 

Design and how-to: [Media element control guide](media-playback.md) 

Sample code: [Media Transport Controls sample](http://go.microsoft.com/fwlink/p/?LinkId=620023)

### Video
See Media element.

## Navigation

### NavigationView

An adaptable container and flexible navigation model that implements the left navigation pane, top navigation and tabs pattern.

Reference: [NavigationView](https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.navigationview)

Design and how-to: [NavigationView control guide](navigationview.md)

### SplitView

A container control with two views; one view for the main content and another view that is typically used for a navigation menu.

![Split view control](images/controls/split-view.png) 

```xaml
<SplitView>
    <SplitView.Pane>
        <!-- Menu content -->
    </SplitView.Pane>
    <SplitView.Content>
        <!-- Main content -->
    </SplitView.Content>
</SplitView>
```

Reference: [SplitView](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.splitview.aspx) 

Design and how-to: [Split view control guide](split-view.md)

### Web view

A container control that hosts web content.

```xaml
<WebView x:Name="webView1" Source="http://dev.windows.com" 
         Height="400" Width="800"/>
```

Reference: [WebView](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.webview.aspx) 

Design and how-to: Guidelines for Web views 

Sample code: [XAML WebView control sample](http://go.microsoft.com/fwlink/p/?linkid=238582)

### Semantic zoom

A container control that lets the user zoom between two views of a collection of items.

```xaml
<SemanticZoom>
    <ZoomedInView>
        <GridView></GridView>
    </ZoomedInView>
    <ZoomedOutView>
        <GridView></GridView>
    </ZoomedOutView>
</SemanticZoom>
```

Reference: [SemanticZoom](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.semanticzoom.aspx) 

Design and how-to: [Semantic zoom control guide](semantic-zoom.md)

Sample code: [XAML GridView grouping and SemanticZoom sample](http://go.microsoft.com/fwlink/p/?linkid=226564)

## Progress controls

### Progress bar
A control that indicates progress by displaying a bar.

![Progress bar control](images/controls/progress-bar-determinate.png)

A progress bar that shows a specific value.

```xaml
<ProgressBar x:Name="progressBar1" Value="50" Width="100"/>
```

![Indeterminate progress bar control](images/controls/progress-bar-indeterminate.png)

A progress bar that shows indeterminate progress.

```xaml
<ProgressBar x:Name="indeterminateProgressBar1" IsIndeterminate="True" Width="100"/>
```

Reference: [ProgressBar](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.progressbar.aspx) 

Design and how-to: [Progress controls guide](progress-controls.md) 

### Progress ring
A control that indicates indeterminate progress by displaying a ring. 

![Progress ring control](images/controls/progress-ring.png) 

```xaml
<ProgressRing x:Name="progressRing1" IsActive="True"/>
```

Reference: [ProgressRing](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.progressring.aspx) 

Design and how-to: [Progress controls guide](progress-controls.md) 

## Text controls

### Auto suggest box
A text input box that provides suggested text as the user types.

![An auto suggest box for search](images/controls/auto-suggest-box.png) 

Reference: [AutoSuggestBox](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.autosuggestbox.aspx)

Design and how-to: [Text controls](text-controls.md), [Auto suggest box control guide](auto-suggest-box.md)

Sample code: [AutoSuggestBox migration sample](http://go.microsoft.com/fwlink/p/?LinkId=619996)

### Multi-line text box
See Text box.

### Password box
A control for entering passwords.

 ![A password box](images/controls/password-box.png)

```xaml
<PasswordBox x:Name="passwordBox1" 
             PasswordChanged="PasswordBox_PasswordChanged" />
```

Reference: [PasswordBox](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.passwordbox.aspx) 

Design and how-to: [Text controls](text-controls.md), [Password box control guide](password-box.md) 

Sample code: [XAML text display sample](http://go.microsoft.com/fwlink/p/?linkid=238579), [XAML text editing sample](http://go.microsoft.com/fwlink/p/?linkid=251417)

### Rich edit box
A control that lets a user edit rich text documents with content like formatted text, hyperlinks, and images.

```xaml
<RichEditBox />
```

Reference: [RichEditBox](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.richeditbox.aspx) 

Design and how-to: [Text controls](text-controls.md), [Rich edit box control guide](rich-edit-box.md)

Sample code: [XAML text sample](http://go.microsoft.com/fwlink/p/?linkid=238578)

### Search box
See Auto suggest box.

### Single-line text box
See Text box.

### Static text/paragraph
See Text block.

### Text block
A control that displays text.

![Text block control](images/controls/text-block.png) 

```xaml
<TextBlock x:Name="textBlock1" Text="I am a TextBlock"/>
```

Reference: [TextBlock](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.textblock.aspx), [RichTextBlock](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.richtextblock.aspx) 

Design and how-to: [Text controls](text-controls.md), [Text block control guide](text-block.md), [Rich text block control guide](rich-text-block.md)

Sample code: [XAML text sample](http://go.microsoft.com/fwlink/p/?linkid=238578)

### Text box
A single-line or multi-line plain text field.

![Text box control](images/controls/text-box.png) 

```xaml
<TextBox x:Name="textBox1" Text="I am a TextBox" 
         TextChanged="TextBox_TextChanged"/>
```

Reference: [TextBox](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.textbox.aspx) 

Design and how-to: [Text controls](text-controls.md), [Text box control guide](text-box.md) 

Sample code: [XAML text sample](http://go.microsoft.com/fwlink/p/?linkid=238578)

## Selection controls

### Check box
A control that a user can select or clear.

![The 3 states of a check box](images/templates-checkbox-states-default.png)

```xaml
<CheckBox x:Name="checkbox1" Content="CheckBox" 
          Checked="CheckBox_Checked"/>
```

Reference: [CheckBox](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.checkbox.aspx) 

Design and how-to: [Check box control guide](checkbox.md) 

### Combo box
A drop-down list of items a user can select from.

![Open combo box](images/controls/combo-box-open.png) 

```xaml
<ComboBox x:Name="comboBox1" Width="100"
          SelectionChanged="ComboBox_SelectionChanged">
    <x:String>Item 1</x:String>
    <x:String>Item 2</x:String>
    <x:String>Item 3</x:String>
</ComboBox>
```

Reference: [ComboBox](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.combobox.aspx) 

Design and how-to: [Lists](lists.md) 

### List box
A control that presents an inline list of items that the user can select from. 

![List box control](images/controls/list-box.png)

```xaml
<ListBox x:Name="listBox1" Width="100"
         SelectionChanged="ListBox_SelectionChanged">
    <x:String>Item 1</x:String>
    <x:String>Item 2</x:String>
    <x:String>Item 3</x:String>
</ListBox>
```

Reference: [ListBox](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.listbox.aspx) 

Design and how-to: [Lists](lists.md) 

### Radio button
A control that allows a user to select a single option from a group of options. When radio buttons are grouped together, they are mutually exclusive.

![Radio button controls](images/controls/radio-button.png)

```xaml
<RadioButton x:Name="radioButton1" Content="RadioButton 1" GroupName="Group1" 
             Checked="RadioButton_Checked"/>
<RadioButton x:Name="radioButton2" Content="RadioButton 2" GroupName="Group1" 
             Checked="RadioButton_Checked" IsChecked="True"/>
<RadioButton x:Name="radioButton3" Content="RadioButton 3" GroupName="Group1" 
             Checked="RadioButton_Checked"/>
```

Reference: [RadioButton](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.radiobutton.aspx) 

Design and how-to: [Radio button control guide](radio-button.md)
 
### Slider
A control that lets the user select from a range of values by moving a Thumb control along a track.

![Slider control](images/controls/slider.png)

```xaml
<Slider x:Name="slider1" Width="100" ValueChanged="Slider_ValueChanged" />
```

Reference: [Slider](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.slider.aspx) 

Design and how-to: [Slider control guide](slider.md) 

### Toggle button
A button that can be toggled between 2 states.

```xaml
<ToggleButton x:Name="toggleButton1" Content="Button" 
              Checked="ToggleButton_Checked"/>
```

Reference: [ToggleButton](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.primitives.togglebutton.aspx)

Design and how-to: [Toggle control guide](toggles.md) 

### Toggle switch
A switch that can be toggled between 2 states.

![Toggle switch control](images/controls/toggle-switch.png) 

```xaml
<ToggleSwitch x:Name="toggleSwitch1" Header="ToggleSwitch" 
              OnContent="On" OffContent="Off" 
              Toggled="ToggleSwitch_Toggled"/>
```

Reference: [ToggleSwitch](https://msdn.microsoft.com/library/windows/apps/xaml/windows.ui.xaml.controls.toggleswitch.aspx) 

Design and how-to: [Toggle control guide](toggles.md) 
