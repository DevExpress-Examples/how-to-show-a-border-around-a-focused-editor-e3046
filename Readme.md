<!-- default file list -->
*Files to look at*:

* [MainPage.xaml](./CS/SLEditorsTemplating/MainPage.xaml) (VB: [MainPage.xaml](./VB/SLEditorsTemplating/MainPage.xaml))
* [SLEditorsFocusFrame.xaml](./CS/SLEditorsTemplating/Themes/SLEditorsFocusFrame.xaml) (VB: [SLEditorsFocusFrame.xaml](./VB/SLEditorsTemplating/Themes/SLEditorsFocusFrame.xaml))
<!-- default file list end -->
# How to show a border around a focused editor


<p>This example shows the way to change visual appearance of a focused editor.  Let's assume that the editor must show an additional border when focused. There is three steps.</p><p>1. It's necessary to create a custom template for a control and place a new border element there.<br />
2. Next, bind the border's Visibility property to the IsKeyboardFocusWithin property of the editor.<br />
3. Create a new style with template setter and apply this style to the editor.</p><p>There are three new templates in the attached solution: the first for TextEdit, the second for PasswordBoxEdit and the third for button-based controls (ComboBoxEdit, SpinEdit, PopupCalcEdit, LookUpEdit...) Inside each of these templates is placed a rectangle named "FocusFrame" which is playing the role of the focus border, and it's Visibility property is bound to the IsKeyboardFocusWithin property of the control. Note that BoolToVisibilityConverter is used in this binding. Described templates are applied to editors through a number of implicit styles for a every DXEditor type. Both styles and all templates listed above are placed in "SLEditorsFocusFrame" resource dictionary.</p>

<br/>


