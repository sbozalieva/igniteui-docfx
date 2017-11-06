---
title: List View Component 
_description: Using any template, display data within rows seamlessly and intuitively through a native Angular framework with Ignite UI for Angular List View component.
_keywords: Ignite UI for Angular, UI controls, Angular widgets, web widgets, UI widgets, Angular, Native Angular Components Suite, Native Angular Controls, Native Angular Components Library, Angular List View components, Angular List View controls
---

##List View
_Igx-List represents a list of identical items._

###Usage
```html
<igx-list>
    <igx-list-header>Header 1</igx-list-header>
    <igx-list-item>Item 1</igx-list-item>
    <igx-list-item>Item 2</igx-list-item>
    <igx-list-item>Item 3</igx-list-item>
    <igx-list-header>Header 2</igx-list-header>
    <igx-list-item>Item 4</igx-list-item>
    <igx-list-item>Item 5</igx-list-item>
    <igx-list-item>Item 6</igx-list-item>
</igx-list>
```

The children components of the IgxList are:

- *Igx-List-Header* - represents list header - non-interactable list item which role is to label, describe and unify the next list items, composed below it
- *Igx-List-Item* - represents list item

Both: item and header, implement `IListChild`.  
The list provides three arrays: 

- one that contains all the children: items and headers,
- only items,
- only headers.

#### List Properties
- `children` - Array of all `IListChild` components: items and headers
- `items` - Array of items in the list
- `headers` - Array of headers in the list
- `allowLeftPanning` - Determines whether the left panning of an item is allowed
- `allowRightPanning` - Determines whether the right panning on an item is allowed

#### Methods
- `addChild` - Add `IListChild` component to children array and to the respective specific array
- `removeChild` - Remove `IListChild` component from children array and from the respective specific array

#### Events
- `onPanStateChange` - Triggered when pan gesture is executed on list item
- `onLeftPan` - Triggered when left pan gesture is executed on list item
- `onRightPan` - Triggered when right pan gesture is executed on list item

###List Header
_Child component of Igx-List, that represents a single non-interactable item, that is used as a header of the following items. The header implements `IListChild` interface._

#### Header Properties
- `index` - The index of header in children array

###List Item
_Child component of Igx-List, that represents a single interactable item. Its content can be text or any other HTML content. The item implements `IListChild` interface._

#### Item Properties
- `index` - The index of item in children array
- `hidden` - Determines whether the item should be displayed
- `panState` - Gets the items pan state
- `options` - Defines the options of particular list item, that will be displayed on item swipe (pan)