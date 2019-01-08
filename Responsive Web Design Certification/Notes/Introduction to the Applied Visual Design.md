Visual Design in web development combines typography, color theory, graphics, animation, and page layout to help deliver a site's message.

# Create Visual Balance Using the text-align Property

text-align: justify; /* causes all lines of the text except the last line to meet the left and right edges of the line box.
text-align: center; /* centers the text */
text-align: right; /* right-aligns the text */
text-align: left; /* (default) left-aligns the text */

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
With the <strong> tag, the browser applies the CSS of font-weight: bold; to the element.
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







