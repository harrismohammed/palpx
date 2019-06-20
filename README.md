# Palpx-Task

## <b><i>This is a task provided by Palpx as part of their Recruitment Process :</i></b>

### <b>1) Problem statement :</b>

To Build a question answering system for a text article. Which returns the answer to the question with a confidence score.

### <b>2) Input :</b>

Input 1. Link to an English wikipedia article page
Example: article: “https://en.wikipedia.org/wiki/R2-D2”

Input 2. Question in natural language related to that article content.
Example: “When was R2-D2 inducted into the Robot Hall of Fame?”

### <b>3) Output :</b>

Extract and show the particular sentence containing the answer to the
question with a confidence score.
Example: “R2-D2 was inducted into the Robot Hall of Fame in 2003.”, score: 0.8

### <b>4) Code Format :</b>

- I have used Jupyter Notebook to exhibit my work.

### <b>5) Requirements & Packages :</b>

A. Python 3.7 

B. NLTK = Natural Language processing Toolkit. It can be used for a wide range of Text Processing use cases. I have used it to detect Sentences from my article.

> $ pip install nltk

After installing nltk, you need to download 'punkt'; which enables you to tokenize :

> import nltk

> nltk.download('punkt')

C. BEAUTIFUL SOUP = This library helps us to get the HTML structure of the page that we want to work with. We can then, use its functions to access specific elements and extract relevant information.

> $ pip install beautifulsoup4

D. FUZZY WUZZY = It uses Levenshtein Distance to calculate the similarities between two given sentences.

> $ pip install fuzzywuzzy

E. REGULAR EXPRESSIONS = I have used RE to preprocess Data by removing HTML Tags from Data.

> $ pip install regex

F. TQDM = It is used to print progress in a script.

> $ pip install tqdm

G. SPACY = spaCy is a free open-source library for Natural Language Processing in Python. It features NER, POS tagging, dependency parsing, word vectors and more.

> $ pip install -U spacy

-Required to download English Language model.

> $ python -m spacy download en

### <b>6) Understanding Tags :</b>

- <"a"> The links are described in this tag, of the webpage that gets loaded on the click. Link is mentioned in its property href.
- <"p"> When some information is to be displayed on the webpage as a block of text, this tag is used. Each such tag appears as its own paragraph.
- <"table">  Tables are displayed in HTML with the help of this tag, where data is displayed in cells formed by intersection of rows and columns.

### <b>7) Procedure :</b>

- Download and import all the necessary libraries and packages.
- Enter the link for the webpage that needs to be scraped in html format.
- Print the HTTP status code. If it returns 200,then the request has succeeded.
- Strip all Html tags and carry out preprocessing to obtain the clean article text and store each sentence in a list.
- Match the words in the question from the list of sentences of the article. 
- Extract sentences before and after containing majority of the words from the question to obtain the context.
- Using spacy find the subject, object and the root word of the sentence. This is done inorder to understand on what topic the question revolves around.
- Find the sentence from the context containing the subject, object and the root word. As this sentence is supposed to contain the answer.

### <b>8) Future Possible modifications :</b>

- Word embeddings can be applied. This helps build a very robust model.
- Googles open source pretrained model BERT can be attached to build a question answer model.