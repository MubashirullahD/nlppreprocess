# NLPPREPROCESS

NLPPREPROCESS is a preprocessing package for NLP task. The main objective of the package is to reduce time consumed for preprocessing by using ready made functions.
Processing for tweets can be all done with a single function call.

# Requirements

 * Python 3.4 or higher

# Installation


 ### Manually via GIT
 ```
 $ git clone git://github.com/MubashirullahD/nlppreprocess
 $ cd nlppreprocess
 $ python setup.py install
 ```

# Functionalities
1. Original nlppreprocess
2. Dedicated for tweets
   • Lower-casing
   
   • Normalizing URLs
   
   • Normalizing Tags and email addresses
   
   • Normalizing Numbers
   
   • Normalizing Dollars
   
   • Normalize punctuation
   
   • Removal of composition
   
   • Removal of punctuation
   
   • Word Stemming (Porter Stemmer)

# Usage
```
>>> from nlppreprocess import NLP
>>> obj = NLP()
```
 ## Parameters
 ```
 >>> obj = NLP(
        replace_words=True,
        remove_stopwords=True,
        remove_numbers=True,
        remove_HTML_tags=True,
        remove_punctation=True,
        lemmatize=False,
        lemmatize_method='wordnet'
       )
 ```
 ## Using with Pandas Library
 ```
 >>> dataFrame['text'] = dataFrame['text].apply(obj.process)
 >>> dataFrame['text'] = obj.processTweet(dataFrame['text])

 ```
 ## Using with plain textx
 ```
 >>> print(obj.process("Pass a text here"))
 ```
 ## Add more stopwords
 ```
 >>> obj = NLP()
 >>> obj.add_stopword(['this', 'and this'])
 ```
 ## Add more replace words
 ```
 >>> obj = NLP()
 >>> obj.add_replacement([this="by this", this="by this"])
 ```
