# Recommender_systems
Recommender systems are the systems that are designed to recommend things to the user based on many different factors. These systems predict the most likely product that the users are most likely to purchase and are of interest to. Companies like Netflix, Amazon, etc. use recommender systems to help their users to identify the correct product or movies for them. 
The recommender system deals with a large volume of information present by filtering the most important information based on the data provided by a user and other factors that take care of the user’s preference and interest. It finds out the match between user and item and imputes the similarities between users and items for recommendation. 
Both the users and the services provided have benefited from these kinds of systems. The quality and decision-making process has also improved through these kinds of systems.

## Why the Recommendation system?
 
Benefits users in finding items of their interest.
Help item providers in delivering their items to the right user.
Identity products that are most relevant to users.
Personalized content.
Help websites to improve user engagement.


## What is a good recommendation?

The one that is personalized (relevant to that user)
The one that is diverse (includes different user interests)
The one that doesn’t recommend the same items to users for the second time
The one that recommends available products


## Recommendation system processes data through four phases as follows-

#### Collection
Data collected can be explicit (ratings and comments on products) or implicit (page views, order history, etc.).

#### Storing
The type of data used to create recommendations can help you decide the kind of storage you should use- NoSQL database, object storage, or standard SQL database.

#### Analyzing
The recommender system finds items with similar user engagement data after analysis.

#### Filtering
This is the last step where data gets filtered to access the relevant information required to provide recommendations to the user. To enable this, you will need to choose an algorithm suiting the recommendation system.

### The following Tree-Diagram shows the recommendation systems and its major types

![image](https://user-images.githubusercontent.com/88995459/157931746-c501b883-1fce-426e-98a4-de30300e7555.png)

### Three very important types of recommender systems:

### Content-Based Filtering

It is another type of recommendation system which works on the principle of similar content. If a user is watching a movie, then the system will check about other movies of similar content or the same genre of the movie the user is watching. There are various fundamentals attributes that are used to compute the similarity while checking about similar content.

TF-IDF
Classifiers (e.g. ANN or Naive Bayes)

![image](https://user-images.githubusercontent.com/88995459/157934879-78876c6e-9a1c-441f-ba35-7c9123733a4a.png)


### Collaborative Filtering
two types of collaborative filtering
Model based and Memory based

Nearest-neighbors
Matrix Factorization
Clustering 


### Model based
Model-based recommendation systems involve building a model based on the dataset of ratings. In other words, we extract some information from the dataset, and use that as a "model" to make recommendations without having to use the complete dataset every time. 


### Memory Based
### User based (Based on similar users) (users in Rows and movies in columns - user with a vector of reviews - finding similar users using cosine)
Users who are similar to you also liked…” Products are recommended to the user based on the fact that they were purchased / liked by users who are similar to the observed user. If we say that users are similar what does that mean? For example, Jenny and Tom love sci-fi books. When a new sci-fi book appears and Jenny buys that book, since Tom also likes sci-fi books then we can recommend the book that Jenny bought. 
eg - clubbing the similar users together and recommend them what they haven't watched.

![image](https://user-images.githubusercontent.com/88995459/157935231-137373b8-47d6-4f2d-9d51-43741bb56d27.png)

### Item based (movies in Rows and user rating in columns - movies with a vector of reviews - finding similar movies using the ratings using cosine)
“Users who liked this item also liked…” If John, Robert and Jenny highly rated sci-fi books Fahrenheit 451 and The time machine, for example gave 5 stars, then when Tom buys the book Fahrenheit 451 then the book The time machine is also recommended to him because the system identified books as similar based on user ratings.
eg - clubbing the 5 star rated movies by averaging the number of reviews gave by all the users.

![image](https://user-images.githubusercontent.com/88995459/157937305-fce3cb20-f649-475d-b196-714dd652ff4b.png)



### Hybrid Recommendation Systems

In hybrid recommendation systems, products are recommended using both content-based and collaborative filtering simultaneously to suggest a broader range of products to customers. This recommendation system is up-and-coming and is said to provide more accurate recommendations than other recommender systems.

eg - Netflix  - When a new user registers in to Netflix they have to setup their own prefrences and that's how it recommend movies to the users related to the content based RS.
And as the user develops the history by watching movies for a period of time then it uses the collaborative based recommendation systen for recommending the movies.

## But how is it recommended? 

There are different scenarios where we need to check about the similarities, so there are different metrics to be used. For computing the similarity between numeric data, Euclidean distance is used, for textual data, cosine similarity is calculated and for categorical data, Jaccard similarity is computed.

#### Euclidean Distance: Distance between two points can be calculated by the equation;
![image](https://user-images.githubusercontent.com/88995459/157934365-652b90d5-3716-4d75-b336-81ec5bdff58d.png)

#### Cosine Similarity: Cosine of the angle between the two vectors of the item, vectors of A and B is calculated for imputing similarity. If the vectors are closer, then small will be the angle and large will be the cosine. 
![image](https://user-images.githubusercontent.com/88995459/157934439-dedd54d9-70e1-45a4-be7e-7adbc64c6c83.png)

#### Jaccard Similarity: Users who have rated item A and B divided by the total number of users who have rated either A or B gives us the similarity. It is used for comparing the similarity. 
![image](https://user-images.githubusercontent.com/88995459/157934528-d0fab6d5-7f73-487f-8e32-d790f9f7b8c1.png)

## Measuring metrics and test
Online A/B testing – A/B testing is the best way to do online evaluation of your recommender system.


# Another tupe of recommendation system
# Market Basket 
Market basket works on association rules which answer a question “What are the items that frequently appear together?” 
The answer to the first question can be used to recommend you products, videos, restaurants, hotels or any other content that you haven't seen previously and that have been appreciated by a group of other users.
For example, if you buy a burger and fries, you will probably want soda; or a very famous example, those who buy diapers tend also to buy beer. Association rules are independent of personal preference profiles and for mining them you need a dataset of transactions from all users.

![image](https://user-images.githubusercontent.com/88995459/157941573-db8c3957-b43a-49f0-802a-1804146e4159.png)

### Three metrics associated with market basket
### Support:
Within a dataset, i.e. a list of transactions, how many transactions contain item A, so it is just the probability of item A occurring, which we can represent as below. Statistically speaking, it is a frequent estimate of the probability.

![image](https://user-images.githubusercontent.com/88995459/157944864-ff7e2f93-be86-49c7-8864-e702a0aafb23.png)

### Confidence:
Out of the transactions that contains item A, how many also contains item B. The bigger the overlap, the greater the confidence we have that people who are buying item A also buys item B.  Statistically speaking, it is (estimated) conditional probably of item B given item A, i.e. P(B|A).

![image](https://user-images.githubusercontent.com/88995459/157945134-a46db2e3-7730-41ec-ade1-b9944f04a375.png)


### Lift:
The ratio between Confidence of A and Support B, it is less intuitive with the description, so let's try to visualize it better.

![image](https://user-images.githubusercontent.com/88995459/157945447-ef61bfc3-ef30-47aa-b5c4-b5b825747202.png)


### Choosing the metric

One way in which you can relate these concepts is to think in the following way:
Support is similar to Recall metric, a rule with high support means it has high presence on the dataset.
Confidence is similar to Precision metric, a rule with high confidence means it has high precision whenever the rule appears.
While mining association rules, you prefer the ones with high confidence (precision) over ones with high support (recall). That is why usually the minSupport may be on the lower side, even lower than 50%, while minConfidence is usually set higher, above 50% for example.
Lift is a relative strength indicator showing the association between 2 Items.
