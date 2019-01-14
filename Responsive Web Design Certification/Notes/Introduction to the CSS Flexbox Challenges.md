A website's User Interface (UI) has two components.

- The visual elements, such as colors, fonts, and images.
- Placement or positioning of those elements.

In Responsive Web Design, a UI layout must accommodate many different browsers and devices accessing the content.

CSS 3 introduced Flexible Boxes (flexbox), to create page layouts for a dynamic UI.
Flexbox is a layout mode that arranges elements in a predictable way for different screen sizes and browsers.

# Use display: flex to Position Two Boxes

Placing the CSS property `display: flex;` on an element allows you to use other flex properties to build a responsive page.

# Use the flex-direction Property to Make a Row

Adding `display: flex;` to an element turns it into a flex container.
This makes it possible to align any children of that element into rows or columns.

`flex-direction` is used on the parent item and setting it to row or column.
Creating a row will align the children horizontally.
Creating a column will align the children vertically.

Other options for `flex-direction` are row-reverse and column-reverse.

The default property for the `flex-direction` property is row.

<style>
  #box-container {
    display: flex;
    height: 500px;
    flex-direction: row-reverse;
  }
</style>

# Use the flex-direction Property to Make a Column

`flex-direction: column` vertically stacks the children of a flex container.

# Align Elements Using the justify-content Property

The direction of the flex items that are arranged is called the <strong>main axis</strong>.
For a row, this is a horizontal line that cuts through each item.
For a column, this is a vertical line that cuts through each item.

https://www.w3.org/TR/css-flexbox-1/images/flex-direction-terms.svg

`justify-content: center;` aligns all the flex items to the center inside the flex container.

`justify-content: flex-start` aligns items to the start of the flex container. Row pushes to the left, column pushes to the top.

`justify-content: flex-end` aligns items to the end of the flex container. Row pushes to the right, column pushes to the bottom.

`justify-content: space-between` aligns items to the center of the main axis, with extra space placed between the items.

- The first and last items are pushed to the very edge of the flex container.
- For a row the first item is against the left, the last item is against the right. THe other items in between are spaced evenly.

`justify-content: space-around` similar to `space-between` but the first and last items are not locked to the edges of the container.

- The space is distributed around all the items.

# Align Elements Using the align-items Property

Flex containers can also have a `cross axis`, which is the opposite of the main axis.
For rows, cross axis is vertical.
For columns, cross axis is horizontal.

`align-items` property aligns flex items along the cross axis.
For a row, push the items in the row up or down.
For a column, push all the items in the row left or right.

`align-items: flex-start;` aligns items to the start of the flex container.

- For rows, aligns to the top of the container
- For columns, aligns to the left of the container

`align-items: flex-end;` aligns items to the end of the flex container.

- For rows, aligns to the bottom of the container
- For columns, aligns to the right of the container

`align-items: center;` align items to the center.

- For rows, vertically align items (equal space above and below the items)
- For columns, horizontally aligns items (equal space to the left and right of the items)

`align-items: stretch;' stretch the items to fill the flex container.

- Row items are stretched to fill the flex container top-to-bottom

`align-items: baseline;` align items to their baselines. Baseline is a text concept - the line that the letters sit on.

# Use the flex-wrap Property to Wrap a Row or Column

CSS flexbox has a feature to split a flex item into multiple rows (or columns).
By default, a flex container will fit all flex items together.
A row will all be on one line.

`flex-wrap` property tells CSS to wrap items.
Extra items move into a new row or column.
The break point of where the wrapping happens depends on the size of the items and the size of the container.

`flex-wrap: nowrap;` the default setting, does not wrap items
`flex-wrap: wrap;` wraps items from left-to-right if they are in a row, or top-to-bottom if they are in a column
`flex-wrap: wrap-reverse;` wraps items from bottom-to-top if they are in a row, or right-to-left if they are in a column

# Use the flex-shrink Property to Shrink Items

`flex-shrink` applies to the flexbox items (not the flex container)

`flex-shrink` allows an item to shrink if the flex container is too small.
Items shrink when the width of the parent container is smaller than the combined widths of all the flex items within it.

`flex-shrink` takes numbers are values. The higher the number, the more it will shrink compared to the other items in the container.
`flex-shrink: 3;` will shrink three times as much as `flex-shrink: 1;`

# Use the flex-grow Property to Expand Items

`flex-grow` is the opposite of the `flex-shrink` property.
`flex-grow` property controls the size of the items when the container expands.

`flex-grow: 3;` will grow three times as much as the `flex-grow: 1;`

# Use the flex-basis Property to Set the Initial Size of an Item

`flex-basis` property specifies the initial size of the item before CSS makes adjustments with `flex-shrink` or `flex-grow`

`flex-basis` property units are the same as other size properties (px, em, %, etc).
`flex-basis: auto;` sizes items based on the content.

# Use the flex Shorthand Property

`flex` property can set `flex-grow`, `flex-shrink`, and `flex-basis` together.

`flex: 1 0 10px;` will set the item to `flex-grow: 1;`, `flex-shrink: 0;`, and `flex-basis: 10px;`

Default is `flex: 0 1 auto;`

These values will cause #box-1 to grow to fill the extra space at twice the rate of #box-2 when the container is greater than 300px and shrink at twice the rate of #box-2 when the container is less than 300px. 300px is the combined size of the flex-basis values of the two boxes.

<style>
  #box-container {
    display: flex;
    height: 500px;
  }
  #box-1 {
    background-color: dodgerblue;
    flex: 2 2 150px;
    height: 200px;
  }

  #box-2 {
    background-color: orangered;
    flex: 1 1 150px;
    height: 200px;
  }
</style>

# Use the order Property to Rearrange Items

`order` property is used to tell the order of how flex items appear in the flex container.
By default, items will appear in the same order they come in the source HTML.
`order` takes numbers are values, negative numbers can be used.

`order: 1;` comes before `order: 2;`

# Use the align-self Property

`align-self` property adjusts each item's alignment individually, instead of setting them all at once.
This is useful since other common adjustment techniques using `float`, `clear`, and `vertical-align do not work on flex items.

`align-self` accepts the same values as `align-items` and will override any value set by the `align-values` property.
