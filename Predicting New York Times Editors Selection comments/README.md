# Predicting New York Times "Editor's Selection" comments

### Abstract

The following notebook has the goal to predict the "Editor's Selection" comments of the open articles from the [New York Times](https://www.nytimes.com/) webpage.

These are the steps to achieve this goal:
- **Import data**
- **Pre-processing features**
- **Processing comments texts**
- **Modeling and testing**
- **Discussing results**

The imported dataset contains data from January 2017 until May 2017 and from January 2018 until May 2018, related to articles and comments from NY Times. After importing, some features are pre-selected to be used in the model. The features are treated and some new features are created. The *editorsSelection* represents if the comment is an "Editor's Selection" or not, and will be the target.

The feature **commentBody** represents the comment itself. I separate it and process the text using NLP techniques. I do **Count Vectorization**, **Stemming** and **TF-IDF** to vectorize and prepare the comments for use in the model.

For classification, the **SVM** algorithm is the chosen one. It will be evaluated using three measures: **Accuracy**, **AUROC**, and **F1-Score**.

After that, the SVM will be reparameterized with **Grid Search**.

Finally, the results will be discussed and some future works will be recommended.

>Some codes and ideas were inspired by [Aashita Kesarwani Predicting NYT's pick notebook](https://www.kaggle.com/aashita/predicting-nyt-s-pick/notebook)