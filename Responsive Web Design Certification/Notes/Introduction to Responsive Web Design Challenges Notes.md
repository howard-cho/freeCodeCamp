# Create a Media Query
Media Queries are new in CSS3 that change the presentation of content based on different viewport sizes.

Viewport - a user's visible area of a web page, different depending on the device used to access the site.

Media Queries consist of a media type, and if that media type matches the type of device the document is displayed on, the styles are applied.
You can have as many selectors and styles inside your media query as you want.

Media query that returns the content when the device's width is less than or equal to 100px:
`@media (max-width: 100px) { /* CSS Rules */ }`

Media query that returns the content when teh device's height is more than or equal to 350px:
`@media (min-height: 350px) { /* CSS Rules */}`

CSS inside the media query is applied only if the media type matches that of the device being used.

`p` tag has a `font-size` of 10px when the device's height is less than or equal to 800px.
<style>
  p {
    font-size: 20px;
  }
  
  @media (max-height: 800px) {
    p {
      font-size: 10px;
    }
  }
</style>

# Make an Image Responsive

<style>
  img {
    max-width: 100%;  /* scales the image to fit the width of its container, but won't stretch wider than its original width */
    display: block;  /* changes the image from an inline element (its default), to block element on its own line */
    height: auto;  /* keeps the original aspect ratio of the image */
  }
</style>

# Use a Retina Image for Higher Resolution Displays
The simplest way to make your images appear "retina" (and optimize them for retina displays) is to define their width and height values as only half of what the original file is.

# Make Typography Responsive
Instead of using em or px, you can use viewport units for responsive typography.
Viewport units are relative to the viewport dimensions (width or height) of a device.

Four different viewport units:
- `vw - 10vw` would be 10% of the viewport's width.
- `vh - 3vh` would be 3% of the viewport's height.
- `vmin - 70vmin` would be 70% of the viewport's smaller dimension (height vs. width).
- `vmax - 100vmax` would be 100% of the viewport's bigger dimension (height vs. width).

<style>
  h2 {
      width: 80vw;
  }
  p {
      width: 75vmin;
  }
</style>

