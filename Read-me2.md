# TF-IDF based Movie and Music search based on Amazon Reviews

This project aims to retrieve Movies as well as Music based on the TF-IDF weights of the terms in the documents and keyword supplied by the User 
## Dataset

The Dataset is a corpus of 8,765,568 reviews of 203,970 products. These products are mainly Movies and Music Albums.
The dataset can be found at:
https://nijianmo.github.io/amazon/index.html


## Data-preprocessing
The data is a single document consisting of the following review of a movie in the following JSON format
```

```
The movies and music albums are identified by an unique id ```asin```

There is another document corpus consisting of metadata about the movies and music albums.


```
{
  "category": [
    "Movies & TV",
    "Movies"
  ],
  "title": "Chapter X Live [VHS]",
  "rank": "1,007,436inMoviesTV(",
  "also_view": [
    "B005IGVTDS",
    "B00LVCK6VO",
    "B000002HQW",
    "B0006L0LM0",
    "B00092ZLXA",
    "B00SINZ0NS",
    "B000005IRR",
    "B000005IRU"
  ],
  "main_cat": "Movies & TV",
  "asin": "000503860X"
}

```
This document corpus of reviews of Movies and Music albums is broken down into individual documents whose name of the file is the name of the Movie or Music Album and content of the document are the reviews corresponding to the Movie or Music Albums. So after preprocessing of data, we have 203,970 number of documents.

A small portion of the data preprocessing part is implemented under the project folder SimpleApps.7z 





## TF-IDF calculation

The formula for TF-IDF is as follows:

![Formula](formula.PNG)


The project folder all-new implements the process of calculating TF-IDF as well as searches the document based on TF-IDF weights.


1)the documents are taken into the data frame and are assigned document ID
2)All the punctuation, stop-words and a few common words as as love, climax, happy, ending is removed
3)the original dataframe is transformed to get a new dataframe with 
  document_ID and term as the columns of the dataframe
4)the term frequency, document frequency and inverse document frequencies are calculated using aggregate functions
5)terms and their respective TF-IDF score are stored in cache

 
## Document Searcher
1)the user supplied keywords are taken into a set
2)set of matching documents are retrieved which contains the user supplied keywords
3) The total TF-IDF score is calculated with the help of the formula
```
TF-IDF(Document) = TF-IDF(Keyword1) + TF-IDF(Keyword2) +TF-IDF(Keyword3) +TF-IDF(Keywordn)
```

5)The top 5 documents with the decreasing score of TF-IDF is shown along with the file-path(treat file path as URL of the resource)

## Illustrative Examples

1)
![Image of Yaktocat1](1.PNG)


2)
![Image of Yaktocat2](2.PNG)



3)
![Image of Yaktocat3](3.PNG)



4)
![Image of Yaktocat4](4.PNG)



5)
![Image of Yaktocat5](5.PNG)



## License
[MIT](https://choosealicense.com/licenses/mit/)
