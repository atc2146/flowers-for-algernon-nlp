# Flowers for Algernon

:books: :cherry_blossom: :mouse2:  
Natural Language Processing and textual analysis on the novel Flowers for Algernon.

## Introduction

Flowers for Algernon  is a 1966 novel written by Daniel Keyes that tells the story of Charlie Gordon, a 32-year-old man with an IQ of 68.  Charlie undergoes an operation to increase his intelligence, and the operation is a success, with his IQ eventually reaching 185.  However, the effects are temporarily, and Charlie begins to regress to his original state.<sup>[[1]](#myfootnote1)</sup>

Charlie's progression throughout the novel is analyzed using natural language processing.

## Tableau Dashboard

Find the [Tableau Dashboard here](https://public.tableau.com/app/profile/atcwy/viz/FlowersforAlgernon-TextAnalysisandNLP/Main "Tableau Public | Flowers for Algernon - NLP and Textual Analysis").  

## Methodology
<!--For a more detailed write-up, see [here](Writeup/).  -->

 * Words were tokenized using NLTK's `word_tokenize` function and using a custom regex tokenization.
 * Misspellings were checked using the [Brown](https://en.wikipedia.org/wiki/Brown_Corpus) corpus, [Words](https://en.wikipedia.org/wiki/Words_(Unix)) corpus, and a manually generated list of valid words.  Overall, this contained 261822 'valid' words.
 * Sentiment Analysis was completed using a Lexicon based approach by referencing the [NRC Emotion Leixcon](https://saifmohammad.com/WebPages/NRC-Emotion-Lexicon.htm).
 * Various reading scores such as the [Flesch-Kincaid readability tests](https://en.wikipedia.org/wiki/Flesch%E2%80%93Kincaid_readability_tests) were calculated using the Python package `textstat`.
 * [CSV's](Data/) were exported to build the visualization in Tableau.
   * [CSV](Data/Flowers%20for%20Algernon%20-%20Chapter%20summaries.csv) with chapter level summaries of reading scores and sentiment.
   * [CSV](Data/Flowers%20for%20Algernon%20-%20All%20word%20tokens.csv) containing a list of all words, whether it was misspelled, its context, etc...

See Jupyter Notebooks for full details.

## Data

Data is taken from the novel under fair use for the purpose of education and commentary uses only.  

Exported data used to build the Tableau visualization can be found [here](Data/).


## References, Resources, and Inspirations

 * <a name="myfootnote1">[1]</a> https://en.wikipedia.org/wiki/Flowers_for_Algernon
 * Python Packages: [Pandas](https://pandas.pydata.org/), [NumPy](https://numpy.org/), [NLTK](https://www.nltk.org/), [SpellChecker](https://pypi.org/project/pyspellchecker/), [TextStat](https://pypi.org/project/textstat/)
 * [NRC Emotion Leixcon](https://saifmohammad.com/WebPages/NRC-Emotion-Lexicon.htm)
 * Tableau Dashboard Inspirations: [The Eponymous Phrase](https://public.tableau.com/profile/skybjohnson#!/vizhome/TheEponymousPhrase/TheEponymousPhrase), [Sentiment Analysis w/ Quentin Tarantino](https://public.tableau.com/profile/tim.lafferty#!/vizhome/SentimentAnalysiswQuentinTarantino/Basic)

## Extensions and To-do
 * Finish  write-up
 * Remove unnecessary data (to speed up Tableau)
 * Generate random text using a trigram (or other n-gram) model
