---
title: Partial render file
docTags: 
createdAt: Wed May 13 2026 12:03:51 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed May 13 2026 12:03:51 GMT+0000 (Coordinated Universal Time)
---

## Directive that you can use

`partial` or `use`

```javascript
::use{file="/.archbee.yaml" from="1" to="5" syntax="javascript"}
```

## Render petstore from line 9 to 12

::Partial[]{file="../petstore-2.0.yaml" from="9" to="12"}

## Render .archbee.yaml

::Partial[]{file="/.archbee.yaml" from="1" to="5" syntax="javascript"}

## Render file hints.md line 1

### Line 5 only

::Partial[]{file="hints.md" from="5"}

### From line 1 to line 5 with lang javascript

::Partial[]{file="hints.md" from="5" to="10" syntax="javascript"}

## Print line 2 from .archbee.yaml

::Partial[]{file="/.archbee.yaml" from="3"}

## Errors and limitations

### Undefined range

::Partial[]{file="hints.md" from="5" to="10000"}

### Self referencing is not allowed

The output will not be rendered.

***

::Partial[]{from="5"}

***

### Rendering entire file .archbee.yaml is not allowed

::Partial[]{file="/.archbee.yaml" syntax="javascript"}
