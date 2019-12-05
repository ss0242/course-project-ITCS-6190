# TF-IDF based recommendation for Movies, Music albums based on Amazon Reviews


<h4>Group-member</h4>
Sagar Sharma

<h4>Project Overview </h4>
The project tries to recommend movies tiles and music albums based on the TF-IDF score of the keywords supplied by the user.
The final TF-IDF score is the addition of individual TF-IDF scores of each keyword.

<h5>Tasks involved</h5>
<br>1)transforming the Amazon reviews dataset in to appropriate format. The reviews file is a big json file consisting of item-id known as asin(in the terminologies of amazon) . This json has to be parsed and the reviews must be grouped by asin. Using the metadata.json file this asin is mapped on to the title and a saperate file is created corresponding to every title. Each file contains reviews corresponding to that title.
<br>2)the data set is loaded in the form of dataframe
<br>3)each document is assigned an id
<br>4)each document is preprocessed to remove stop words (using built-in function) and a few more words have been added to serve the purpose of the system
<br>5)tokens are extracted out and term frequecies are calculated using calculated using group by and aggregated count function
<br>6)similarly document frequencies are calculated using group by and aggregated count distinct function
<br>7)idf score is calculated according to the formula :

![Formula](formula.PNG)

8)the TF-IDF score is calculated for each token by multiplying the TF with IDF
9)user is asked for input
10)the matching documents are extracted which contains the keywords and grouped by the title
11)the TF-IDF of every keyword is added and the documents are order in the decresing order of TF-IDF scores
