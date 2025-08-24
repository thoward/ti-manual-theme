# Design

## Context

The context for this project is rooted in an appreciation for the writing culture of early technologists from the 
80s. At the time of this writing, 2021, I'm 43 years old. I first started using computers in 1985 when I was 7 years old. 
This era of computing was deeply inspiring to me and I hold a lot of nostalgia for it. Also, there seems to be a 
clarity of focus from that time, which is largely lost in modern tech industry culture. Maybe no more profoundly than in 
the writing that accompanied technology.

The old printed manuals which came with your calculator or computer were the only resource, the only teacher, that you 
had to help with unlocking the mysteries of the device. They were carefully crafted by skilled technical writers, and 
once released they were not updatable. So a lot of deep care went into each manual, and a lot of considered design.

I miss this vibe and want to recreate that.

## Form

I found a nearly untouched, pristine copy of a TI-5310 Business Manager calculator manual in a local second hand 
store. This will be my reference for building this theme.

However, there are aspects of the original form which will need to be updated to be suited for the modern reading 
environment. Firstly, the original format was focused on print media. There are some forms within print that aren't 
relevant to the modern reading environment, specifically, the page. In a print manual, the layout of the information 
is constrained to a page. The width and height of the page determine many things about the resulting design. There 
are features of this manual such as *page headers* and *page numbers* which do not naturally fit into a webpage context.
Also the width of a paragraph is determined in inches, or the count of characters that can fit within the margins. 

For example, if we look at my model print manual, the plain text paragraph can allow 64 fixed width characters, and 
roughly 46 vertical lines. With websites we have no such fixed viewing environment. Computer monitors can easily 
display more than 64x46 characters, and it is common for a screen of text on a computer to scroll vertically, meaning
there is not practical vertical line limit.
variety of screens, from full sized desktop monitors, to laptop monitors, to tablets, to phones, we have a widely
varying screen width to work with. Paragraph text is expected to adjust to the screen width and documents are expected 
to grow and scroll vertically for as long as needed.

Also factored into this are margins on the sides, tops, and bottoms of pages.

There are some ways we can adapt these components to the website form, which each have some tradeoffs:

   - Fixed width: We can set a fixed character size and page width expressed as a quantity of characters, eg 64 chars wide
     on screens where this is too wide, it will scroll both horizontally and vertically.
   - Percentage Width: We can express the paragraph area and margins as a percentage of the available page width, with a 
     varying amount of characters that can be displayed. This causes some problems because other elements would then also 
     need to scale and flow their contents, and some are less easily "flowed" and scaled than others (e.g table layouts)
   - Virtual Pages: Another alternative is to recreate the concept of the page within the computer environment, which
     we see with tools like PDF readers and Google Docs/MS Word in "print layout", which use a page model concept. That is 
     because these are print focused document applications, which intend for the contents to eventually be printed out. 
     This would create virtual pages, likely vertically aligned with scrolling up and down vs flipping pages in a book. 
   - Full Skeumorphism: A virtual book model with pages flipping side to side, only showing one or two at a time, just
     as traditional paper books would be.

Along with page, we also have some concepts like the cover, inside cover, back cover, spine, book info/copyright page, and the
standard ordering of the Table of Contents preceding the Body Text, organized into one or more chapters, with one or more 
Appendices and Indices following that Body Text. None of these fit neatly into the context of HTML pages and typical 
website information architecture. They are generally expected to be read in a linear manner from front to back, and then 
used as a reference later using the ToC and Index to quickly navigate to a previously read section.

Rather, a website will have a landing page (similar to a cover), a navigation menu, an always-present Table of Contents
(typically in a sidebar), a search bar rather than an index, and no meaningful distinction between body text articles,
rarely any concept of chapters or the expectation of linear reading of articles, nor a concept of appendices being 
different from the main content. Further there is a footer for an entire article, not per page, and it tends to contain
site-wide information and navigation links. There is no near-content way to handle footnotes, rather those are collected
at the end of an article and linked, meaning a reader must jump back and forth between the bottom of the page and their
reading location as needed, rather than simply glancing at the bottom of the page they are currently reading as they go.

There is no meaningful analog to the back cover, spine, inside cover, or copyright page. Rather the meta info is usually
collected in an "about" page article, and listed in the ToC or footer. Spine information (title, author, publisher) may 
reside in the footer, or in the browser title bar, with its information assigned via the HTML META tags, and its display 
varying by browser and device.

So, these mismatches in form can be problematic. I will try to find reasonable compromises and analogs within the webpage 
context and do my best to port these informational and layout components and concepts over from print media as faithfully
as possible. 

The specifics of these components and their translation are captured in the Components and Layout Design document.

## Fit

Many software engineers are of a similar age range as me and would find this styling appealing. Many younger engineers
are fascinated with "retro styling" and would also appreciate it. Regardless of anachronism or nostalgia, I believe
strongly that this design style is highly functional and well designed for the task of conveying technical information
and so will remain useful and relevant without concern for the time or media that it is used on. Basic concepts like 
letter spacing, visual layout, font choice, and which components are represented and used, are all evergreen and will
be just as useful any time technical information needs to be conveyed via text.

