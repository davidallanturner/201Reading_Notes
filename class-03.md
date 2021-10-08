lists


ordered -- 1,2,3 -- for lists with steps --eg: recipe
unordered -- bullet points, not ordered -- eg: sales points of this model of car
definition -- used to define words

ordered
<ol><li></li></ol>
<ol> -- ordered list
<li> -- list items

unordered
<ul><li></li></ul>
<ul> -- Unordered List
<li> -- list item

definition
<dl><dt></dt><dd></dd></dl>
<dl> -- definition list
<dt> -- definition term
<dd> -- definition data

lists can be nested, but be careful of validation, some combinations do not go with other combinations and do not validate.


Boxes
“You can’t force creatives into a box. If you try, they’ll no longer be creative. And no one will want your box.”
? Ryan Lilly 

Boxes are the model for all things on a page.
All items exist with a box.
By default the size of the box is determined by what it contains in HTML.
	A background image will not make a box larger, but a new <p> tag would.


Sizing Boxes
	Absolute, relative.
	Absolute -- pixels,cm , mm, q, in, pc, pt
	Relative -- %, em, ex, ch,rem,em,lh,vw,vh,vmin, vmax

	Absolutes are used for pixel perfect percision
	Relative are used for responsive design

	Max and Min can be set to limit how small or large a box should be regardless of the window.
	


Box Model
	BMP
		Border -- Physical lined border (usually invisible) that seperates elements. 
			size, style and color can be changed per edge or as a whole. Always uses clockwise styling, individual edge styling, or shorthand styling.
		Margin -- room after the box between other boxes -- white space generation -- like line height
			Clockwise spacing on either shorthand or individual elements
		Padding -- how much space internal from the edge of the text. --similar to page margins in word
			clockwise spacing on either shorthand or individual elements

	After a boxes height and width are set (auto or manually), any BMP is added after to make it larger.
	

Overflow
	If you set a max width or height and something is larger than that (like an article excerpt), how do you handle the overflow?
		overflow: hidden || overflow: scroll
			there are others but this is the basics

Visibility
	Blocks can be made invisible and visible
		***!!!*** Security warning, all blocks that are invisble are STILL THERE in the HTML, do not use it to hide ANY sensitive data!!!!!!!!

Center content
	set width, set left and right margin to auto
	width: 300px ; margin-left:auto; margin-right: auto
		older browsers need text-align set to center in the containing box.
		To make sure the text isn't centered in your box but left or right aligned, change the text-align of the text element itself.

	IE6 warning: use a doctype to prevent width changes by the margin and padding.

Block display and visiblity
	Want to put several boxes side by side or "inline?"
		inline -- causes blocks to be in a line
		block -- default blocks have full block level action
		inline-block -- blocks are inline, but maintain some block features

visibility
	display: none || visibility: hidden
	display: none removes the element and the space it took (leaves a gap and shifts elements)
	visibility: hidden just makes the items invisible, does not refactor the DOM

DO NOT USE VISIBILITY FOR SECURE ITEMS!!!
DO NOT USE VISIBILITY FOR SECURE ITEMS!!!
DO NO.... ok

Border-images
	borders can have images, you can slice images using ps or something similar, or not. Stretch repeat and round will change how the border pictures appear.


box-shadow
	(shorthand can be expanded)
	horizontal offset, vertical offset, blur distance, spread of shadow, shadow color
	2px 2px 2px 5px rgba()
	
	insert creates inner shadow

	needs -moz and -webkit prefixes for full browser compatability

border-radius
	makes rounded corners
	top right clockwise.
	radius value is in pixels
	older browsers will show right angle corners
	must use -moz and -webkit to achieve full browser compatability

	border radius can have vertical and horizontal value for each corner creating flat rounding and such.
	Circle made by border radius equaling the height of box


Javascript Structure
	T/F programming languages have a vocabulary?
		True, and the vocbulary even makes a syntax. It's how a language is a language.
	
statements, bocks, loops and conditions are all types of vocabulary.
Javascripts vocabulary is case sensitive. eg: hello does not equal Hello

statements are mini tasks for the computer to follow. They are usually on their own line, and just like a sentence, end with a period (or a semicolon in this case)

need a paragraph use a code block. It use the "{" and "}" block to group similar thoughts or tasks. In this case, the paragraph doesn't get the period(;) all the sentences(statements) do.

T/F You should use comments to help others?
	True. There's 2 types of comments (or code that isn't executed, but there to help the programmer). That is, the multi-line and the single line. Single line can be used on the same line as a sentence(statement) but must go at the end.

	// -- single line, anything after it on this line will be commented and not read by the browser
	/* -- multi line, everything between this and the terminator "*/" will be comments and not interpreted into code.

variable -- a chunk of memory that stores a piece of information for later. A cubby hole with names that hold biger or complex things we can get later. eg: myName = 'David"
	variables are called later by using the name we gave them in memory.
	in our example, myName is the variable. Unless I am quoting the word "myName", the browser with automatically input 'David' every time it see's myName in the code.

To create a variable the syntax is 
	"keyword variableNameInCamelCaseUsually = 'Some Piece of data we want to store here'"
	3  variable keywords are:
		var -- traditional. sets a (semi)global variable can be read in (almost)all the code -semi-deprecated
		let -- replaces var, has scope, cannot be read in all parts of the code, ensures security, can be mutated, muxed, or changed to later fit the codes needs
		const -- new, is ALWAYS the same. Has scope. Const is used for things that will never change in your code. An example would be a tax rate for a local shop. The tax rate will never change while the code is running, as the local tax is the local tax. It can be turned off maybe but it will always be the local tax.

Asignment operator
	"="
	eg: let taxRate = 8.25
	Assignment evaluates EVERYTHING on the right of it first, and then sets the result of that, to the variable
	complex eg: let myName = firstName + " " + middleName + " " + lastName // David Allan Turner
	first it figures out my name, then it assigns it.

NOTE: variables can be undefined.
	eg: let nothing //unassigned so it is undefined.

Data Types
	numbers (1, 3.8, -7, e, pi, etc), string ('words in quotes'), booleans (true or false, on or off, defined or undefined), arrays (a list of different items created with square brackets and seperated by commas eg: ['string', 1.72398, true]), objects (complex structures of paramaters (deifintions, variables for that object like let ball = 'round') and methods, or named actions that allow you to do something to the object, like start: engineOn = true ). Also undefined (previously mentioned), and null (empty thing not undefined).

Vanilla JS does not require you to define the variable type.