---
title: Machine Learning
nav: true
---

# Machine Learning (ML)

ML is the application of algorithms and statistical modeling to allow computers to "learn" from data to do a task (often overlapping or used interchangeably with Artificial Intelligence / AI).

ML tasks are broadly separated into *supervised* or *unsupervised* learning.
Supervised learning tasks typically involve feeding the algorithm a labeled training data set which is used to build a model that can then classify unknown items, making inferences based on what it knows. 
Unsupervised learning tasks involve feeding unlabeled data to an algorithm that can identify patterns and clustering in the grouping. 

The ability to learn from data is changing the approach to many computational tasks, such as OCR or NLP, putting the focus on curating training data sets rather than developing new software (see Andrej Karpathy, [Software 2.0](https://medium.com/@karpathy/software-2-0-a64152b37c35), 2017).
However, computational techniques can also challenge our expertise in DH, stretching even stats experts ability to evaluate the validity of complex models (for fun, [spurious correlations](http://www.tylervigen.com/spurious-correlations){:target="blank"}).

## Natural Language Processing (NLP)

NLP is a family of techniques to analyze unstructured language data found in everyday speech and writing. 

Historically, it wasn't based in ML, but relied on manually identifying rules and patterns in human speech that could be parsed by code.
For example, take a minute to play with [ELIZA](https://www.masswerk.at/elizabot/eliza.html) (1966), an electronic psychologist based in early NLP pattern matching.

The web has provided an explosion of unstructured text, making NLP a huge business as enterprise seeks to extract information from social media or create chat-bots to minimize labor costs.
Typical tasks involve chunking/stemming, part-of-speech tagging, named entity recognition (NER), classification, and sentiment analysis.
Speech recognition, OCR , and text-to-speech are also considered NLP tasks.

Demos:

- IBM Watson [Natural Language Understanding](https://www.ibm.com/watson/services/natural-language-understanding/) (API trained on web content)
    - [VPOD sentiment analysis](https://uidaholib.github.io/poemchoice/index.html) (poetry sent to IBM NLU API for sentiment analysis)
- Text-processing [NLTK demos](http://text-processing.com/demo/) (free API, based on [Python NLTK](https://www.nltk.org/))
- [Book Visualizations Sandbox](https://observablehq.com/@bmschmidt/book-visualizations-sandbox?htid=pst.000061166424) (Text and sentiment analysis with Hathi books. Shared on the Observable platform, a web-based code notebook for javascript)

-----------------

## Topic Modeling

{% capture text %}
- Text mining that allows the user to identify patterns in a corpus of texts
    - **Input**: texts 
    - **Output**: several lists of words that appear in the texts
- Groups words across the corpus into clusters of words, or "topics" based on those words' similarity and dissimilarity
- Sometimes topics are easy to identify (for example: "navy, ship, captain"). Other times they're more ambiguous.
- Usually works best on large bodies of text
- Some familiarity with your text is important
    - See ["When you have a MALLET, everything looks like a nail"](http://sappingattention.blogspot.com/2012/11/when-you-have-mallet-everything-looks.html) for an example of what can happen when you're not familiar with your data or the tools you're using
{% endcapture %}
{% include card.md text=text header="A few basics of topic modeling" %}

Topic modeling is an example of **unsupervised machine learning**
- You have input data but don't know the output variables
- Used as a process to find meaningful structure and groupings in your data

**Latent Dirichlet Allocation (LDA)**
- A type of topic modeling
- Matt Jockers's Topic Modeling "Fable" ([LDA Buffet](http://www.matthewjockers.net/2011/09/29/the-lda-buffet-is-now-open-or-latent-dirichlet-allocation-for-english-majors/))

**What to do with your output?**
- [Mining the Dispatch](http://dsl.richmond.edu/dispatch/pages/intro){:target='_blank'}

{% capture text %}
**Topic Modeling Activity** 
- Topic modeling in-browser with [jsLDA](https://mimno.infosci.cornell.edu/jsLDA/)
    - Explore a sample corpus of <a href="../data/austen.zip">Jane Austen texts</a>
        - Click on the link above, unzip the downloaded file. Inside you'll find a text file of Austen's corpus, along with a stopword list. Upload both of these files to jsLDA. 
    - You can also try it with your own corpus. Just make sure your text file is formated correctly:
        - One document per line, with each document consisting of `[doc ID] [tab] [label] [tab] [text...]`
        - If you need to get rid of line breaks in your text, try the following regex:
            - Find `([\n\r])+`
            - Replace a space
{% endcapture %}
{% include alert.md text=text color=secondary %}

Don't be afraid to fail or get bad results. Topic modeling is exploratory, and sometimes you have to play around with it before you know what settings work best for your project.

-----------------

## Exploring big data

**Google Books [Ngram Viewer](https://books.google.com/ngrams){:target='_blank'}**

<div class="p-3">
<div style="position:relative;height:0;padding-bottom:56.25%"><iframe src="https://embed.ted.com/talks/lang/en/what_we_learned_from_5_million_books" width="854" height="480" style="position:absolute;left:0;top:0;width:100%;height:100%" frameborder="0" scrolling="no" allowfullscreen></iframe></div>
</div>

-----------------

## Fun with Text Generators

Unsupervised deep learning neural network models?
Can you collaborate with a machine algorithm?

- [Sunspring](https://youtu.be/LY7x2Ihqjmc) (Oscar Sharp, Ross Goodwin, Thomas Middleditch, 2016)
- Janelle Shane, [Darth Vader's recipe](https://twitter.com/JanelleCShane/status/1125963320823934976) ([aiweirdness blog](https://aiweirdness.com/))
- [Train a GPT-2 Text-Generating Model w/ GPU For Free](https://colab.research.google.com/drive/1VLG8e7YSEwypxU-noRNhsv5dW4NfTGce), google colab
- [GPT-2 code](https://github.com/openai/gpt-2), recent press [1](https://openai.com/blog/better-language-models/) [2](https://towardsdatascience.com/openais-gpt-2-the-model-the-hype-and-the-controversy-1109f4bfd5e8), [3](https://www.vox.com/2019/5/15/18623134/openai-language-ai-gpt2-poetry-try-it), etc...
- [Talk to Transformer](https://talktotransformer.com/) (ask it a question, like `Q: What is Digital Humanities?`)
