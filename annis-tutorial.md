# ANNIS Tutorial

### NOTE: The links below are live. We recommend you right-click or command-click to open links in new windows, so you can keep this window open and available.

## <a name="intro"></a>Introduction to ANNIS
Coptic Scriptorium uses the [ANNIS](http://corpus-tools.org/annis/) search and visualization tool. You can access Coptic Scriptorium's corpora in ANNIS in multiple ways:
* Go 
ly to [https://corpling.uis.georgetown.edu/annis/scriptorium](https://corpling.uis.georgetown.edu/annis/scriptorium) and run a query
* In the [Coptic online dictionary](https://corpling.uis.georgetown.edu/coptic-dictionary/), search for a word; click on the red "C" icon (the Coptic Scriptorium logo) to find instances of that lemma in ANNIS
* When browsing documents at [our portal for reading Coptic texts](http://data.copticscriptorium.org), click on the "Search ANNIS" button to query that corpus.

This tutorial will: 
  * [introduce you to our documents and corpora in ANNIS](#corpus)
  * [show you how to perform simple word searches](#search)
  * [show you how to perform more complex searches for annotations and metadata](#complex)
  * [provide you with sample queries for entities and dependency syntax](#parsing)
  * [demonstrate how to generate word frequency lists](#freq)
  * [show you how to download search/query results](#download)
  * [provide models for citing or linking to the data in your publications](#cite)

## <a name="corpus"></a>ANNIS Corpus Browser
When you arrive at [https://corpling.uis.georgetown.edu/annis/scriptorium](https://corpling.uis.georgetown.edu/annis/scriptorium), you will see the list of publicly available corpora on the lower left of your screen.  (On the right, you will see a list of sample queries for our corpora -- more on that in a minute.)

Each _corpus_ contains multiple _documents_.  
  * Each corpus has its own  _metadata_ (information about the corpus, such as all the editors/annotators who worked on the corpus, license information, the date this version of the corpus was released, etc.)
  * Each document within the corpus also has its own  _metadata_ (tite of the document, manuscript information if the text is from a manuscript, specific editors/annotators for that document, translators, the date this version of the document was released, etc.)

<a name="docinfo"></a>Look at the list of corpora:
1.  To find out more information about any corpus, click the "i" information button for that corpus.  A window will appear with:
  * a dropdown menu at the top listing all the documents in a corpus
  * on the left, _metadata_ (information about the corpus, such as annotators, translators, the date this version of the corpus was released)
  * on the right, all the annotations available for texts in this corpus.  These annotations will make more sense to you after you run a few searches.  
2.  To see a list of documents in any corpus, click the document icon :page_facing_up: for that corpus name
  * Click the "i" information button for any document for more information
  * You'll also see a list of visualizations for each document (the same visualizations available at [http://data.copticscriptorium.org](http://data.copticscriptorium.org))
  
  **:arrow_right:Try it:  What happens when you click on a link for a visualization?**
  
  ![corpus document list](https://github.com/CopticScriptorium/NAPS2017/raw/master/images/corpus-document-list.png)
  
3. You can filter the list of corpora also:
  
  **:arrow_right:Try it:  What happens when you type in "shenoute." (without the quotation marks) in the Filter box above the list of corpora?**
  
  **:arrow_right:What happens when you click the :arrows_counterclockwise: button ?**

## <a name="search"></a>Basic Search
Let's start by using the example queries provided for any given corpus.

**:arrow_right:1. Try it:  Click on the first corpus, apophthegmata.patrum.  Then play around with the sample queries or follow the following steps**
  * In the panel on the right, click on the query to search for the word "ⲁⲡⲁ".  Note:  this searches for the *normalized* word, meaning spelling variants have been normalized, diacritics removed, and missing/damaged letters reconstructed. 
  * In the search results on the right, your query term should appear in red (possibly within a Coptic bound group).
  * See the phrase "Base text" at the top of the list of results?  
    * Change the base text from "norm_group" to "norm"?  How does this change how the results appear on the screen?
    * Change the base text to "orig"?  (Note:  orig is an abbreviation for "original text" transcription)
  * You should see the same visualizations we've seen before (Analytic, Diplomatic, Normalized views).  Click on the + next to "analytic view".
    * Can you see your search result in red again?
    * This view visualizes annotations of the textual data, including  [part of speech annotations](http://copticscriptorium.org/download/tools/scriptorium_tagset_documentation.pdf), the normalized Coptic text, and an English translation.
  * What happens when you click the "i" information icon for the first search result?  What information does this give you?
  * To view ALL the annotations for any given query result, click on "annotations (grid)".
    * All annotations for that stretch of text will appear as layers below.
    * Some annotations have been manually encoded; others have been added using our [Natural Language Processing tools](http://copticscriptorium.org/tools)
    
ANNIS uses a multi-layer annotation model, where a base text appears followed by layers of annotations on that base text.  You can have any number of customized annotations.  All our paleographic and manuscript annotations (lacunae, page breaks, column breaks) follow a set of annotation and encoding standards known as the TEI-XML (the Text Encoding Initiative standards for extensible markup language).  Specifically, we use the [Epidoc subset of TEI XML](http://epidoc.sourceforge.net/), the same encoding standards that Papyri.info uses.

**:arrow_right:2. Try it:  Let's create your own simple searches for words.**
  * Modify the search we just did by typing your own favorite Coptic word where "ⲁⲡⲁ" appears.  Click "Search".  Check out the results.
  * Don't have a Coptic font installed on your computer?  Click on the little keyboard to the right of the search pane!
  * Let's now search for your favorite word in more than one corpus.  Control-click on a Mac/right-click on a PC on another corpus name in the corpus list in the lower left.  Click Search.

**:arrow_right:3. Try it:  Create simple queries for information other than words.**
  * Search for norm="ⲥⲟⲛ" in your chosen corpora
  * Now search for lemma="ⲥⲟⲛ".  What's the difference in the results?
  * Search for all Greek words in Shenoute's "I See Your Eagerness":  click on the shenoute.eagerness corpus and search for lang="Greek"
  * Now try the query for only lang in the same corpus; what's the difference?
    * Look at result number 5 -- open the annotation grid. What do you see in the lang layer?
  * Search for all words with the morpheme "ⲙⲛⲧ" in Shenoute's "Not Because a Fox Barks": click on the shenoute.fox corpus and search for morph="ⲙⲛⲧ" 
  * Search for all proper names in Warren Wells' Sahidica edition of the Gospel of Mark: click on the sahidica.mark corpus and search for pos="NPROP"
  * Play around with some simple searches.
  
**:arrow_right:4. Try it:  You can click on the History button to see all the previous queries you've run in your current ANNIS session.**

## <a name="complex"></a>Complex Searches 

You can also use [regular expressions](http://ryanstutorials.net/regular-expressions-tutorial/) and the Annis Query Language to create complex queries, searches for sequences of characters, queries for two or more annotations, etc.

**:arrow_right:5. Try it: Select a corpus, like 1 Corinthians, and try the following queries.  (Type or cut-and-paste.) What kind of results do you get?**
  * norm_group=/ⲡⲉⲧ.*/ 
  * norm=/.*ⲟⲥ/ 
  * norm=/ⲥ[ⲟⲱ]ⲧⲙ/ 

Hint:  the .* in the query syntax signals that you want to search for any character(s).

You can also search within a translation, if your corpus has a translation.  (Not all do.)

**:arrow_right:6. Try it:  Select the 1 Corinthian corpus. Try the following queries.  What's the difference?**
  ```
  translation=/.*brother.*/
  translation=/.*[Bb]rother.*/
```

You can search more than one field at the same time.  

**:arrow_right:7. Try it: Say you're interested in proper names. Select the corpus for Abraham Our Father. Compare the following queries**
  * `pos="NPROP" _o_ lang="Greek"`
  * `pos="NPROP" _o_ lang="Hebrew"`
  * `pos="NPROP" _o_ lang=/.*/`

Note:  We tag loan words for language of origin based on the oldest possible language.  To find all loan words, use the lang=/.*/ query.  

You can also add metadata to your queries.

**:arrow_right:8. Try it: Select the Abraham Our Father corpus.  Search for all the appearances of "ϣⲉⲉⲣⲉ" in the codex MONB.YA:  norm="ϣⲉⲉⲣⲉ" & meta::msName="MONB.YA"**
  * Play around with other metadata fields.  To find all words in documents edited by Rebecca Krawiec, select your corpora and search: 
```  
norm & meta::annotation=/.*Krawiec.*/
```

There's lots of fun stuff you can do with regular expressions and the ANNIS Query Language:
  * Find either circumstantial converters or focalizing converters: pos=/CCIRC|CFOC/
  * Find either form of the same verb: norm=/ⲥ[ⲟⲱ]ⲧⲙ/ 
  * Query for things following each other: To search for a copular pron sentence (a copula following a pronoun):  pos="PPERI" . pos="COP" 
  * Query for nearness:  To find "daughter" within 50 tokens after "son": norm="ϣⲏⲣⲉ" ^* norm="ϣⲉⲉⲣⲉ"

*Know your corpus and annotations when doing research.  For example, in our corpus, a compound word containing both Greek and Coptic contains a language tag only for the Greek morph within the compound. (E.g., in ⲣⲭⲣⲉⲓⲁ, only ⲭⲣⲉⲓⲁ receives the Greek tag. Hence, we use syntax for finding overlapping search fields ("o") rather than equivalent fields ("="). `lang="Greek" _=_ pos="V"` ([link](https://corpling.uis.georgetown.edu/annis/?id=dc1b4bdf-6d0e-407e-9c27-80265da4f58a))
finds all verbs that are Greek loanwords; `lang="Greek" _o_ pos="V"` ([link](https://corpling.uis.georgetown.edu/annis/?id=b40a6020-3be6-4f25-bb38-97d64ce6ac79)) finds all verbs that are Greek loanwords or are compound words with Greek loan words as part of the compound.  Compare the results in the links.* 

## <a href="parsing"></a>Parsing (Dependency Syntax) and Entities in Complex Searches

Our corpora are all parsed for dependency syntax. (See https://universaldependencies.org/cop/ for details.) That means you can search for things like all the subjects of a certain verb.

**:arrow_right:9. Let's search for verbs that have a first person subject. Copy the query into ANNIS and select your corpus/corpora: pos="V" ->dep[func="nsubj"] lemma="ⲁⲛⲟⲕ" (direct link [here](https://corpling.uis.georgetown.edu/annis/?id=afa909c2-f1f1-4c1c-b877-9c2cca4b0368))

You can even search for verbs that are Greek loanwords and that have a first person subject: lang="Greek" _o_ pos="V" ->dep[func="nsubj"] lemma="ⲁⲛⲟⲕ" (direct link [here](https://corpling.uis.georgetown.edu/annis/?id=151b6687-2beb-4c9a-b5ef-d2bad47d0dc7))

We also annotate for entities! We have ten entity classes:

![entities](https://github.com/CopticScriptorium/NAPS2022/raw/main/entities.png)

**:arrow_right:10. Try searching for [all animals in the AP](https://corpling.uis.georgetown.edu/annis/?id=3d7071de-024e-4077-972d-cb4157cbcc9d). (Query is entity="animal").

Some other sample queries:
  * entity ->head pos="ART" searches for entities headed by articles
  * entity="place" _i_ lang="Greek" searches for places containing Greek loan words in their place names


## <a name="freq"></a>Word Frequencies
ANNIS allows you to find word frequency lists for our corpora.

**:arrow_right:11. Try it: Select the shenoute.eagerness corpus.**
  * type in the following query to find all the lemmas in the corpus:  lemma
  * Click Search
  * Below the query window, you should see a button for "More."  Click on it and select "Frequency Analysis."  Click "Perform Frequency Analysis"
  * Both a chart and a list of word frequencies will appear.
  * You can see your frequencies on a [linear scale or a log scale](http://www.fool.com/foolfaq/foolfaqcharts.htm)

**:arrow_right:12. Try it: Download your frequency list by clicking the "Download as CSV" button**

You can also produce frequencies for more refined lists. **_Be sure to close the "Frequency Analysis" pane to clear your data before you start a new analysis._**

**:arrow_right:13. Try it: Create lists for loan words in our corpus.**

  **Remember: If you have just run a frequency analysis, then close the current "Frequency Analysis" pane first.  Do this (or click "new analysis") between each new frequency analysis.**
  
  A. Find the Greek loan words in the shenoute.eagerness corpus using this query: `lang="Greek" _o_ lemma`
    * Enter the query and click Search.  (If you've closed the Frequency Analysis pane, click "More" then "Frequency Analysis")
    * Delete all rows EXCEPT "lemma" (since you want the frequency of each lemma)
    * Click "Perform Frequency Analysis"
  B. Can you do the same to find _all_ loan words in the shenoute.eagerness corpus (remember to hit "new analysis" first): `lang=/.*/ _o_ lemma`
  C. Can you do the same to find all loan words that are _verbs_ (remember to hit "new analysis" first): `lang=/.*/ _o_ lemma _o_ pos="V"`
  
**BONUS question:  What do you do about corpora that contain more than one manuscript witness to the same text?**  I See Your Eagerness is one such corpus.  In some places, we have parallel manuscript witnesses to the same text.  So if you run a straight word frequency list, you'll get duplicate "hits".  For this corpus (and future versions of other corpora) we encode parallel witnesses in the metadata fields.  When you [click on the "i" information button](#docinfo) for a document, you'll see metadata fields for "witness" and "redundant".

  ![Image of metadata-witness](https://github.com/CopticScriptorium/NAPS2017/raw/master/images/metadata-witness.png)

**:arrow_right:14. Try it: Run a freqency analysis using the following query: `lang=/.*/ _o_ norm _o_ pos="V" & meta::redundant="no"`**
  * Remember to click "new analysis" to clear your old frequency data first!
  * Remember to delete rows for everything except norm when you run the analysis.
  * Are the results _different_ from the results from #3 above?

_Again:  know your corpus so you understand the numbers.  Spend some time looking at the metadata, understanding the annotation layers, and running queries to see how the annotations and textual data work.  In our corpora, we designate as redundant the withness(es) with the most damage or lacunae._

## <a name="download"></a>Download Your Results

We encourage all researcher to keep records of their research in ANNIS.  This includes queries, the corpora on which the queries are run , the version number and version date of the corpora, and the results.

There are multiple ways you can download the results of your query by clicking More > Export underneath the query panel.  Each way or format works well for a different discipline or research objective.  For most people who work with texts as philologists, historians, or religious studies scholars, we recommend using the GridExporter.  The GridExporter allows you to tell ANNIS which annotations and which metadata you want to export.

**:arrow_right:15. Try it: Run a query ([such as this one](https://corpling.uis.georgetown.edu/annis/?id=ad9787db-c777-465f-8c39-a8f1b661ebca)) and download your results.**
  * Run the query
  * Click "More" > "Export"
  * In the Exporter dropdown menu select GridExporter
  * In the "annotation keys" box, type the annotations you want to export.  Try: orig, norm, translation, pb_xml_id to export the original manuscript text, normalized text, translation (if available), and the page number of the manuscript
  * In the Parameters box type numbers=false;metakeys=title,version_n,version_date to export the document title, version number, and version date for EVERY hit in your search.
  * Click Perform Export
  * Click Download
  * You can open this text file in any text editor (such as TextEdit, Text Wrangler, etc.)
  * If you want more annotations (such as part of speech tags) add them to the "annotation keys" box; be sure to use the correct name for the annotation
  * If you want more metadata (such as the names of editors or translators of each document), add them to the "Parameters" box; be sure to use the correct name for the metadata field

## <a name="cite"></a>Citing and Linking to Your Data

When researching our corpora for a future publication, **please note the date and version number of the documents or corpora while you are conducting your research**.  (This information is in the corpus and document metadata accessed via the information button(s) for each corpus and each document within a corpus.)  We update our corpora regularly and recommend all citations include the version number and date of the resources used, as described below. (If you conducted research in the past and did not note the version and date of the corpus at that time, then please cite the date you accessed the corpus.)

We have [Citation Guidelines](http://copticscriptorium.org/citation-guidelines.html) with examples for how to cite the project, the project site, individual corpora, and individual documents in your bibliography and footnotes.  If you are using documents or queries on only one corpus, then you may cite only that corpus. 

When citing more than one corpus, we recommend citing the corpora and versions of each corpus used.

### You can save a link to a query or even to a query result.

![screenshot of linking to query](https://github.com/CopticScriptorium/NAPS2017/raw/master/images/link-to-query.png)

If you want to embed a result in a blog, webpage, or other electronic publication, you can do that too!

![screenshot of embed dialogue](https://github.com/CopticScriptorium/NAPS2017/raw/master/images/embed-viz.png)

Some DH researchers recommend providing access to your data when you publish your analysis.  You can do this in a number of ways:
  1. Link to our project's raw data on our [GitHub corpus repository](https://github.com/CopticScriptorium/corpora). 
    * Link to the version that corresponds to your data.  See our [release page](https://github.com/CopticScriptorium/corpora/releases).
    ![screenshot of GitHub corpora repository page](https://github.com/CopticScriptorium/NAPS2017/raw/master/images/github-release-page.png)
    * So, for research conducted in May 2017, link to the [April 2017 version](https://github.com/CopticScriptorium/corpora/releases/tag/v2.3.1).  For research that was conducted in January 2017, you would want to link to the [December 2016 version](https://github.com/CopticScriptorium/corpora/releases/tag/v2.2)
  2.  Download your query results using the [process described above](#download) and post them on your own site; link to them in your publication.
  3.  Link to your query on our ANNIS site.

_Important note:  the URLs for the query and result links should remain stable, but the core text data may change if we update the corpus or documents you are querying.  We update regularly to add more documents to a corpus, to add new annotations, or to make corrections.  **We encourage all researchers to download query results and cite the version number(s)and date(s) of the data used.**_
    

