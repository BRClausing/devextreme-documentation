---
EventForAction: ..\4 Events\pageLoading.md
default: null
type: function(e)
---
---
##### shortDescription
A handler for the [pageLoading](/api-reference/10%20UI%20Widgets/dxLookup/4%20Events/pageLoading.md '/Documentation/ApiReference/UI_Widgets/dxLookup/Events/#pageLoading') event.

##### param(e): Object
Information about the event.

##### field(e.component): DOMComponent
The widget's instance.

##### field(e.element): dxElement
The widget's container. It is an [HTML Element](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement) or a [jQuery Element](https://api.jquery.com/Types/#jQuery) when you use jQuery.

##### field(e.model): Object
The model data. Available only if Knockout is used.

---
Assign a function to perform a custom action before loading the next page in the lookup list if auto-paging is enabled.