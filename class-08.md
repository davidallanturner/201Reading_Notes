Layouts

grid, liquid, and mediums oh my.

##block level elements vs inline elements##
block level elements will always go to a new line.
inline elements will have things next to each other.

Containing elements are block level elements at a high level that form containers or parents for major sections of items. eg: nav, main, foot, asides, etc.

##positioning scheme##
normal: block is block on new level and new line.
relative: moves elements themselves, but does not affect position of surrounding elements or space
absolute: items moved, all other items ignore space would have taken. directs exact positioning. - may cause overlaps

box offset
fixed: relative to browser, not containing element. Stays when scrolling, stickied to size of browser.

floating elements: take element out of flow and move to left or right. element becomes block-level element.

with overlaps, z-index fixes overlaps.

###flow###
position static
blck is usually one on top of another.
static is default.

float: moves items left or right as far in the container as possible. The flow is moved around the item. 

floats can be used to put items side by side.

height and width can affect where the element sits.

common to clear floats
left right both none
left: left side of box should not touch any other elements in the same container.
right: right side of the box will not touch elelements in the same container.
both: neither left nor right side will touch any other element in the container.
none: elements can touch either side.

**issues**
if everything is floated, some browsers treat the container or elements like they are 0px tall.
solution is adding extra element after last floated box.
css rule would have clear of both.

new method of fix is:
overflow auto; width: 100%


floats can make multi column layouts.
width set to force colums to correct size.
float to put them next to each other.
margin to put spacing between them.
can be used for multiple columns.


Different screens have different resolutions and that can affect how your site is layed out.

Designing your page for each possible browser size is impractical, but you can use breakpoints to design common sizes.
Mobile first design should be your focus.
Remember that your layout and load time can affect user perception of your site.
Your design above the fold (the inital part of the browser that your user sees) will make a large determination of what the site has and does for the user.

fixed width layouts
uses pixels for sizing. can have pixel perfect style.
can control flow of text, etc.
best used when you need to have a specific design layout for your site.
can end up requiring a lot of finding of items. If resolution or size is too large or small, can cause user experience to suffer.

liquid layouts
usually uses percentages
can fill the page appropriately depending on size of viewing device.
design can look different and can have unintended consequences.
without min or max width, text can become harder to read.
Fixed width items will break layout and pages.


fixed width layouts use width with pixel
liquid uses percentages (set min and max)

