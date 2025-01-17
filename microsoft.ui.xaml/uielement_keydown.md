---
-api-id: E:Microsoft.UI.Xaml.UIElement.KeyDown
-api-type: winrt event
---

<!-- Event syntax
public event Microsoft.UI.Xaml.Input.KeyEventHandler KeyDown
-->

# Microsoft.UI.Xaml.UIElement.KeyDown

## -description

Occurs when a keyboard key is pressed while the [UIElement](uielement.md) has focus.

## -xaml-syntax

```xaml
<uiElement KeyDown="eventhandler"/>
```

## -remarks

Controls in your UI generate keyboard events only when they have input focus. By default, the first focusable element in the visual tree is given focus by the system. An individual control gains focus when the user clicks or taps directly on that control in the layout, or uses the Tab key to step into a tab sequence within the content area. You can also focus controls programmatically by calling [UIElement.Focus(Microsoft.UI.Xaml.FocusState)](uielement_focus_1914077590.md).

`KeyDown` is a routed event. For more info on the routed event concept, see [Events and routed events overview](/windows/uwp/xaml-platform/events-and-routed-events-overview).

`KeyDown` uses [KeyRoutedEventArgs](../microsoft.ui.xaml.input/keyroutedeventargs.md) event data. The most relevant properties of `KeyRoutedEventArgs` for most handler scenarios are [Key](../microsoft.ui.xaml.input/keyroutedeventargs_key.md) and possibly [KeyStatus](../microsoft.ui.xaml.input/keyroutedeventargs_keystatus.md). For more info on handling keyboard events, including example code for defining a [KeyEventHandler](../microsoft.ui.xaml.input/keyeventhandler.md) method, see [Keyboard interactions](/windows/uwp/input-and-devices/keyboard-interactions).

One scenario for handling keyboard events is to support access keys or accelerator keys for an app, or a region or control within an app. For more info about this scenario, see [Keyboard accessibility](/windows/uwp/accessibility/keyboard-accessibility).

Specific Windows Runtime controls may have class-based handling for the KeyDown input event. If so, the control probably has an override for the method [OnKeyDown](../microsoft.ui.xaml.controls/control_onkeydown_647020286.md). Typically these class handlers are intended to process a subset of key presses that enable a keyboard-based user interaction with that control, and often this interaction supports a keyboard accessibility feature. If a key press is handled by class-based handling, then the key press is considered to be already handled, and the KeyDown event is not raised for handling by any user code handlers on that control for that key specifically. Usually this is just for a few dedicated keys. For example, [ButtonBase](../microsoft.ui.xaml.controls.primitives/buttonbase.md) has class handling so that the _Space_ key and _Enter_ key are handled as keyboard equivalents for invoking the [Button](../microsoft.ui.xaml.controls/button.md). That provides a built-in keyboard equivalent for tapping the button or clicking on it with a mouse, and enables the accessibility scenario of using the UI and the button using a keyboard only. But any other keys other than _Space_ or _Enter_ will still fire a KeyDown and [KeyUp](uielement_keyup.md) event for a `Button`. For more info on how class-based handling for events works, see [Events and routed events overview](/windows/uwp/xaml-platform/events-and-routed-events-overview).

`KeyDown` supports the ability to attach event handlers to the route that will be invoked even if the event data for the event is marked [Handled](../microsoft.ui.xaml.input/keyroutedeventargs_handled.md). See [AddHandler](uielement_addhandler_1350394113.md).

## -examples

## -see-also

[KeyRoutedEventArgs](../microsoft.ui.xaml.input/keyroutedeventargs.md), [KeyUp](uielement_keyup.md), [GotFocus](uielement_gotfocus.md), [OnKeyDown](../microsoft.ui.xaml.controls/control_onkeydown_647020286.md), [Keyboard interactions](/windows/uwp/input-and-devices/keyboard-interactions), [Events and routed events overview](/windows/uwp/xaml-platform/events-and-routed-events-overview), [XAML user input events sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Input%20XAML%20user%20input%20events%20sample)
