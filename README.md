# drummer-outline-renderers
A repo to encourage collaboration on developing outline renderers for the Drummer app from Dave Winer

# Welcome to the Drummer Outline Rendering project!

An area of Drummer that has not been explored is how to take the content of an outline and render it into the form of a document. The Old School feature within Drummer renders outlines into the format of a weblog post, but this is only one application of outliner output.

To foster collaboration and creativity in this area, I have created this Github repo to share some examples, and to get feedback from other Drummer users on what they would like to see. 

The initial script I have created will scan a two-level outline (an outline with headings and one level of subheadings) and create a web page with the content from that outline. In this first example, the subheadings are not indented, so the text from both first level and second level headlines are treated as paragraphs at the same level. I have added a minor check for double-quote marks within the text of each heading to convert it to the web form (&quot;) so that the text string formed by concatenating all of the headlines does not have an error in display. This does have the effect of modifying web hyperlinks to where they do not display (although the link text is present). I am looking for help/suggestions with this problem – please reach out!

To get a copy of the script, first open my sharedScripts OPML file in Drummer (http://drummer.scripting.com/AndySylvester99/sharedScripts.opml ) using the File → Open URL menu item and copy the script headline “twoLevelOutlineRenderer” to your Scripts menu outline. To open the Scripts menu outline, go to the File → Special files → Scripts menu item. Once you have pasted the script, you should see “TwoLevelOutlineRenderer” appear in your Scripts menu.

To use the script, open a tab with an outline to be rendered, or select a tab that is already opened. Next, go to the Scripts menu and select the “TwoLevelOutlineRenderer” menu item. Drummer will open a new browser tab to display the page. If the text “object Object” is displayed in the new browser tab, switch back to Drummer and run the script again. Drummer will open another browser tab, and the rendered text should appear in the new browser tab.

# Area for experimentation

# Page design

This initial version of the script reads an HTML template from my personal website for creating the web page. This file contains a CSS style element which can be modified to change the font size and type (.divHappyOutline). You can save a copy of this in a different location and update as you wish. If you do that, make sure to update the script parameter urlTemplate to point to the new location of the file. Also, make note of whether the file is hosted using HTTP or HTTPS. On my site, I use HTTP, although for some reason my template file is using an HTTPS URL – I don’t understand this, but ...oh well…..

# Script design

As mentioned earlier, the script performs rendering of all headlines as paragraphs (no indenting). This could be changed in the script to apply a CSS property to cause indentation (for example, see https://www.w3schools.com/cssref/pr_text_text-indent.asp). Also, the script only handles a two level outline, so an obvious improvement would be to handle multi-level outlines.

# Problem reporting

If you have a problem, please create an issue in this repo. 

# Use cases

Schoolwork

The initial use case was to be able to render an outline such that it could be turned in as an assignment for school.

Meeting handout

Be able to create a handout from an outline that could be distributed in a meeting.


If anyone has other use cases to propose, please create an issue in this repo.

# Credits

[Ken Smith](http://oldschool.scripting.com/KenSmith/)- "The user" who proposed this idea (I of course am "the developer"!)

[Little Outliner](http://littleoutliner.com/) - Used the Build a Listicle feature as prior art

