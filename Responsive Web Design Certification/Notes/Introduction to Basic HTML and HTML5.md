HTML5 introduces more descriptive HTML tags.

<header></header>
<footer></footer>
<nav></nav>
<video></video>
<article></article>
<section></section>

These tags make your HTML easier to read, and also help with Search Engine Optimization (SEO) and accessibility.

The <main> HTML5 tag helps search engines and other developers find the main content of your page.

# Adding images to web page
You can add images to your website by using the <img> element, and point to a specific image's URL using the src attribute.

<img src="https://www.your-image-source.com/your-image.jpg" alt="Author standing on a beach with two thumbs up.">

<img> elements are self closing.
<img> elements must have an <alt> attribute. Used by screen readers to improve accessibility and is displayed if the image fails to load.

Note: if the image is purely decorative, using an empty <alt> attribute is a best practice.

<alt> attributes should not contain special characters unless needed.

# Linking to another web page
<a> anchor elements are used to link content outside of your web page. href attribute is the destination web address.

<a href="https://freecodecamp.org">this links to freecodecamp.org</a>

# Link to Internal Sections of a Page with Anchor Elements

<a> elements can also be used to create internal links to jump to different sections within a webpage.

You assign a link's href attribute to a hash symbol # plus the value of the id attribute for the element that you want to internally link to, usually further down the page. Then add the same id attribute to the element you are linking to.

An id is an attribute that uniquely describes and element.

<a href="#contacts-header">Contacts</a>
...
<h2 id="contacts-header">Contacts</h2>

When users click on the Contacts link, they will be taken to the section of the webpage with the Contacts header element.

<a> attribute target="_blank" forces the linked document to open in a new window tab.


# Nest an Anchor Element within a Paragraph

<p>
Here's a <a target="_blank" href="http://freecodecamp.org">link to freecodecamp.org</a> for you to follow.
</p>


Dead links can be created using the # symbol in the href="#"

# Turn an Image into a Link

You can nest your images within an <a> element.

<a href="#"><img src="image.jpg" alt="Three kittens running towards the camera."></a>

# Create a Bulleted Unordered List

<ul>
    <li>milk</li>
    <li>cheese</li>
</ul>

# Create an Ordered List

<ol>
    <li>Garyfield</li>
    <li>Sylvester</li>
</ol>

# Create a text field

input elements are self-closing
<input type="text">

Add placeholder text to text fields
<input type="text" placeholder="This is placeholder text">

# Create a Form Element
Submit data to a server using an action on a <form> element

<form action="/url-where-you-want-to-submit-form-data"></form>

# Add a Submit Button to a Form

A submit button will send the data from your form to the URL you specified with your form's action attribute

<button type="submit">this button submits the form</button>

# Use HTML5 to Require a Field

Require a specific field so that your user will not be able to submit your form until he or she has filled them out.

<input type="text" required>

# Create a Set of Radio Buttons

radio buttons can be used when you want the user to give only one answer out of multiple options

Each radio button can be nested within its own <label> element.
By wrapping an <input> element inside a <label> element, it will automatically associate the radio button input with the label element surrounding it.

All related radio buttons should have the same name attribute to create a radio button group.
By using a radio button group, selecting any single radio button will automatically deselect the other buttons within the same group ensuring only one answer is provided by the user.

<label>
  <input type="radio" name="indoor-outdoor">Indoor
</label>

It is best practice to set a for attribute on the <label> element, with a value that matches the value of the id attribute of the input element.
This allows assistive technologies to create a linked relationship between the label and the child input element.

<label for="indoor">
  <input id="indoor" type="radio" name="indoor-outdoor">Indoor
</label>


Add a pair of radio buttons to your form, each nested in its own label element. One should have the option of indoor and the other should have the option of outdoor. Both should share the name attribute of indoor-outdoor to create a radio group.

<label for="indoor">
    <input id="indoor" type="radio" name="indoor-outdoor">Indoor
</label>
<label for="outdoor">
    <input id="outdoor" type="radio" name="indoor-outdoor">Outdoor
</label>


# Create a Set of Checkboxes

Forms commonly use checkboxes for questions that may have more than one answer.

Checkboxes are a type of input.

Each checkbox can be nested within its own <label> element.
Wrapping an <input> element inside of a <label> element will automatically associate the checkbox input with the label element surrounding it.

All related checkbox inputs should have the same name attribute.

It is considered best practice to define the relationship between a chekbox input and its coresponding label by setting the for attribute on the label element to match the id attribute of the associated input element.

<label for="loving">
  <input id="loving" type="checkbox" name="personality">Loving
</label>

Add to your form a set of three checkboxes. Each checkbox should be nested within its own <label> element. All three should share the name attribute of personality.

<label for="shy">
    <input id="shy" type="checkbox" name="personality">Shy
</label>
<label for="outgoing">
    <input id="outgoing" type="checkbox" name="personality">Outgoing
</label>
<label for="crazy">
    <input id="crazy" type="checkbox" name="personality">Crazy
</label>

# Check Radio Buttons and Checkboxes by Default

You can set checkbox or radio button to be checked by default using the checked attribute.

<input type="radio" name="test-name" checked>


Example form:
<form action="/submit-cat-photo">
    <label><input type="radio" name="indoor-outdoor"> Indoor</label>
    <label><input type="radio" name="indoor-outdoor"> Outdoor</label><br>
    <label><input type="checkbox" name="personality"> Loving</label>
    <label><input type="checkbox" name="personality"> Lazy</label>
    <label><input type="checkbox" name="personality"> Energetic</label><br>
    <input type="text" placeholder="cat photo URL" required>
    <button type="submit">Submit</button>
</form>

# Nest Many Elements within a Single div element

<div></div>

# Declare the Doctype of an HTML Document, Head and Body of HTML Document

<!DOCTYPE html> <!-- HTML5 as the Doctype>
<html>
<head>
    <!-- metadata elements -->
</head>
<body>
    <!-- page contents -->
</body>
</html>

