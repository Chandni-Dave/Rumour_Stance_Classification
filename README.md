## Rumour Stance Classification ##

Rumour stance classification is the task of determining if each tweet discussing particular rumour is supporting, denying, querying or
just commenting on the rumour, has been of substantial interest. False claims and rumours affect people’s perceptions of events and
their behavior, sometimes in harmful ways. Previous work regarding stance classification has treated tweets as an independent unit.
The objective is to accurately determine the support each tweet expresses and ultimately help to aggregate views to determine the
veracity of the rumour. This task uses eight Twitter datasets, collected from different breaking news and aims at evaluating the stance
of each tweets belonging to a rumour using non-sequential classifiers.

#### Dataset -

* The PHEME dataset consists of nine events which corresponds to different breaking news stories,
which has tweet level annotations for stance.Dataset contains tree-structured conversations, which are intitiated by a
source tweet for a rumour and nested replies that discuss the source tweet and the rumour itself(replies). Dataset is available publicly and can be downloaded from link below.
Dataset link - <https://figshare.com/articles/PHEME_rumour_scheme_dataset_journalism_use_case/2068650>

* Dataset folder contains **pheme-dataset** which is the training data, **test-data** which is the test data, **test_label.json** which contains testing labels and **train_data.json** contains training labels.

* The dataset contains **badwords.txt** which is list of bad-words which is used to find feature in Data.ipynb

#### Requirements to run the code -
* Python version - 3.6 or above
* Libraries needed - 
  * NLTK Version 3.5
  * Gensim Version 3.5 or above
  * TextBlob Version 0.15
  * NumPy Version 1.11
  * scikit-learn version 0.21
  
 #### Steps to run the code -
 1. Pre-trained model *GoogleNews-vectors-negative300* is used for word2Vec features. GoogleNews-vectors-negative300 is required by Data.ipynb file. This is available at https://github.com/mmihaltz/word2vec-GoogleNews-vectors. After downloading, place it in the Code folder.
 2. Run Data.ipynb to read the dataset and generate features for each tweet. The feature data and labels will be stored in **train.pkl** and **test.pkl** for the classifers.
 3. For Naive Baiyes classifier, run the **NB_Classifier.ipynb** file.
 4. For SVM, LR and Random Forest results, run the **RandomForest_LR_SVM.ipynb** file.
