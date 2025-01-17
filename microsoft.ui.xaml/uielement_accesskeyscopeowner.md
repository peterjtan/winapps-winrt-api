---
-api-id: P:Microsoft.UI.Xaml.UIElement.AccessKeyScopeOwner
-api-type: winrt property
---

<!-- Property syntax
public Microsoft.UI.Xaml.DependencyObject AccessKeyScopeOwner { get;  set; }
-->

# Microsoft.UI.Xaml.UIElement.AccessKeyScopeOwner

## -description

Gets or sets a source element that provides the access key scope for this element, even if it's not in the visual tree of the source element.

## -property-value

The element that defines the access key scope.

## -remarks

The source element must have it's [IsAccessKeyScope](uielement_isaccesskeyscope.md) property set to `true`.

## -examples

## -see-also

[Access keys](/windows/apps/design/input/access-keys)
