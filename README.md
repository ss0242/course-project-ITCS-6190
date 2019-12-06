# TF-IDF based recommendation for Movies, Music albums based on Amazon Reviews


<h4>Group-member</h4>
Sagar Sharma

<h4>Project Overview </h4>
The project tries to recommend movies tiles and music albums based on the TF-IDF score of the keywords supplied by the user.
The final TF-IDF score is the addition of individual TF-IDF scores of each keyword.

<h5>Tasks involvedand approach</h5>
<br>1)transforming the Amazon reviews dataset in to appropriate format. The reviews file is a big json file consisting of item-id known as asin(in the terminologies of amazon) . This json has to be parsed and the reviews must be grouped by asin. Using the metadata.json file this asin is mapped on to the title and a saperate file is created corresponding to every title. Each file contains reviews corresponding to that title.
<br>2)the data set is loaded in the form of dataframe
<br>3)each document is assigned an id
<br>4)the document is unfolded into tokens in order to calculate Term Frequency
<br>5)tokens are extracted out and term frequecies are calculated using calculated using group by and aggregated count function
<br>6)similarly document frequencies are calculated using group by and aggregated count distinct function
<br>7)idf score is calculated according to the formula :

![Formula](formula.PNG)

<br>8)the TF-IDF score is calculated for each token by multiplying the TF with IDF
<br>9)user is asked for input
<br>10)the matching documents are extracted which contains the keywords and grouped by the title
<br>11)the TF-IDF of every keyword is added and the documents are order in the decresing order of TF-IDF scores

<h5>Final Product</h5>
<br>The final product is the Movie-recommendation system that gives results on the basis of Amazon reviews

<h5>Context and Motivation</h5>
<br>A lot of people have specific taste of movies and albums. They know what they are looking for. This system will help them get the movies they are looking for. It's similar to asking a friend for a suggestion of a movie by describing the type of movie someone is interested in.

<h5>Dataset</h5>
<br>https://nijianmo.github.io/amazon/index.html
<br>This dataset contains reviews of various amazon products ae well as thier meta-data

<h5>Frameworks used</h5>
<br>Spark-Core</br>
<br>Spark-SQL

<h5>Anyother software and packages used </h5>
<br>Scala programming language
<br>SBT: a build tool on the top of maven
<br>Eclipse for Scala IDE

<h5>Illustrative Results and Examples</h5>
<br>

![Image of Yaktocat1](1.PNG)

![Image of Yaktocat2](2.PNG)

![Image of Yaktocat3](3.PNG)

![Image of Yaktocat4](4.PNG)

![Image of Yaktocat5](5.PNG)


<h5>Performance Evalutaion</h5>
<br>
<br>Qualitatively, The Movies obtained were related to keyword supplied (if we google the movie, and read it's plot and description)
<br>Please refer the plot for the movie Chapter X live at 
<br>https://www.sparknotes.com/lit/narrative/section7/
<br>The movie is quite resonant with words such as "country" and "trust"

<h5>Tasks Accomplished</h5>
<br>Will be definated done: TF-IDF implemetation
<br>Likely to do: None </br>
<br>ideally to do: None </br>

<h5>Additional Observations</h5>
<br>COLLECT_SET is highly performace intensive
<br> SBT is an excellent tool. If you want to change the version of your scala compiler, simply change the version number. All the dependecies will be automatically resolved and code will be compiled by new version

<h5>Division of Work</h5>
<br>Sagar Sharma


<h5>Important Reference </h5>
<br>https://dzone.com/articles/calculating-tf-idf-with-apache-spark
<br>https://www.youtube.com/watch?v=qrPjAyIapFY







