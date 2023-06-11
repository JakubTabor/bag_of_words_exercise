# bag_of_words_exercise
I gonna test different models to check their efficiency in pipeline
# First i load my dataset, it include review and sentiment to review, then I check shape of data, it is big dataset with two columns
# Then I change sentiment column into numbers, using lambda to apply 0 on negative sentiment and 1 to positive
# I check category imbalance, there is no imbalance, now I can import train_test_split and supply "df.review" as X and "df.Category" as y
# Now when I have train and test set ready I can import vectorizer, pipeline and RandomForestClassifier
# Then I create my pipeline and supply it into vectorizer, then RandomForestClassifier with 50 trees entropy criterion
