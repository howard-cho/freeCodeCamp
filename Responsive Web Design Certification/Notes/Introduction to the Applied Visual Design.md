Visual Design in web development combines typography, color theory, graphics, animation, and page layout to help deliver a site's message.

# Create Visual Balance Using the text-align Property

text-align: justify; /_ causes all lines of the text except the last line to meet the left and right edges of the line box.
text-align: center; /_ centers the text _/
text-align: right; /_ right-aligns the text _/
text-align: left; /_ (default) left-aligns the text \*/

# Adjust the Width of an Element Using the width Property

width can be specified in relative length units (such as em), absolute length units (such as px), or as a percentage of its containing parent element.

<style>
  img {
    width: 220px;
  }
</style>

# Adjust the Height of an Element Using the height Property

Similar to the width property, using relative, absolute, and percentage units.

<style>
  img {
    height: 20px;
  }
</style>

# Use the strong Tag to Make Text Bold

This is often used to draw attention to text and symbolize that it is important.
With the <strong></strong> tag, the browser applies the CSS of font-weight: bold; to the element.
<strong>Stanford University</strong>

# Use the u Tag to Underline Text

This is often used to signify that a section of text is important, or something to remember.
With the <u> tag, the browser applies the CSS of text-decoration: underline; to the element.
<u>Ph.D. students</u>

Try to avoid using the <u> tag when it could be confused for a link. Anchor tags also have a default underlined formatting.

# Use the em Tag to Italicize Text

To emphasize text. This displays text as italicized.
The browser applies the CSS of font-style: italic; to the element.

# Use the s Tag to Strikethrough Text

When a horizontal line cuts across the characters. It shows that a section of text is no longer valid.
With the <s></s> tag, the browser applies the CSS of text-decoration: line-through; to the element.

# Create a Horizontal Line Using the hr Element

Use the <hr> tag to add a horizontal line across the width of its containing element.
This can be used to define a change in topic or to visually separate groups of content.

<hr> is a self-closing tag.

# Adjust the background-color Property of Text

rgba stands for:
r = red
g = green
b = blue
a = alpha/level of opacity - range from 1 (solid color/fully opaque) to 0 (fully transparent)

background-color: rgba(45, 45, 45, 0.1)

# Adjust the Size of a Header Versus a Paragraph Tag

The font size of header tags (h1 through h6) should generaelly be larger than the font size of paragraph tags.
Use the font-size property to adjust the size of the text in an element.

# Add a box-shadow to a Card-like Element

box-shadow property applies one or more shadows to an element.

The box-shadow property takes values for:
offset-x (how far to push the shadow horizontally from the element)
offset-y (how far to push the shadow vertically from the element)
blur-radius (optional)
spread-radius (optional)
color value

box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);

# Decrease the Opacity of an Element

The opacity property in CSS is used to adjust the opacity (transparency) for an item.

A value of 1 is opaque, which isn't transparent at all.
A value of 0.5 is half see-through.
A value of 0 is completely transparent.

# Use the text-transform Property to Make Text Uppercase

The text-transform property in CSS is used to change the appearance of text. It's a convenient way to make sure text on a webpage appears consistently, without having the change the text content of the actual HTML elements.

text-transform values:

Value Result
lowercase "transform me"
uppercase "TRANSFORM ME"
capitalize "Transform Me"
initial Use the default value
inherit Use the text-transform value from the parent element
none Default: Use the original text

# Set the font-size for Multiple Heading Elements

# Set the font-weight for Multiple Heading Elements

font-weight property sets how thick or thin characters are in a section of text.

# Set the line-height of Paragraphs

line-height property changes the height of each line in a block of text. It changes the amount of vertical space that each line of text gets.

# Adjust the Hover State of an Anchor Tag

A psuedo-class is a keyword that can be added to selectors, in order to select a specific state of the element.

The styling of an anchor tag can be changed for its hover state using the :hover pseudo-class selector.

<style>
  a:hover {
    color: red;
  }
</style>

# Change an Element's Relative Position

CSS Box Model - CSS treats each HTML element as its own box.

Block-level items automatically start on a new line (headings, paragraphs, divs).
Inline items sit within surrounding content (images or spans).

Normal flow of a document - the default layout of elements.

CSS offers the position property to override it.

position: relative; /_ allows you to specify how CSS should move it relative to its current position in the normal flow of the page. _/
Pair with the CSS offset properties of left or right, and top or bottom.

Specify how many pixels, percentages, or ems to move the item AWAY from where it is normally positioned.

/_ Move the paragraph 10 pixels <u>away</u> from the bottom _/
p {
position: relative;
bottom: 10px;
}

Changing the element's position to relative does not remove it from the normal flow.
Other elements around it still behave as if that item were in its default position.

# Move a Relatively Positioned Element with CSS Offsets

The CSS offsets of top or bottom, left or right tell the browser how far to offset an item relative to where it would sit in the normal flow of the document.
You're offsetting an element away from a given spot, which moves the element away from the referenced side (the opposite direction as the CSS).

# Lock an Element to its Parent with Absolute Positioning

position: absolute;
Locks the element in place relative to its parent container.
This removes the element from the normal flow of the document, so surrounding items ignore it.
The CSS offset properties (top/bottom, left/right) are used to adjust the position.

It will be locked to the closest positioned ancestor.
If you forget to add a position rule to the parent item, (typically using position: relative;), the browser will keep looking up the chain and ultimately default to the body tag.

/_ Lock the #searchbar element to the top-right of its section parent by declaring its position as absolute. Give it top and right offsets of 50 pixels each. _/

<style>
  #searchbar {
    position: absolute;
    top: 50px;
    right: 50px;
  }
</style>

# Lock an Element to the Browser Window with Fixed Positioning

position: fixed;

Type of Absolute positioning that locks an element relative to the browser window.
Removes the element from the normal flow of the document.
Other items no longer "realize" where it is positioned.

Key difference between the fixed and absolute positions is that an element with a fixed position won't move when the user scrolls.
position: fixed; /_ won't move when scrolled _/

Position to fixed, and offset it 0 pixels from the top and 0 pixels from the left.

<style>
  #navbar {
    position: fixed;
    top: 0px;
    left: 0px;
    
    width: 100%;
    background-color: #767676;
  }
</style>

# Push Elements Left or Right with the float Property

Floating elements are removed from the normal flow of the document and pushed to either the left or right of their containing parent element.
Commonly used with the width property to specify how much horizontal space the floated element requires.

<style>
  #left {
    float: left;
    width: 50%;
  }
  #right {
    float: right;
    width: 40%;
  }
</style>

# Change the Position of the Overlapping Elements with the z-index Property

When elements are positioned to overlap, the element coming later in the HTML markup will, by default, appear on the top of the other elements.

z-index property can specify the order of how elements are stacked on top of one another.
z-index must be an integer.
Higher values for the z-index property of an element move it higher in the stack than those with lower values.

z-index: 2; /_ 2 is on top of 1 _/
z-index: 1;

# Center an Element Horizontally Using the Margin Property

Center a block element horizontally by setting margin: auto;
Images are inline elements by default, but can be changed to block elements when you set the display property to block.

# Learn about Complementary Colors

When two colors are opposite each other on the wheel, they are called complementary colors.
They have the characteristic that if they are combined, they "cancel" each other out and create a gray color.
When placed side by side, these colors appear more vibrant and produce a strong visual contrast.

Examples:
red (#FF0000) cyan (#00FFFF)
green (#00FF00) magenta (#FF00FF)
blue (#0000FF) yellow (#FFFF00)

Modern color theory uses the additive RGB model (computer screen) and the subtractive CMY(K) model (in printing).

# Learn about Tertiary Colors

Tertiary colors are the result of combining a primary color with one of its secondary color neighbors.
Split-complementary color scheme - start with a base color, then pair it with the two colors that are adjacent to its complement.
The three colors provide strong visual contrast in a design, but are more subtle than using two complementary colors.

orange #FF7D00
cyan #00FFFF
raspberry #FF007D

# Adjust the Hue of a Color

CSS3 introduced the hsl() (hue, saturation, lightness) property as an alternative way to pick a color by directly stating hue, saturation, and lightness.

Hue is color - a value between 0 and 360.
Saturation - the amount of gray in a color. A percentage with 100% being fully saturated. Fully saturated has no gray in it. Minimally saturated is almost completely gray.
Lightness - the amount of white or black in a color. 0% (black) 100% (white), 50% is normal color.

red hsl(0, 100%, 50%)
yellow hsl(60, 100%, 50%)
green hsl(120, 100%, 50%)
cyan hsl(180, 100%, 50%)
blue hsl(240, 100%, 50%)
magenta hsl(300, 100%, 50%)

# Adjust the Tone of a Color

Mixing white with a pure hue creates a tint of that color.
Adding black will make a shade.

<style>
  header {
    background-color: hsl(180, 90%, 35%);
    color: #FFFFFF;
  }
  
  nav {
    background-color: hsl(180, 80%, 25%);
  }
</style>

# Create a Gradual CSS Linear Gradient

CSS provides the ability to use color transitions (gradients) on elements.

Syntax:
background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);

gradient_direction specifies the direction from which color transition starts - stated as a degree.
90deg - vertical gradient
45deg - angled like a backslash.

<style>
  div{ 
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin: 50px auto;
    background: linear-gradient(35deg, #CCFFFF, #FFCCCC);
  }
</style>

# Use a CSS Linear Gradient to Create a Striped Element

background: repeating-linear-gradient(); repeats the specified gradient pattern.
Angle pattern (90deg for vertical), with color stop values.

https://learn.freecodecamp.org/responsive-web-design/applied-visual-design/use-a-css-linear-gradient-to-create-a-striped-element

If every two color stop values are the same color, the blending isn't noticeable because it's between the same color, followed by a hard transition to the next color, so you end up with stripes.

<style>
  div{ 
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin:  50 auto;
    background: repeating-linear-gradient(
      45deg,
      yellow 0px,
      yellow 40px,
      black 40px,
      black 80px
    );
  }
</style>

# Create Texture by Adding a Subtle Pattern as a Background Image

The background property supports the url() function to link to an image of the chosen texture or pattern.

<style>
  body {
    background: url(https://i.imgur.com/MJAkxbh.png);
  }
</style>

# Use the CSS Transform scale Property to Change the Size of an Element

transform: scale() changes the scale of an element.

<style>
  p {
    transform: scale(2); /* double the size */
  }
</style>

Add interactivity to your elements using the transform property with on hover

<style>
  p:hover {
    transform: scale(2.1);
  }
</style>

# Use the CSS Transform Property skewX and skewY to Skew an Element Along the X-Axis and Y-Axis.

transform: skewX(); skews the element along its X (horizontal) axis by a given degree.
transform: skewY(); skews the element along its Y (vertical) axis by a given degree.

<style>
  p {
    transform: skewX(-32deg);
  }
  h1 {
    transform: skewY(-10deg);
  }
</style>

# Create a Graphic Using CSS

box-shadow property sets the shadow of an element.
border-radius property controls the roundness of the element's borders.

https://learn.freecodecamp.org/responsive-web-design/applied-visual-design/create-a-graphic-using-css

<style>
.center
{
  position: absolute;
  margin: auto;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  width: 100px;
  height: 100px;
  
  background-color: rgba(0,0,255,0);
  border-radius: 50%;
  box-shadow: 25px 10px 0 0 blue; 
}

</style>
<div class="center"></div>

# Create a More Complex Shape Using CSS and HTML

Create a heart symbol using pure CSS:
https://learn.freecodecamp.org/responsive-web-design/applied-visual-design/create-a-more-complex-shape-using-css-and-html

<style>
.heart {
  position: absolute;
  margin: auto;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background-color: pink;
  height: 50px;
  width: 50px;
  transform: rotate(-45deg);
}
.heart::after {
  background-color: pink;
  content: "";
  border-radius: 50%;
  position: absolute;
  width: 50px;
  height: 50px;
  top: 0px;
  left: 25px;
}
.heart::before {
  content: "";
  background-color: pink;
  border-radius: 50%;
  position: absolute;
  width: 50px;
  height: 50px;
  top: -25px;
  left: 0px;
}
</style>
<div class = "heart"></div>
