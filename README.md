# bag_of_words_exercise
I gonna test different models to check their efficiency in pipeline
# First i load my dataset, it include review and sentiment to review, then I check shape of data, it is big dataset with two columns
# Then I change sentiment column into numbers, using lambda to apply 0 on negative sentiment and 1 to positive
# I check category imbalance, there is no imbalance, now I can import train_test_split and supply "df.review" as X and "df.Category" as y
# Now when I have train and test set ready I can import vectorizer, pipeline and RandomForestClassifier
# Then I create my pipeline and supply it into vectorizer, then RandomForestClassifier with 50 trees entropy criterion
# Next I train my data and prepare y_pred making predictions on my X_test, then i print classification report
# "random_forest" works pretty good, decision trees helps overcomes high variance and overfitting of high dimensional
# It also use feature importance of words for better classifying the categories, he managed good on this dataset
# Now I gonna check performance of "KNeighborsClassifier", so I put in into my pipeline, setting "n_neighbors to 10" and "metric will be euclidean"
# I train it, then prepare y_pred and print classification_report, we can see that score is low in both classes 
# The reason is that KNN doesn't work well with high dimensional data and we work here on bag of words, so KNN have low perforamnce
# Main reason of low performance is cost to calculate distance which is expensive in that case
# Then I gonna check "MultinomialNB", so I put it into my pipeline, then I train it and get y_pred which I put into classification_report
# "MultinomialNB" work as good as "random_forest", but computation cost was lower and I get my results faster
# Advantages are easy calculation of probabilities for the words in corpus(Bag of words) and storing them in contigency table
