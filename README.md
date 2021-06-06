COMP6200 Data Science Portfolio 
===


### Name : ARTH MUKESHBHAI PATEL (46117253)
### Portfolio Projects

#### Portfolio 1 Analysis of CSV data for cycling

- **Dataset** : Strava (https://strava.com/) and GoldenCheetah (https://www.goldencheetah.org/)

- **Dataset description** : Strava is online social network site for cycling and other sports.  This data is a log of every ride since the start of 2018 and contains summary data like the distance and average speed.  It was exported using the script `scripts/stravaget.py` which uses the stravalib module to read data. The second dataset comes from an application called GoldenCheetah which provides some analytics services over ride data.  This has some of the same fields but adds a lot of analysis of the power, speed and heart rate data in each ride.  This data overlaps with the Strava data but doesn't include all of the same rides. 
 some of the more important fields in the data. Capitalised fields come from the GoldenCheetah data
while lowercase_fields come from Strava. There are many cases where fields are duplicated and in this case the values
should be the same, although there is room for variation as the algorithm used to calculate them could be different
in each case. 

 
- **Analysis** : 
  
  * converting dataframe index using tz_localize and tz_convert to UTC and Combine two data frame using join (innner join).
  * performing the cleaning task remove null values and other unwanted values from columns.
  * Check some key variables: time, distance, average speed, average power, TSS. Are they normally distributed or Skewed.
  * Explore the relationships between the following variables. Are any of them corrolated with each other and explained relationships.
  * Explore the values of NP for races vs the overall set of rides to see if this hypothesis is supported (using graphs and summary statistics) and check races more challenging than rides in general or not.
  * Generate a plot that summarises the number of km ridden each month over the period of the data. Overlay this with the sum of the Training Stress Score and the average of the Average Speed to generate an overall summary of activity.
  * Check What leads to more kudos. Indicate which rides are more popular the relationship between the main variables and kudos.
  * summary graph but one that shows the activity over a given month, with the sum of the values for each day of the month shown. So, if there are two rides on a given day, the graph should show the sum of the distances etc for these rides.


#### Portfolio 2 Analysing COVID-19 Data

- **Dataset** :  the global spread of COVID-19

- **Dataset description** : The first step is to get a copy of the raw data. The data is being made available by Johns Hopkins University in this GitHub repository. We're interestd in the global confirmed cases dataset but you can also get data on deaths and recovered cases. You can either download a copy of the data into your project or just read it from the URL. The advantage of reading the URL is that you'll get live updates, but this might make it harder for you to repeat your experiments if the data changes. Also, you would be making new requests for data every time you ran your worksheet putting load on the server.

- **Analysis** : 

  * World map of covid-19 spread
  * Select a number of countries and plot their data on the same graph to reproduce visualisation.
  * Visualisation shows the data for different countries aligned from the time that they have 100 confirmed cases.
  * Normalisation by Population
  * Predictive Model
  * Select a country with a clear exponential curve and build a linear regression model to predict the log of the number of case.
  
#### Portfolio 3 Predicting the Genre of Books from Summaries

- **Dataset** :  CMU Book Summaries Corpus

- **Dataset description** : Use a set of book summaries from the [CMU Book Summaries Corpus](http://www.cs.cmu.edu/~dbamman/booksummaries.html) in this experiment.  This contains a large number of summaries (16,559) and includes meta-data about the genre of the books taken from Freebase.  Each book can have more than one genre and there are 227 genres listed in total.  To simplify the problem of genre prediction we will select a small number of target genres that occur frequently in the collection and select the books with these genre labels.  This will give us one genre label per book. 

- **Analysis** : 

  * import data from the .txt file and filter the data so that only our target genre labels are included and we assign each text to just one of the genre labels. It's possible that one text could be labelled with two of these labels (eg. Science Fiction and Fantasy) but we will just assign one of those here.
  * Clean the book summaries using regular expression and NLTK. NTLK used for tokenization and removing stopword from the summaries.using regular expression remove numeric value and some unwanted characters.
  * Apply term frequency–inverse document frequency(TF-IDF) for numerical statistic that is intended to reflect how important a word is to a document in a collection or corpus.
  * Apply model Logistic Regression and k-nearest neighbors
  * Compare Accuracy score of model with other model.