# Spam-Classifier

Here, I will implement a spam classifier for the mailing system using Naive Bayes in Python.
As the name suggests, what spam classifier basically does is is that it will look for words that could potentially make an email as spam. For eg: An email containg the word "FREE!"
"Get Free movie tickets!!" Now this can be treated as spam.
So the spam classifier will make use of the Bayes theorem by which it will calculate the probability of an email being spam or ham(non-spam) by taking the word 'free' into consideration, as given below:
P(spam|free) = P(spam)P(free|spam) / P(free)
We can calculate this probability for any word by P(spam|word) for every word that we encounter in a spam email and later on multiply these probabilities.
Here, it is assumed that the presence of different words is independent of each other, hence called Naive.

**PROCESS**

Since it is naive, I'll be using sklearn.naive_bayes to train the spam classifier. Most of the code is just reading the data and loading it into the Pandas dataframe. The ML classification bit is just few lines of code.

**CountVectorizer**: Function in scikit which can operate on lots of words at once.

**MultinomialNB**: is going to do all the heavy work on Naive Bayes.

The DataFrame contains two folders as spam and ham(non-spam) and can be found here.

(You can also make your own DataFrame or append to the existing dataframe)
