# Element `class`

## Props

| Prop | Type | Requried | Description |
| --- | --- | --- | --- |
| type | `string` | `false` |  |
| id | `string, number` | `false` |  |
| tag | `string` | `false` |  |
| name | `string` | `false` |  |
| href | `string` | `false` |  |
| linkTarget | `string` | `false` |  |
| attrs | `string` | `false` |  |
| classes | `string` | `false` |  |
| variant | `string` | `false` |  |
| preset | `string, number` | `false` |  |
| psuedo | `string` | `false` |  |
| psuedoState | `string` | `false` |  |
| data | `object` | `false` |  |
| binding | `object` | `false` |  |
| state | `string` | `false` |  |
| script | `string` | `false` |  |
| unique | `bool` | `false` |  |
| locked | `bool` | `false` |  |
| editable | `bool` | `false` |  |
| dynamic | `bool` | `false` |  |
| useLayout | `number` | `false` |  |
| dynamicItem | `number` | `false` |  |``
| hidden | `bool` | `false` |  |
| url | `string` | `false` |  |
| hideOnLarge | `bool` | `false` |  |
| hideOnLaptop | `bool` | `false` |  |
| hideOnTablet | `bool` | `false` |  |
| hideOnMobile | `bool` | `false` |  |
| gaEvent | `string` | `false` |  |
| pxEvent | `string` | `false` |  |
| pxCode | `string` | `false` |  |
| animation | `string` | `false` |  |
| animationHover | `string` | `false` |  |
| pro | `bool` | `false` |  |
| elType | `string` | `false` |  |
| model | `any` | `false` |  |
| collection | `any` | `false` |  |



## contextTypes (  ) `static`


## contextTypes ( types ) `static`

| Param | Type | Description |
| --- | --- | --- |
| types | `null` |  |


## childContextTypes (  ) `static`


## childContextTypes ( types ) `static`

| Param | Type | Description |
| --- | --- | --- |
| types | `null` |  |


## propTypes (  ) `static`


## propTypes ( types ) `static`

| Param | Type | Description |
| --- | --- | --- |
| types | `null` |  |


## defaultProps (  ) `static`


## defaultProps ( props ) `static`

| Param | Type | Description |
| --- | --- | --- |
| props | `null` |  |


## updateComputedStyle (  ) 


## set ( path | value ) 

get /set methods provide a simple interface for
exchanging data with other libraries. Our UI Controls
will look for the get / set function and use it first

| Param | Type | Description |
| --- | --- | --- |
| path | `undefined` |  |
| value | `undefined` |  |


## stateHandler (  ) 


## style (  ) 


## styleHandler (  ) 


## hasher (  ) 


## computedStyle (  ) 


## inspector (  ) 


## inspector ( input ) 

| Param | Type | Description |
| --- | --- | --- |
| input | `null` |  |


## key (  ) 


## page (  ) 


## editor (  ) 


## parent (  ) 


## section (  ) 


## document (  ) 


## window (  ) 


## path (  ) 


## data (  ) 


## dataJSON (  ) 


## templateJSON (  ) 

Return a nested data with its children mapped with actual data
Normally, element children state only store an array of IDs
The real data is stored on the items state of page


## label (  ) 

Label for showing on top left corner of element when mouse over


## pathLabel (  ) 

Label for showing in path view in header of inspectors


## index (  ) 

Return the index of this element in which parent it was rendered in


## mode (  ) 

Return current page's render mode => 'edit' or 'view'


## id (  ) 

Return the unique id generated for this element instance


## type (  ) 

Return this element type


## name (  ) 

Return this element name


## hash (  ) 

Computed unique hash key for every element based on
--- Element type + Page ID + Element ID


## selectorName (  ) 

Return a generated hash based on element's type and page's id
This hash only need to be generated once when the first instance initialised


## selectorClassNames (  ) 

A list of class names associated with this element

1) A hash encrypted from type and page key
2) A hash encrypted from type, page key, and element key
3) A hash for variant which this element inherited its style from


## selector (  ) 

It's very important to keep this function SIMPLE and STRAGHT FOWARD
it should return an unique CSS selector depends on where it's rendered

The structures are:
1) ._GAyI7J                  <-- Block
2) ._GAyI7J__title           <-- Element in a block
3) ._PKxInD ._PKxInD         <-- Item in a collection block


## selectorLegacy (  ) 


## formattedName (  ) 


## locked (  ) 

Get the current locked state


## flow (  ) 

Get the flow direction used for sorting elements


## boundingBoxNode (  ) 


## boundingBox (  ) 


## updateCachedBounds (  ) 


## OldboundingBox (  ) 


## isEmpty (  ) 


## placeholder (  ) 


## isNested (  ) 


## isProElement (  ) 


## visibility (  ) 


## dataModel (  ) 


## prepareData (  ) 

Parent element will invoke this function on all of its children
before proceeding with its data extracting procedure. This ensure
all child element get a chance to populate its latest data where needed.
---
In this very specific case, all nested element need to update its styles
in the parent state. This apply for bound element with "bind" prop only.


## _parseProps ( props ) 

Take only the properties defined in static getProptypes

| Param | Type | Description |
| --- | --- | --- |
| props | `undefined` |  |


## getStyleSelector ( psuedo | state | psuedoState ) 

| Param | Type | Description |
| --- | --- | --- |
| psuedo | `null` |  |
| state | `null` |  |
| psuedoState | `null` |  |


## customHash ( pageKey | elKey | elType ) 

custom hash used for preset

| Param | Type | Description |
| --- | --- | --- |
| pageKey | `mixed` |  |
| elKey | `mixed` | => key of preset |
| elType | `mixed` | => type of preset |


## findAll (  ) 

Find all deeply nested child components


## extractStyles (  ) 

Extract all style rules belong to this element and render as CSS text


## applyStyles ( styles ) 

Apply element styles passed as props to page stylesheets

| Param | Type | Description |
| --- | --- | --- |
| styles | `null` |  |


## css ( prop ) 

Return the computed style of this element's DOMNode

| Param | Type | Description |
| --- | --- | --- |
| prop | `null` |  |


## isChildOf ( parent ) 

Check if this element is child of given element

| Param | Type | Description |
| --- | --- | --- |
| parent | `null` |  |


## isChildOfParentType ( type ) 

| Param | Type | Description |
| --- | --- | --- |
| type | `null` |  |


## forceUpdateAll ( callback ) 

| Param | Type | Description |
| --- | --- | --- |
| callback | `null` |  |


## copy (  ) 


## setStyle ( nextStyle | psuedo ) 

| Param | Type | Description |
| --- | --- | --- |
| nextStyle | `null` |  |
| psuedo | `null` |  |


## getStyle ( psuedo ) 

| Param | Type | Description |
| --- | --- | --- |
| psuedo | `null` |  |


## saveState ( state | cb ) 

| Param | Type | Description |
| --- | --- | --- |
| state | `null` |  |
| cb | `null` |  |


## getCopiedElLayout (  ) 

ThanhCH Oct 2 2017
Core COPY/PASTE styles feature is implemented here
How it works:
When copy styles, we also copy the data structure of that given element
so that we can check if the destination el has the same layout with the original el =>  can paste style
NOTE:
copied data is stored in {localStorage}
saved layout and saved styles are actually arrays, because constructing function of layout and styles are consistent
so the order is certainly unchanged => The styles will be applied respectively well with that order
that's why we need to check the layout


## constructLayout ( layout | el ) 

| Param | Type | Description |
| --- | --- | --- |
| layout | `null` |  |
| el | `null` |  |


## getAllStyles (  ) 


## constructStyles ( styles | el ) 

| Param | Type | Description |
| --- | --- | --- |
| styles | `null` |  |
| el | `null` |  |


## copyStyles (  ) 


## canPasteStyle (  ) 


## pasteStyles (  ) 


## applyClipboardStyle ( styles | el ) 

| Param | Type | Description |
| --- | --- | --- |
| styles | `null` |  |
| el | `null` |  |


## focus (  ) 

====== end COPY/PASTE implementation ====


## select (  ) 


## triggerAction ( action | ...args ) 

| Param | Type | Description |
| --- | --- | --- |
| action | `null` |  |
| ...args | `null` |  |


## handleMouseDown ( e ) 

| Param | Type | Description |
| --- | --- | --- |
| e | `null` |  |


## handleMouseEnter ( e ) 

| Param | Type | Description |
| --- | --- | --- |
| e | `null` |  |


## handleMouseOver ( e ) 

| Param | Type | Description |
| --- | --- | --- |
| e | `null` |  |


## handleMouseOut ( e ) 

| Param | Type | Description |
| --- | --- | --- |
| e | `null` |  |


## handleMouseLeave ( e ) 

| Param | Type | Description |
| --- | --- | --- |
| e | `null` |  |


## handleDrag ( e ) 

| Param | Type | Description |
| --- | --- | --- |
| e | `null` |  |


## handleDragEnd ( e ) 

| Param | Type | Description |
| --- | --- | --- |
| e | `null` |  |


## handleDragStart ( e ) 

| Param | Type | Description |
| --- | --- | --- |
| e | `null` |  |


## handleDragEnter ( e ) 

| Param | Type | Description |
| --- | --- | --- |
| e | `null` |  |


## handleDragOver ( e ) 

| Param | Type | Description |
| --- | --- | --- |
| e | `null` |  |


## handleDragLeave ( e ) 

| Param | Type | Description |
| --- | --- | --- |
| e | `null` |  |


## moveItem ( child ) 

| Param | Type | Description |
| --- | --- | --- |
| child | `null` |  |


## handleDrop ( e ) 

| Param | Type | Description |
| --- | --- | --- |
| e | `null` |  |


## enhanceTemplateJSON ( templateJSON | parentType | isMoved ) 

| Param | Type | Description |
| --- | --- | --- |
| templateJSON | `null` |  |
| parentType | `null` |  |
| isMoved | `null` |  |


## showPlaceHolder ( edge | bounds ) 

| Param | Type | Description |
| --- | --- | --- |
| edge | `null` |  |
| bounds | `null` |  |


## hidePlaceHolder (  ) 


## enhance ( element ) 

| Param | Type | Description |
| --- | --- | --- |
| element | `null` |  |


## remove (  ) 

DEPRECATED FUNCTIONS !!
This is left for fallback support our previous elements
DO NOT use these in new codes


## _duplicate (  ) 

