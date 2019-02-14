# Unidad-2-Actividad-1

## Métricas de evaluación de modelos de clasificación

Using the metrics studied previously evaluate and compare models' performance and implement following:

1. Try to build a classifier for the MNIST data set that achieves over 97% accuracy on the test set. Hint: The KneighborsClassifier works quite well for the task, you just need to find good hyperparameter values (try a grid search on the weights and n_neighbors hyperparameters.)
2. Write a function that can shift an MNIST image in any direction (left, right, up, or down) by one pixel. Then, for each image in the trainin set, create four shifted copies (one per direction) and add them to the training set. Finally, train your best model on this expanded training set and measure its accuracy on the test set. You should observe that your model performs even better now!. This technique of artificially growing the training set is called *data augmentation* or *training set expansion*.
3. Tackle the **Titanic** dataset. A great place to start is on [Kaggle](https://www.kaggle.com/c/titanic).
4. Build a spam classifier:
  * Download examples of spam and ham from Apache SpamAssassin's [public dataset](https://spamassassin.apache.org/old/publiccorpus/)
  * Unzip the dataset and familiarize yourself with the data format.
  * Split the dataset into a training set and a test set.
  * Write a data preparation pipeline to convert each email into a feature vector. Your prepariation pipeline should transform an email into a (sparse) vector indicating the presence or absence of each possible word. For example, if all emails only ever contain four words, "Hello", "how", "are" "you", then the email "Hello youe hello hello you" would be converted into a vector [1, 0, 0, 1] (meaning ["Hello", is present, "how" is abstent, "are" is absent, "you" is present]), or [3, 0, 0, 2] if your prefer to count the number of occurrences of each word.
  * You may want to add hyperparameters to your preparataion pipeline to control whether or not to strip off email headers, convert each email to lowercase, remove punctuation, replace all URLs with "URL", replace all number with "NUMBER" or even perform stemming.
  * Then try out several classifiers and see if you can build a great spam classifier, with both high recall and high precision.
  * Emulate a email form using a web application, and use your model to classify new incoming emails.
