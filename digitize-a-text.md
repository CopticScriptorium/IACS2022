# Digitize and Annotate a Text Using Coptic Scriptorium's GitDox Tool and Natural Language Processing Tools

In this tutorial, you will learn how to digitize and annotate a short Coptic text using our GitDox tool and NLP tools.  For participants in the NAPS workshop, we will provide a text and all the other necessary materials.  Check with the facilitators.  In groups of 2-4 people, you will transcribe a text and provide basic paleographic/manuscript encoding.

For more detailed documentation, visit our [wiki](http://wiki.copticscriptorium.org/doku.php?id=gitdox_workflow); some of this tutorial is taken from that documentation.

If you want to digitize a specific text for inclusion in the Coptic Scriptorium corpora and database, we would like to collaborate with you. Please contact us!

## Helpful Resources

Check out [Coptic Scriptorium's Documentation Page](https://copticscriptorium.org/documentation) including:
  * a [quick start overview guide](https://copticscriptorium.org/download/scriptorium_guidelines_overview.pdf)
  * transcription guidelines
  * annotation guidelines
  * part of speech tagging guidelines
  * and much much more!

## Login and Orientation to GitDox

GitDox is an online XML and spreadsheet editor which uses [GitHub](github.com/CopticScriptorium/) for data storage and versioning. Coptic Scriptorium currently uses GitDox to transcribe texts and edit them in a spreadsheet.Although you don't need to have a GitHub account to use GitDox, it's helpful.  For the purposes of the NAPS workshop, you don't need one.  If you want to collaborate with us or use GitDox in the future, you can get an account later.

GitDox is located at https://corpling.uis.georgetown.edu/gitdox/ .  Navigate there on your computer, and login using the username and password we provided you at the workshop.

When you log in to GitDox, you see a list of current documents. Use the dropdown menu above the list to display only documents from a certain corpus. You can also use the arrows to the right of each column name to sort by that column.

Documents are assigned to users. Please only edit documents assigned to you. If you believe a document should be assigned to you but isn't, please contact the person to whom it is currently assigned to confirm that you should be assigned the document before editing it.

Find the text we assigned to you in the workshop.  Click on the "Edit" button for your text.

## Saving and Committing

The transcription mode of GitDox has two options for saving work: save and commit. The save button saves changes within GitDox but does not commit those changes to GitHub. Your permission levels will not allow you to commit to GitHub; one of the workshop facilitators will complete this step of the process. 

Because GitDox depends on an internet connection, it's a good idea to save your work frequently while you're working using the save button.

## Adding metadata

Use the button at the bottom of the page to add metadata.  You will need to add your own names to the "annotation" metadata separated by commas (e.g., Caroline T. Schroeder, Rebecca Krawiec).  

## Transcribing

Now begin typing in your text.  Use a utf-8 (Unicode) characterset, such as the Antinoou font and keyboard.  Transcribe as you would any manuscript.  Use regular returns to create line breaks

You'll notice two "tags" already in your otherwise empty document.  These are XML tags for annotating text.  If you want to annotate something in your text, you'll wrap the relevant text in "tags".  The first tag (the open tag) is in brackets, such as `<TEI>`; the close tage has brackets and a slash, such as `</TEI>` (If you want, you can read more about [TEI XML](http://www.tei-c.org/index.xml) and the [Epidoc](https://sourceforge.net/p/epidoc/wiki/Home/) subset of XML.)

Start your transcription _inside_ the TEI tags.

You will want to encode for information about pages and columns.  
  * `<pb></pb>` The page break tags will wrap around all the text in a given page.  We use what's called an attribute to encode the page number of the manuscript.
  * `<cb></cb>` Column break tags will wrap around all the text in a given column.

When you open an angle bracket, GitDox suggests tags that are currently available. GitDox will also suggest attributes for tags. Improperly closed tags and other errors are highlighted in red.

If you need to provide other information, such as if a letter in the manuscript is large or ekthetic (hangs out in the margin), see the cheatsheet provided in the workshop or our longer [Transcription Guidelines](https://github.com/CopticScriptorium/tagger-part-of-speech/blob/master/scriptorium-transcription-guidelines.pdf) for instructions.

Below, see a sample text encoded as an example:

![screenshot of sample text](https://github.com/CopticScriptorium/NAPS2017/raw/master/images/sample-text.png)

Either while you are typing or after you are done transcribing, separate Coptic bound groups with a space or underscore.  For example:

ⲁϥⲥⲱⲧⲙ̄ⲛ̄ϭⲓⲡϫⲟⲉⲓⲥ ⇒ ⲁϥⲥⲱⲧⲙ̄_ⲛ̄ϭⲓⲡϫⲟⲉⲓⲥ_

Be sure to separate the punctuation, as well.  

ⲁϥⲥⲱⲧⲙ̄ⲛ̄ϭⲓⲡϫⲟⲉⲓⲥ· ⇒ ⲁϥⲥⲱⲧⲙ̄_ⲛ̄ϭⲓⲡϫⲟⲉⲓⲥ_·_

Put a separator between all bound groups, even if a bound group ends at the end of a line:

ⲁϥⲥⲱⲧⲙ̄     ⲁϥⲥⲱⲧⲙ̄_
ⲛ̄ϭⲓⲡϫⲟⲉⲓⲥ ⇒  ⲛ̄ϭⲓⲡϫⲟⲉⲓⲥ_·_

If you need to provide other information, such as if a letter in the manuscript is large or ekthetic (hangs out in the margin), see the cheatsheet provided in the workshop or our longer [Transcription Guidelines](https://github.com/CopticScriptorium/tagger-part-of-speech/blob/master/scriptorium-transcription-guidelines.pdf) for instructions.

When you are done typing in your text, be sure to SAVE.

## Tokenizing and Processing using the NLP

Our natural language processing tools will automatically divide bound groups into words.  This process is called tokenization.  

Gitdox can also run all the natural language processing tools that tokenize and normalize and lemmatize each word, tag for part of speech, tag for language of origin, etc.  

Click EITHER the Tokenize button OR the NLP button under the transcription box 
  * **If you Tokenize**, the tools will insert horizontal pipes between the words in every bound group
    * If you Tokenize first, you can check the word segmentation
    * After you check segmentation, run the full NLP tools by clicking the NLP button
  * **If you click the NLP button first** the tools will tokenize (segment the words) and run all the rest of the tools all at once.

When you're done with this Gitdox should send you into a spreadsheet mode.

## Editing the annotations

After you've run all the NLP tools, you should be in a spreadsheet mode.

In the spreadsheet you will see annotations in layers, very similar to the grid annotations we saw in the ANNIS database.  

Check the annotations! You probably don't know all our [part of speech abbreviations](http://copticscriptorium.org/download/tools/scriptorium_tagset_documentation.pdf), but you can tell if the NLP tools caught all the loan words, or if they expanded nomina sacra in the normalized layers.


