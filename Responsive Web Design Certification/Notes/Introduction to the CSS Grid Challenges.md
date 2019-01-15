CSS grid turns HTML elements into a grid container with rows and columns to place children elements in the grid.

# Turn any HTML element into a grid container

`display: grid;`

In CSS Grid, the parent element is referred to as the <em>container</em> and its children are called <em>items</em>.

# Add Columns with grid-template-columns

Use `grid-template-columns` property to add some columns to the grid.

<style>
  .container {
      display: grid;
      grid-template-columns: 50px 50px; /* Creates two columns that are 50px wide each. */
  }
</style>

The number of parameters given to the `grid-template-columns` property indicates the number of columns in the grid.
The value of each parameter indicates the width of each column.
The number of rows are adjusted automatically.

# Add Rows with grid-template-rows

To adjust the number of rows manually, use the `grid-template-rows` property.

`grid-template-columns: 50px 50px;` two rows 50px each.

# Use CSS Grid units to Change the Size of Columns and Rows

CSS grid size can be defined with absolute or relative units like `px` and `em`.

The following are also supported:

`fr`: sets the column or row to a fraction of the available space.
`auto`: sets the column or row to the width or height of its content automatically.
`%`: adjusts the column or row to the percent width of its container.

`grid-template-columns: auto 50px 10% 2fr 1fr;`

# Create a Column Gap Using grid-column-gap

Sometimes you want a gap in between the columns.
`grid-column-gap` creates a gap between columns.

`grid-column-gap: 10px;` - creates 10px of empty space between all of your columns.

# Create a Row Gap using grid-row-gap

`grid-row-gap` creates a gap between rows.

# Add Gaps Faster with grid-gap

`grid-gap` is a shorthand property for `grid-row-gap` and `grid-column-gap`.

If `grid-gap` has one value, it creates a gap between all rows and columns.
If `grid-gap` has two values, first - rows, second - columns.

`grid-gap: 10px 20px;`

# Use grid-column to Control Spacing

`grid-column` property controls the amount of columns an item will consume.

The hypothetical horizontal and vertical lines that create the grid are referred to as <em>lines</em>.

.1......2......3......4
1|------|------|------|
.|......|......|......|
2|------|------|------|
.|......|......|......|
3|------|------|------|
.|......|......|......|
4|------|------|------|

`grid-column: 1 / 3;` will make the item start at the first vertical line of the grid on the left and span to the 3rd line of the grid, consuming two columns.

# Use grid-row to Control Spacing

`grid-row` property controls the amount of rows an item will consume.

`grid-row: 1 /3;` will make the item start at the first horizontal line of the grid on the top and span to the 3rd line of the grid, consuming two rows.

# Align an Item Horizontally using justify-self

In CSS Grid, the content of each item is located in a box which is referred to as a cell.
You can align the content's position within its cell horizontally using `justify-self` on a grid item.

`justify-self: start;` aligns the content at the left of the cell.
`justify-self: center;` aligns the content in the center of the cell.
`justify-self: end;` aligns the content at the right of the cell.

# Align an Item Vertically using align-self

`align-self` property aligns an item vertically. Same values as `justify-self`

`align-self: start;` aligns the content at the top of the cell.
`align-self: center;` aligns the content in the center of the cell.
`align-self: end;` aligns the content at the bottom of the cell.

# Align All Items Horizontally using justify-items

`justify-items` property will move <strong>all</strong> the items in your grid to the desired element.

`justify-items: start;` aligns every item of the grid container at the left of the cell.
`justify-items: center;` aligns every item of the grid container in the center of the cell.
`justify-items: end;` aligns every item of the grid container at the right of the cell.

# Align All Items Vertically using align-items

`align-items` property on a grid container will set the vertical alignment for all the items in our grid.

# Divide the Grid Into an Area Template

You can group cells of your grid together into an <em>area</em> and give the area a custom name.

Merge top three cells together into an area named `header`
Merge bottom three cells together into an area named `footer`
Two areas in the middle row `advert` and `content`

`grid-template-areas: "header header header" "advert content content" "footer footer footer";`

Every word in the code represents a cell.
Every pair of quotation marks represent a row.

You can use a period ( `.` ) to designate an empty cell in the grid.

# Place Items in Grid Areas Using the grid-area Property

After creating an areas template for your grid container, you can place an item in your custom area by referencing the name you gave it.

`item1` class will go in the area named `header`.

<style>
  .item1 {
      grid-area: header;
  }
</style>

# Use grid-area Without Creating an Areas Template
