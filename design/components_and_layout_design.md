# Components and Layout Design

## Cover and Spine Components

### Cover Block Logo Title
### Cover Block Logo Subtitle
### Cover Document Title
### Cover Graphic 

### Spine Title
### Spine Subtitle
### Spine Logo

### Back Cover Logo
### Back Cover Logo Title
### Back Cover Logo Subtitle
### Back Cover Footer

## Body and Text Components

### Chapter Title

* Uses upper-case lettering in BOLD
* Uses heavy underline, full width of the page

### Table of Contents

* Uses Normal Text font size and weight
* Uses 2-space indent for each sub-section
* Uses right-aligned chapter/section numbering, only one section deep, chapter number in bold, section number not in bold.
* Uses periods to pad out extra space between ToC text and chapter numbers

### Chapter Section Heading Level 1

* Uses uppercase bold text with full width lines above and below
* Uses single space empty line padding below, and two empty lines above
* Long lines wrap at page width, breaking at word. See 2-12.

### Chapter Section Heading Level 2 

* Uses bold text in the same size as paragraph text.
* Break long lines into two roughly equal length wrapped lines See 4-12.

### Paragraph Text

* Uses Helvetica text in various bold/italic forms.
* Uses em-dash instead of colons or other spacers

### Figures
### Figure Captions

### Indented Formula and Other Examples

See 4-12

* Preformatted text indented 

## Page Layout Components

### Page Header

* Contains the Chapter title in bold, underlined with heavy full width line. 
* Note that there is no separate display of chapter title inline. 
* There is always a full blank page between chapters.
* Text aligned left for left-hand pages and right for right-hand pages.

### Page Footer

* Shows the chapter number in bold, with a hyphen and first level of section numbering non-bolded.
* Text aligned left for left-hand pages and right for right-hand pages.

### Two Column Display for Graphics

* Uses two columns in %% proportions with image to left, and text to right (see 2-1 in manual)

### Table Layout

See 2-31 for example

* Uses horizontal single point lines above and below each row, but no vertical lines between cells
* Uses bold text for header
* Uses various alignments for header, but generally uses left-alignment, or center

### Alt Table Layout

See A-1 for example

* Three Columns, with column 1 having no heading, and no lines at all.

### Images

See 1-8 and 1-9

* Full width images break text flow (no wrap)

### Labeled Diagram and Legend

See 1-6, 1-7

* Labeled diagram uses circle around letter with a line pointing to a part of the diagram. 
* Legend uses circled letters with a title in bold, followed by a description on the next line, aligned with the 
  title text, not the circled letter

### Appendices

* In ToC each chapter is given a letter, not a number, but each section within it is given a number as usual
* The chapter title of the appendices is always "APPENDICES" instead of the title for that appendix-chapter
* In the ToC these are listed as "A-1"... etc, but in the index listed as "Appendix-1".


### Index 

* Uses similar formating to ToC except it is in two half-width columns and it is sectioned by the initial letter in 
  bold, with an empty line between each section

### Page Continuation

* in smaller font size
* italic but not bolded paragraph font
* uses the text "(continued)", right aligned on the page
* indicates that there is more of this element on the next page (e.g. for long tables, or the index)
* IDEA: We could constrain tables, ToC, etc to a max vertical height, and if it is longer, scroll within a box and 
  indicate this with the "(continued)" symbol until bottom of scroll area is reached.

### Notes Section

* At the end of the book there are a few pages for notes.
* page is blank other than a center-algined non-bold text "NOTES"
* no header/footer
* IDEA: Could we implement this as a text area that saves its content to local browser storage? This way a 
  person can take notes, within their browser.... 


### Spacing

## Visual Design

### Colors

The majority of the manuals are printed on standard white paper with black ink. On the cover, white text on a blue
background is used, and on the back cover/spine, the same blue color is used for text against a white background. 

One question is how to use texture in this project. Should we attempt to make the cleanest digital representation
using solid colors with no texture, or should we attempt to apply a softer paper-like texture to the backgrounds?
What about colors? The manual I have is nearly 40 years old and the white paper is beginning to yellow and the blue
colors are starting to fade. Should we attempt to match this faded and yellowed feeling? When new, were these colors
more vibrant and the paper more of a "true white"? Also, what about the edges of the text? Print has a naturally 
softer/fuzzier edge than digital text. Should we aim for the crispest image, or try to recreate the softness of 
print? Similarly, ambient light will change the look and feel of the printed page. Reading under full indirect
sunlight will be different than reading under a dim incadescent bulb, and also different from the bright florescent
lighting you may find in an office or retail warehouse. Which environment should we attempt to capture with the 
colors and the intensity of those colors? 

These remain open questions. We may make a variety of subtle variations of the visual design to recreate different
looks, leaving it up to you to decide which is most appropriate for your project. 

### Fonts

This project will attempt to matchs fonts as closely as possible to the specific fonts used in these manuals. This 
could be a difficult task, because some of these fonts may no longer be available, may be copyrighted, or may 
never have been made available as a digital font. 

In the TI-5310 Business Manager manual, we see at least two fonts in regular use; a display font and a text font.

The text font seems to be Helvetica. This is used through the majority of the book's text, in either regular, 
bold, or italic form. It is also used on the front page for the words "TEXAS INSTRUMENTS".

Since Helvetica is a copyright protected font, and may not be installed everywhere, we've opted for a free font
called "Nimbus Sans L" which is very similar. Other Helvetica alternatives were sufficiently different that we
didn't feel comfortable using them (e.g. Arial w/ its diagonal cuts, Universe w/ its non-slanted bar on the 5, etc)

Downloaded from Font Squirrel: https://www.fontsquirrel.com/fonts/nimbus-sans-l

The front cover uses a display font for "TI-5310 BUSINESS MANAGER" and "GUIDEBOOK". This font seems to be Architype 
Renner Bold but this font was not released until 2011, so it must be an earlier font that Architype Renner is based on.
Some research suggests this was a bold font designed by Renner in the 20s and there are some versions of it available.
One such example is the `Jost*` font, which is available here https://indestructibletype.com/Jost.html ... This uses
diagonal cuts to the `1` character instead of striaght, vs the Architype Renner font, so we've decided to stick with 
that one. It's unclear if the Architype Renner font is free or not, but seems to be ok to use for this. 

https://www.dafontfree.io/architype-renner-font/

NOTE: The font Futura is very similar but has significant differences, enough that it is clearly not the same font.

In the manual there are places where a monospaced font is used. We will not be including that because it's actually
meant to show the print/display font of the actual calculator being documented. We are not attempting to recreate the
calculator look and feel, just the look of the manual, and this would vary by the device being documented. So we've 
choosen to leave that out. 

In addition, we plan to patch the fonts to handle some alignment issues (see the alignment of square brackets to 
their contents, among other issues). That's a TODO...

Webfonts were generated with Font Squirrel: https://www.fontsquirrel.com/tools/webfont-generator

Font Fallbacks... Using Better Helvetica recommendation (with our own webfont as the first choice)

https://css-tricks.com/snippets/css/better-helvetica/

For the Renner font, `Century Gothic Bold` and `Futura Bold` are close fallbacks that are installed on Macs. Also, Avenir Black, Avenir Std 95 Black, Nevis

PT Sans

Walkway (family)

Caviar Dreams

Cicle (family)

Kozuka Gothic Pro L (Kozuka is a family)

Futura ("Futura", "Futura Std", "Futura LT Medium", "Futura Md BT", "Futura No 2"), Avenir ("Avenir Medium", "Avenir 55 Roman", "Avenir Next LT Pro"), or even Avant Garde

Arial Black

### Line Sizes and Weights


