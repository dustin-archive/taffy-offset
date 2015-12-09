Taffy Offsets
=============

### Offsets for a sweet responsive grid.

## Overview
Offsets use margins to create space on either side of a Taffy item. Because margins can't flex, offsets won't occupy the same amount of space as an item unless you're using a fixed Taffy grid.

## Offsets
Offsets are attached to items and occupy space normally occupied by items.

```html
<div class='grid'>
  <div class='item.offset'></div>
  <!-- break -->
  <div class='item.offset'></div>
</div>
```

You make an offset the same way you'd make a Taffy item but with `offset-left` and `offset-right` mixins.

```scss
.offset {
  @include offset-left(2 '6:4');
  @include offset-right(2 '6:4');
}
```

## Custom offsets
If you want to use more or less than 12 offsets in a separate instance, use the `taffy-offset-generator` mixin.

```scss
@include taffy-offset-generator($name, $amount);
```

To use a custom offset pass your custom offset name to the offset mixin as the second argument.

```scss
@include offset-left(6 '6:4', 'custom-name');
@include offset-right(6 '6:4', 'custom-name');
```
