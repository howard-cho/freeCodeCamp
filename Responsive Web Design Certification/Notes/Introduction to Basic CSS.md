Cascading Style Sheets (CSS) tell the browser how to display the text and other content that you write in HTML.

CSS is case-sensitive

CSS allows you to control:

- color
- fonts
- positioning
- spacing
- sizing
- decorations
- transitions

# Change the Color of Text

<h2 style="color: blue;">CatPhotoApp</h2> <!-- inline CSS -->

# Use CSS Selectors to Style Elements

Inside <head> block, create a <style> block

<style>
  h2 {color: red;}
</style>

# Use a CSS Class to Style an Element

Classes are reusable styles that can be added to HTML elements

<style>
  .blue-text {
    color: blue;
  }
</style>

Apply a class to an HTML element like this:

<h2 class="blue-text">CatPhotoApp</h2>

Classes allow you to use the same CSS styles on multiple HTML elements.

# Change the Font Size of an Element

h1 {
font-size: 30px;
}

# Change the Font Family of an Element

h2 {
font-family: sans-serif;
}

# Import a Google Font

Google Fonts Library: https://fonts.google.com/

Use link tag to import a font in the <head> element

<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">

font-family: FAMILY*NAME, GENERIC_NAME; /* Case-sensitive and must be wrapped in quotes if more than one word. \_/

# Specify How Fonts Should Degrade

Default fonts available in all browsers: monospace, serif, sans-serif.

When a font isn't available, you can tell the browser to "degrade" to another font.

p {
font-family: Helvetica, sans-serif;
}

# Size Your Images

<style>
  .larger-image {
    width: 500px;
  }
</style>

# Add Borders Around Your Elements

Red, 5 pixel border around an HTML element:

<style>
  .thin-red-border {
    border-color: red;
    border-width: 5px;
    border-style: solid;
  }
</style>

You can add multiple classes to an element by separating class names with a space

<img class="class1 class2">

# Add Rounded Corners with border-radius

<style>
  .thin-red-border {
    border-color: red;
    border-width: 5px;
    border-style: solid;
    /* border-radius: 10px; */
    border-radius: 50%;
  }
</style>

# Give a Background Color to a div Element

background-color property

<style>
  .green-background {
    background-color: green;
  }
</style>

# Set the id of an Element

In addition to classes, each HTML element can also have an id attribute.

You can use an id to style a single element and modify the element with JavaScript.

id attributes should be unique. However, browsers don't enforce it.

<h2 id="cat-photo-app">

# Use an id Attribute to Style an Element

id is not reusable and should only be applied to one element.

id has a higher specificity (importance) than a class - if both are applied to the same element with conflicting styles, the styles of the id will be applied.

<style>
  #cat-photo-element {
    background-color: green;
  }
</style>

classes - .classes
id - #id

# Adjust the Padding, Margin, Border of an Element

Three properties control the space that surrounds each HTML element:

- padding - controls the amount of space between the element's content and its border
  - 4 individual sides can be controlled
  - padding-top, padding-right, padding-bottom, padding-left
  - padding: 10px 20px 10px 20px; (top, right, bottom, left)
- margin - controls the amount of space between an element's border and surrounding elements
  - If you set an element's margin to be negative, the element will grow larger
  - 4 individual sides can be controlled
  - margin-top, margin-right, margin-bottom, margin-left
  - margin: 10px 20px 10px 20px; (top, right, bottom, left)
- border

<style>
  .blue-box {
    /* padding: 20px; */
    /* padding-top: 40px;
    padding-left: 40px;
    padding-bottom: 20px;
    padding-right: 20px; */
    padding: 40px 20px 20px 40px;
    /* margin: 20px; */
    /* margin: -15px; */
    /* margin-top: 40px;
    margin-left: 40px;
    margin-bottom: 20px;
    margin-right: 20px; */
    margin: 40px 20px 20px 40px;
  }
</style>

# Use Attribute Selectors to Style Elements

[attr=value] attribute selector matches and styles elements with a specific attribute value.

<style>
  [type='radio'] {
    margin: 20px 0px 20px 0px;
  }
</style>

# Understand Absolute vesus Relative Units

Absolute units tie to physical units of length. in and mm refer to inches and millimeters. Absolute length units approximate the actual measurement on a screen, but there are some differences depending on a screen's resolution.

Relative units, such as em or rem, are relative to another length value.
em is based on the size of an element's font. If you use it to set the font-size property, it's relative to the parent's font-size.

There are several relative unit options that are tied to the size of the viewport.

<style>
  .red-box {
    padding: 1.5em;
  }
</style>

# Inherit Styles from the Body Element

You can style <body> element just like any other HTML element, and all your other elements will inherit your <body> element's styles.

<style>
  body {
    background-color: black;
    color: green;
    font-family: monospace;
  }
</style>

# Prioritize One Style Over Another

The latest declaration will always take precedence over the earlier declarations.
Browsers read CSS from top to bottom.
In the event of a conflict, the browser will use whichever CSS declaration that came last.

<style>
  .pink-text {
    color: pink; 
  }

  .blue-text {
    color: blue;
  }
</style>
<!-- blue-text overrides pink-text -->
<h1 class="pink-text blue-text">Hello World!</h1>

# Override Class Declarations by Styling ID Attributes

id attributes will always take precedence over classes.

<h1 class="pink-text blue-text" id="orange-text">Hello World!</h1>

# Override Class Declarations with Inline Styles

Inline styles override id and classes

<h1 id="orange-text" class="pink-text blue-text" style="color: white;">Hello World!</h1>

# Override All Other Styles by Using Important

In many situations, you will use CSS libraries. These may accidently override your own CSS. When you absolutely need to be sure that an element has specific CSS, you can use !important.

<style>
  .pink-text {
    color: pink !important;
    /* !important overrides inline, id, classes. The most powerful. */
  }
</style>

# Use Hex Code for Specific Colors

Hex code - hexidecimal code.

Decimals are base 10 numbers, which use symbols 0 to 9 for each digit. 10 total possible values.
Hexidecimals are base 16 numbers, which use symbols 0 to 9, then ABCDEF for ten to fifteen. 16 total possible values.

<style>
  body {
    color: #000000;
  }
</style>

# Use Hex Code to Mix Colors

0 is the lowest number in hex code, represents a complete absence of color.
F is the highest number in hex code, represents the maximum possible brightness.

Hex Code can be abbreviated to 3 digits: #F00 for red. Like RGB.

# Use RGB values to Color Elements

RGB value for black: rgb(0, 0, 0)
RGB value for white: rgb(255, 255, 255)

Specify the brightness of each color with a number between 0 and 255.

<style>
  body {
    background-color: rgb(255, 165, 0);
  }
</style>

# Use CSS Variables to change several elements at once

To create a CSS variable, give it a name with two dashes in front of it and assign a value:

--penguin-skin: gray;

# Use a custom CSS Variable

After creating the CSS variable, you can assign its value to other CSS properties by referencing the name you gave it.
Variables names need to be an exact match.

<style>
  body {
    background: var(--penguin-skin);
  }
</style>

# Attach a Fallback Value to a CSS Variable

You can attach a fallback value that your browser will revert to if your CSS variable is invalid.

Note: This fallback is not used to increase browser compatibility, and it will not work on IE browsers. It is used so that the browser has a color to display if it cannot find your variable.

Useful for debugging.

<style>
  body {
    background: var(--penguin-skin, black); /* It will set the background to black if the variable isn't set. */
  }
</style>

# Improve Compatibility with Browser Fallbacks

Browsers ignore any properties it doesn't recognize or support.
Internet Explorer does not support CSS variables.

If you do want to provide a browser fallback, provide another more widely supported value immediately BEFORE the variable declaration.
The older browser will have something to fall back on, while a newer browser will just interpret whatever declaration comes later in the cascade.

<style>
  :root {
    --red-color: red;
  }
  .red-box {
    background: red;
    background: var(--red-color);
  }
</style>

# Cascading CSS variables

When you create a variable, it becomes available for your to use inside the element in which you create it. It also becomes available within any elements nested within it. This effect is called cascading.

Because of cascading, CSS variables are often declared in the :root element.

:root element is like the container for the entire HTML document.
By creating your variables in :root, they will be available throughout the whole web page.

<style>
  :root {
    --penguin-belly: pink;
  }
</style>

# Change a Variable for a Specific Area

You can override variables set in :root by setting them again within a specific element.

<style>
  :root {
    --penguin-belly: pink;
  }

  .penguin {
    --penguin-belly: white;
  }
</style>

# Use a Media Query to Change a Variable

CSS variables can simplify the way you use media queries.

For instance, when your screen is smaller or larger than your media query break point, you can change the value of a variable, and it will apply its style wherever it is used.

<style>
  :root {
    --penguin-size: 300px;
    --penguin-skin: gray;
    --penguin-belly: white;
    --penguin-beak: orange;
  }
  
  @media (max-width: 350px) {
    :root {
      
      /* add code below */
      --penguin-size: 200px;
      --penguin-skin: black;
      /* add code above */
      
    }
  }
</style>
