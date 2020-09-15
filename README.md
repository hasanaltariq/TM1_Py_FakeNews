# Simple Fake News classifier



## The challenge

Classify a piece of news as REAL or FAKE.

## Assumption

If we have already labeled data, we can use natural language processing techniques to train a classifier to detect fake or real news, which is a binary classification problem in supervised machine learning.

## Data

The data comes from [Kaggle](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset) as Fake.csv and True.csv with *title*, *text*, *subject* and *date*  columns containing political and world news.

## Result
| Measurement criteria | Logistic Regression      | Decision Tree Classifier | Random Forest Classifier |
| ----- | ----- | ----- | ----- |
| Accuracy | 98.9% | 99.7% | 99.18% |

## Methodology
1. Collecting data from Kaggle
2. Cleaning & pre-processing
    - Merging data-sets (Fake.csv & True.csv)
    - Shuffling data
    - Dropping fields such as ‘title’ and ‘date’, which are not used in analysis
    - Converting text to lowercase.
    - Removing punctuations
    - Removing English Stop words using [NLTK](https://www.nltk.org/) library.
3. Exploration
    - Articles per subject
    - Target class (Fake/Real) distribution
    - Most frequent words where the text is labeled as fake and as well as real using a uni-gram approach.
4. Modelling
    - Defining function
    - Splitting data into train and test sets
    - Deploying models:
        - Logistic regression
        - Decision Tree
        - Random Forest


## Measurement Criteria
    Accuracy

## Requirements
    Python 3.8, (Jupyter Notebook), pandas-1.1.1, numpy-1.19.1, scipy-1.5.2, scikit-learn-0.23.2, matplotlib-3.3.1, nltk-3.5    

## Citation
All credit goes to original author [FavioVazquez](https://github.com/FavioVazquez/fake-news/blob/master/FakeNews.ipynb). 

## Disclaimer
We have reproduced the code for educational and learning purposes only. Original article can be found [here](https://towardsdatascience.com/detecting-fake-news-with-and-without-code-dd330ed449d9).



