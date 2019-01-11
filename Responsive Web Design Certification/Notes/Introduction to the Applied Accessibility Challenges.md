"Accessibility" - having web content and a user interface that can be understood, navigated, and interacted with by a broad audience.

1. Have well-organized code that uses appropriate markup.
2. Ensure text alternatives exist for non-text and visual content.
3. Create an easily-navigated page that's keyboard-friendly.

# Add a Text Alternative to Images for Visually Impaired Accessibility

alt text describes the content of the image and provides a text-alternative.
alt text displays when the image fails to load, or can't be seen by the user.
Used by search engines to understand what an image contains to include it in search results.

<img src="importantLogo.jpeg" alt="Company logo">

Screen readers can access the alt attribute and read its contents to deliver key information.

Good alt text is short but descriptive, and meant to briefly convey the meaning of the image.
HTML5 considers alt text mandatory.

# Know When Alt Text Should be Left Blank

In situations when an image is already explained with text content, or does not add meaning to a page, the img still needs an alt attribute, but it can be set to an empty string.

<img src="visualDecoration.jpeg" alt="">

Background images are usually applied with CSS rules and not part of the markup screen readers process.

You may still want to include alt text for search engines to catalog the content of the image.

# Use Headings to Show Hierarchical Relationship of Content

Headings (h1 through h6) provide structure and labeling to your content.
Screen readers can be set to read only the headings on a page so the user gets a summary.

Heading tags should have semantic meaning and relate to each other, not picked merely for their size values.

Semantic meaning - the tag you use around content indicates the type of information it contains.

Headings with equal (or higher) rank start new implied sections, headings with lower rank start subsections of the previous one.

Each page should always have one (and only one) h1 element, which is the main subject of your content.
Headings are used in part by search engines to understand the topic of the page.

# Jump Straight to the Content Using the main Element

The <main></main> element is used to wrap the main content. There should only be one per page.
Meant to surround the information that's related to the central topic of your page.
It is not meant to include items that repeat across pages, like navigation links or banner.

The main tag also has an embedded landmark feature that assistive technology can use to quickly navigate to the main content.

# Wrap Content in the article element

<article></article> is a sectioning element, and is used to wrap independent, self-contained content.
The tag works well with blog entries, forum posts, or news articles.

If you removed all surrounding content, would that content still make sense?

<section></section> is for grouping thematically related content.
For example, if a book is the article, then each chapter is a section.

Use a div when there are no relationships between groups of content.

<div></div> - groups content
<section></section> - groups related content
<article></article> - groups independent, self-contained content

# Make Screen Reader Navigation Easier with the header Landmark

<header></header> is used to wrap introductory information or navigation links for its parent tag.
Works well around content that's repeated at the top on multiple pages.

header also has the embedded landmark assistive feature that quickly navigates to the content for screen readers.

<header></header> is meant for use in the <body></body> tag, different than the <head></head> element, which contains the page's title, and meta information.

# Make Screen Reader Navigation Easier with the nav Landmark

<nav></nav> is meant to wrap around the main navigation links in your page. Includes the embedded landmark feature.

Repeated site links at the bottom of the page use <footer></footer>

# Make Screen Reader Navigation Easier with the footer Landmark

<footer></footer> is used to contain copyright information or links to related documents that usually sit at the bottom of a page. Includes the embedded landmark feature.

# Improve Accessibility of Audio Content with the audio Element

<audio></audio> wraps sound or audio stream content

The controls attribute shows the browser's default play, pause, and other controls, and supports keyboard funtionality. A boolean attribute.

<audio id="meowClip" controls>
  <source src="audio/meow.mp3" type="audio/mpeg" />
  <source src="audio/meow.ogg" type="audio/ogg" />
</audio>

# Improve Chart Accessibility with the figure Element

<figure></figure> and <figcaption></figcaption> wrap a visual representation (image, diagram, chart) along with its caption.

<figure>
  <img src="roundhouseDestruction.jpeg" alt="Photo of Camper Cat executing a roundhouse kick">
  <br>
  <figcaption>
    Master Camper Cat demonstrates proper form of a roundhouse kick.
  </figcaption>
</figure>

# Improve Form Field Accessibility with the label Element

<label></label> wraps the text for a specific form control item, usually the name or label for a choice.
The for attribute on a label tag explicitly associates that label with the form control is used by screen readers.

The value of the `for` attribute must be the same as the value of the id attribute of the form control.

<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name">
</form>

# Wrap Radio Buttons in a fieldset Element for Better Accessibility

<fieldset></fieldset> surrounds the entire grouping of radio buttons to semantically show the radio button choices are part of a set.
<legend></legend> is often used to provide a description for the grouping to be read by screen readers.

`fieldset` and `legend` tags are not necessary when the choices are self-explanatory, like a gender selection.

<form>
  <fieldset>
    <legend>Choose one of these three items:</legend>
    <input id="one" type="radio" name="items" value="one">
    <label for="one">Choice One</label>
    <br>
    <input id="two" type="radio" name="items" value="two">
    <label for="two">Choice Two</label>
    <br>
    <input id="three" type="radio" name="items" value="three">
    <label for="three">Choice Three</label>
  </fieldset>
</form>

# Add an Accessible Date Picker

Forms often include the `input` field, with the `type` attribute that indicates what kind of input will be created.

A date picker shows up in the input field when it is in focus.

For older browsers, the type will default to text, which will show users the expected date format in the label or as placeholder text just in case.

<label for="input1">Enter a date:</label>

<input type="date" id="input1" name="input1">

# Standardize Times with the HTML5 datetime Attribute

<time></time> along with the `datetime` attribute can wrap a date or time on a page. Inline element
`datetime` attribute holds a valid format of the date. Accessed by assistive devices to avoid confusion by stating a standardized version of a time.

<p>Master Camper Cat officiated the cage match between Goro and Scorpion <time datetime="2013-02-13">last Wednesday</time>, which ended in a draw.</p>

# Make Elements Only Visible to a Screen Reader by Using Custom CSS

Sometimes information is in a visual format (like a chart), but a screen reader needs an alternative presentation (like a table) to access the data.
CSS is used to position the screen reader-only elements off the visual area of the browser window.

<style>
  .sr-only {
      position: absolute;
      left: -10000px;
      width: 1px;
      height: 1px;
      top: auto;
      overflow: hidden;
  }
</style>

`display: none;` or `visibility: hidden;` hides content for everyone, including screen reader users.

Zero values for pixel sizes, such as `width: 0px; height: 0px;` removes that element from the flow of your document, meaning screen readers will ignore it.

# Improve Readability with High Contrast Text

Sufficient contrast improves the readability of your content.
The WCAG recommends at least a 4.5 to 1 contrast ratio for normal text.
The ratio is calculated by comparing the relative luminance values of two colors.
1:1 for same color, 21:1 for white against black, the strongest contrast.

# Avoid Colorblindness Issues by Using Sufficient Contrast

Foreground and background colors need sufficient contrast so colorblind users can distinguish them.
Darkening the darker color and lightening the lighter one with the aid of a color contrast checker.

# Avoid Color Blindness Issues by Carefully choosing Colors that Convey Information

The most common form of colorblindness is the reduced sensitivity to detect greens.
If two similar green colors are the foreground and background color of your content, a colorblind user may not be able to distinguish them.

# Give Links Meaning by Using Descriptive Link Text

You should use brief but descriptive text within the `a` tags to provide more meaning for screen reader users.

# Make Links Navigatable with HTML Access Keys

`accesskey` attribute specifies a shortcut key to activate or bring focus to an element. This can make navigation more efficient for keyboard-only users.

HTML5 allows `accesskey` attribute to be used on any element.
Particularly useful when used with interactive elements like links, buttons, and form controls.

<button accesskey="b">Important Button</button>

# Use tabindex to Add Keyboard Focus to an Element

`tabindex` attribute has three distinct functions relating to an element's keyboard focus.

When it's on a tag, it indicates that element can be focused on. The value (integer that's positive, negative, or zero) determines the behavior.

Certain elements, such as links and form controls, automatically receive keyboard focus when a user tabs through a page.
It is in the same order as the elements come in the HTML source markup.

Other elements such as `div`, `span`, and `p` can receive this same functionality by placing a `tabindex="0"` attribute on them.

<div tabindex="0">I need keyboard focus!</div>

A negative `tabindex` value (typically -1) indicates that an element is focusable, but is not reachable by the keyboard.
Used to bring focus to content programmatically (like when a `div` used for a pop-up window is activated).

Using `tabindex` also enables the CSS pseudo-class `:focus` to work on the element.

# Use tabindex to Specify the ORder of Keyboard Focus for Several Elements

`tabindex` also specifies the exact tab order of elements. Achieved when the value is set to a positive number of 1 or higher.

tabindex="1" will bring keyboard focus to that element first, then cycles to tabindex="2", tabindex="3", etc, before moving to the default and tabindex="0" items.

When tabindex is used, it overrides the default order (which uses the HTML source).

<div tabindex="1">I get keyboard focus, and I get it first!</div>
<div tabindex="2">I get keyboard focus, and I get it second!</div>
