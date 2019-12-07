# TF-IDF based Movie and Music search based on Amazon Reviews

This project aims to retrieve Movies as well as Music based on the TF-IDF weights of the terms in the documents and keyword supplied by the User 
## Dataset

The Dataset is a corpus of 8,765,568 reviews of 203,970 products. These products are mainly Movies and Music Albums



## Data-preprocessing
The data is a single document consisting of the following review of a movie in the following JSON format
```
{
  "overall": 5,
  "verified": true,
  "reviewTime": "08 6, 2016",
  "reviewerID": "A3HE4QW1655VB9",
  "asin": "0005419263",
  "style": {
    "Format:": " Audio CD"
  },
  "reviewerName": "bethany robinson",
  "reviewText": "My grandkids loved this and it made it easy for them to learn scripture verses I a fun way. The DVD was a great bonus.",
  "summary": "Loved it!",
  "unixReviewTime": 1470441600
}
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

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
