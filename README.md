# PDF_URL_SUMMARIZER

This Python script is an automatic text summarization tool using TF-IDF (Term Frequency-Inverse Document Frequency). It takes an input text from different sources (manual input, text file, PDF, or Wikipedia page) and generates a concise summary based on the importance of words in the document.

#1. Importing Required Libraries
The script imports several libraries:

sys, math, re: For general operations.

bs4, urllib.request: For web scraping Wikipedia pages.

PyPDF2: For extracting text from PDF files.

nltk (Natural Language Toolkit) & spacy: For Natural Language Processing (NLP).

nltk.stem.WordNetLemmatizer: Used to normalize words (lemmatization).

spacy.load('en_core_web_sm'): Loads the English NLP model.

#2. Reading Input Text
The script allows input in four ways:

Manual input: Direct user input.
Text file: Reads and extracts content from a .txt file.
PDF file: Reads text from a PDF using PyPDF2.
Wikipedia page: Scrapes text from a given Wikipedia URL.

#3. Text Preprocessing
Tokenization: Splits text into sentences and words using spacy.
Lemmatization: Converts words to their base form using WordNetLemmatizer.
Stopwords Removal: Ignores common words like "is", "the", etc

#5. Sentence Scoring
Sentences are assigned a score based on the average TF-IDF score of words in them.
The threshold is calculated as the average of all sentence scores

#6. Generating the Summary
Sentences with a score above 1.3 times the threshold are included in the final summary.
The summarized text is printed along with the word count of the original and summarized content.
