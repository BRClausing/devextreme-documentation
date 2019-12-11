---
type: eventType
---
---
##### shortDescription
Fires before displaying a context menu invoked by a right-click on one of the field chooser's fields.

##### param(e): object
Information about the event.

##### field(e.component): DOMComponent
The widget's instance.

##### field(e.element): dxElement
The widget's container. It is an [HTML Element](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement) or a [jQuery Element](https://api.jquery.com/Types/#jQuery) when you use jQuery.

##### field(e.model): object
The model data. Available only if Knockout is used.

##### field(e.items): Array<Object>
Items to be displayed in the context menu. Their structure is described in the [Default Item Template](/api-reference/10%20UI%20Widgets/dxContextMenu/5%20Default%20Item%20Template '/Documentation/ApiReference/UI_Widgets/dxContextMenu/Default_Item_Template/') section.

##### field(e.area): string
The clicked [area's](/api-reference/30%20Data%20Layer/PivotGridDataSource/1%20Configuration/fields/area.md '/Documentation/ApiReference/Data_Layer/PivotGridDataSource/Configuration/fields/#area') type.

##### field(e.field): PivotGridDataSourceOptions_fields
The [configuration](/api-reference/30%20Data%20Layer/PivotGridDataSource/1%20Configuration/fields '/Documentation/ApiReference/Data_Layer/PivotGridDataSource/Configuration/fields/') of the field on which the context menu is invoked.

##### field(e.jQueryEvent): jQuery.Event
The jQuery event that caused the handler execution. Deprecated in favor of the **event** field.

##### field(e.jQueryEvent).deprecated
Use 'event' instead.

##### field(e.event): event
The event that caused the handler execution. It is a [dxEvent](/api-reference/50%20Common/Object%20Structures/dxEvent '/Documentation/ApiReference/Common/Object_Structures/dxEvent/') or a [jQuery.Event](https://api.jquery.com/Types/#Event) when you use jQuery.

---
Instead, you can use the [onContextMenuPreparing](/api-reference/10%20UI%20Widgets/dxPivotGridFieldChooser/1%20Configuration/onContextMenuPreparing.md '/Documentation/ApiReference/UI_Widgets/dxPivotGridFieldChooser/Configuration/#onContextMenuPreparing') option to handle the event.

Handle this event to change the set of items in the context menu before it is displayed.

#####See Also#####
#include common-link-handleevents