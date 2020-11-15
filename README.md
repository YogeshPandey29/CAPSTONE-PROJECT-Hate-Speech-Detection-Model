# CAPSTONE-PROJECT-Hate-Speech-Detection-Model
# Use of Bag of Words (BoW) model and multiple classification algorithms to classify textual posts and other such contents as being hateful and provocative.

Nowadays, the prime reason for increasing intolerance, mob-lynching along with religious and caste-related conflicts are solely based upon certain posts and articles that target a specific
religion's or person's sentiments. Seeing the criticality of the situation, we thought of coming up with a better approach for classifying the content that is being published on the social media
platforms viz. Twitter, Facebook and Instagram.

So, above is the codebase that lays down the foundation of the core functionality of our project on textual content classification on social media.

# DATA CLEANING AND PREPROCESSING
For any experiment related to Natural Language Processing (NLP), the first and foremost thing to keep in mind is that the data we are going to deal with requires thorough cleaning and
preprocessing tasks. We are basically required to convert the entire dataset from textual format to a numerical format so that it could be fed into a certain classification algorithm.
Because machine learning algorithms deal with and hence understand data only in the form of numbers.

# Methods:

# 1.Stemming with Python nltk package
Stemming is the process of reducing inflection in words to their root forms such as mapping a group of words to the same stem even if the stem itself is not a valid word in the language.
Stem (root) is the part of the word to which you add inflectional (changing/deriving) affixes such as (-ed,-ize, -s,-de,mis). So stemming a word or sentence may result in words that are
not actual words. Stems are created by removing the suffixes or prefixes used with a word. A computer program or subroutine that stems word may be called a stemming program, stemming algorithm, or stemmer.

SO MUCH FOR THIS "NLTK" BUZZOWRD!!!
Natural Language Tool Kit (NLTK) is a Python library to make programs that work with natural language. It provides a user-friendly interface to datasets that are over 50 corpora and
lexical resources such as WordNet Word repository. The library can perform different operations such as tokenizing, stemming, classification, parsing, tagging, and semantic reasoning.

An example for stemmin process is shown as:
INJECT
INJECTIONS------> INJECT
INJECTED------> INJECT
INJECTING------> INJECT
INJECTION------> INJECT

# 2.Lemmatization with Python nltk package
Lemmatization, unlike Stemming, reduces the inflected words properly ensuring that the root word belongs to the language. In Lemmatization root word is called Lemma. A lemma (plural lemmas or lemmata)
is the canonical form, dictionary form, or citation form of a set of words.

For example, runs, running, ran are all forms of the word run, therefore run is the lemma of all these words. Because lemmatization returns an actual word of the language, it is used where it is necessary to get valid words.
Python NLTK provides WordNet Lemmatizer that uses the WordNet Database to lookup lemmas of words.

# FEATURE EXTRACTION
The above processes were applied for filtering the data. This process mainly aims at extracting features from the textual form of the data. The methods explained are as:

# Methods:

# Bag of Words Model
Bag of words is a Natural Language Processing technique of text modelling. In technical terms, we can say that it is a method of feature extraction with text data. This approach is a simple and flexible way of extracting features from documents.
A bag of words is a representation of text that describes the occurrence of words within a document. We just keep track of word counts and disregard the grammatical details and the word order. It is called a “bag” of words because any information
about the order or structure of words in the document is discarded. The model is only concerned with whether known words occur in the document, not where in the document.

One of the biggest problems with text is that it is messy and unstructured, and machine learning algorithms prefer structured, well defined fixed-length inputs and by using the Bag-of-Words technique we can convert variable-length texts into a fixed-length vector.
Also, at a much granular level, the machine learning models work with numerical data rather than textual data. So to be more specific, by using the bag-of-words (BoW) technique, we convert a text into its equivalent vector of numbers.

# CLASSIFICATION MODEL
Now, after filtering the data and extracting the features from the same, we build a model using one or more classification algoirthms, some of which are Decision Tree classifiers, K-nearest neighbours, Support Vector Machines (SVMs), Naive Bayes classifiers, DIET Classifiers and so on.

However, we have made use of Gaussian Naive Bayes classifiers and DIET Classifiers for intent classification as well.

# Gaussian Naive Bayes Classification Algorithm
Naive Bayes is a machine learning model that is used for large volumes of data, even if you are working with data that has millions of data records the recommended approach is Naive Bayes. It gives very good results when it comes to NLP tasks such as sentimental analysis. It is a fast
and uncomplicated classification algorithm. 
1. It is a kind of classifier that works on Bayes theorem. 
2. Prediction of membership probabilities is made for every class such as the probability of data points associated to a particular class. 
3. The class having maximum probability is appraised as the most suitable class. 
