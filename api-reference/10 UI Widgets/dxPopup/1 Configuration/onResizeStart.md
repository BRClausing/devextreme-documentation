---
EventForAction: ..\4 Events\resizeStart.md
default: null
type: function(e)
---
---
##### shortDescription
A handler for the [resizeStart](/api-reference/10%20UI%20Widgets/dxPopup/1%20Configuration/onResizeStart.md '/Documentation/ApiReference/UI_Widgets/dxPopup/Configuration/#onResizeStart') event.

##### param(e): Object
Information about the event.

##### field(e.component): DOMComponent
The widget's instance.

##### field(e.element): dxElement
The widget's container. It is an [HTML Element](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement) or a [jQuery Element](https://api.jquery.com/Types/#jQuery) when you use jQuery.

##### field(e.model): Object
The model data. Available only if Knockout is used.

---
Assign a function to perform a custom action after resizing has been finished.