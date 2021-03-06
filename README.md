# spam-filter
Naive Bayes spam filter using Apache Spark

This is a spam filter that uses a Naive Bayes algorithm with a Bernoulli model to classify emails as spam or not. It leverages Apache Spark to distribute the tasks.

The project is built using the CSDMC2010_SPAM dataset (http://csmining.org/index.php/spam-email-datasets-.html). Similar to the referred dataset, the project assumes a folder containing all the emails that will be used (for training and testing), and a separate files containing a list of labels.

The project uses Spark to distribute two tasks- 
1. Extracting features from the inputted emails.
2. Extracting labels for each email from label file.

Once the dataset has been collected, the model is trained using a random 60% split, and then is tested for accuracy against the rest of the dataset. 


Major outstanding tasks:
1. The feature set has been hardcoded for now. The featres should be stored in a way that they can be updated easily, and more importantly- the features have to be updated dynamically by the algorithm. NLTK (http://www.nltk.org/book/ch06.html) provides some insights in how this can be implemented.

2. Convert this into a web service.

3. Add a testing framework and add test coverage. 