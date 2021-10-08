Images

images were added late (all things considered) for the internet

images are served using standard delivery resources (generally an http request).

browsers are the processing system for the images.
 this means that some browsers cannot view certain image types.
  notoriously, older browsers would not be able to read png or other image formats.
   here's a list of this: https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types

  do not expect that images will render 100% same on the device, especially in terms of color.

Wanna use an image
 <img>
  src? image source location
  semantics now requires alt for screen readers

  can be loaded with async!
  can be loaded with a map to create a specific map of clicking locations on an image.

  loading
   eager and lazy!

 for width and height of image, don't rely on properties, use css



Colors

most browsers will read colors based on their systems color profile and bit depth.
 this was an issue of big concern in the past
 now, less important but can change color rendering for some

Most (always most) browsers support multiple color formats including RGB, RGBA, HEX, color names (red, green, etc), hsl, and hsla.

colors can be inherited
most colors can be applied to MOST elements in the DOM.


Text

can be default (web safe) fonts, or embedded
Most are using WOFF or WOFF2 format for embedded fonts
 Will download to browser

Web has nearly FULL contorol for typography
 kerning
 leading
 tracking
 etc

Text can have size, color, visibility
can have per letter settings.

Text is a first level priority for browsers. Most text is downloaded before rendered, styling being applied before render by the DOM.

Text can have internationalization by using different charsets
 charsets are set in the html file in the head.
 most browsers support things like right -> left reading and vertical reading as well.

text is read by search engines
 this is the (mostly) only thing a search engine cares about.
 text can have semantic tags for SEO purposes.
 h1 -> h9



JPEG v PNG v GIF

guh-if or ji-if
 lol

JPEG highly compressed generally by removing high frequency detail to leave stronger medium and low level frequency information.
 great for compression
  reds suffer most as images store most frequency detail in the red channel
 unless using jpeg2000, no transparency and jpeg2000 is not well represented.

png
 great for good quality images.
 can be compressed, and have a better compression algo
 will be larger than other images
 can include transparent channel.

gif!
 giphy! jk
 gif is highly compressed
  can become VERY large very quickly
  can have animation
  can have transparency
 generally used less than jpg or png for standard pictures, but used strongly for image that has minor changes (think giphy animated images).

for photos, use jpeg
for web images, esp for design or layout, use png
use gif for sequenced images, or moderate quality transparent pictures.

