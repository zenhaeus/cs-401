## Deadline

Wednesday November 22th, 2017 at 11:59PM

## Important Notes

- Make sure you push on GitHub your Notebook with all the cells already evaluated
- Don't forget to add a textual description of your thought process, the assumptions you made, and the solution you plan to implement!
- Please write all your comments in English, and use meaningful variable names in your code

## Question 1: Propensity Score

In this exercise, we will put in practice [propensity score matching](http://www.stewartschultz.com/statistics/books/Design%20of%20observational%20studies.pdf) that we presented in class. We will work with the "classic" Lalonde dataset provided by Robert Lalonde in his study "[Evaluating the Econometric Evaluations of Training Programs](http://people.hbs.edu/nashraf/LaLonde_1986.pdf)" (1986). The study studied the effect of a job training program on the real earnings of an individual, a couple of years after completion of the program. Your task is to determine the effectiveness of this "treatment".

Dataset description

- treat: 1 if treated in the National Supported Work Demonstration, 0 if from the Current Population Survey
- age: age
- educ: years of education
- race: factor; black, Hispanic (hispan), or white
- married: 1 if married, 0 otherwise
- nodegree: 1 if no degree, 0 otherwise
- re74: earnings in 1974 (pretreatment)
- re75: earnings in 1975 (pretreatment)
- re78: earnings in 1978 (outcome)


#### 1. Compare the 'outcome' variable of the two groups.
What could you conclude from a superficial analysis? Support your answer with adequate plots or statistical tests and explain what could go wrong.

#### 2. Compare the features' distribution of the two groups with a proper visualization.
Are they balanced? Describe your observations, and how these can affect your previous conclusion.

#### 3. Use the propensity score to match the observations from the treatment group with the samples from the non-treatment group.
Recall that the propensity score represents the likelihood of every sample to have received the treatment, based on its features (age, demographics...). Use sklearn to train a logistic regression and get the probabilities vector:

```python
from sklearn import linear_model
logistic = linear_model.LogisticRegression()
```

Explain in details your strategy for the matching and plot the distribution of the features again. Is your sub-population more balanced? What can you conclude by comparing the 'outcome' variable in this filtered subset?

#### 4. Did your propensity-score-matching balance the features perfectly?
Can you improve the further the balancing (at the expense of the number of samples)? I.e., How many samples can you keep in the dataset by matching only people with the same 'race' feature?

#### 5. Compare the two conclusions and explain your observations.

___

## Question 2: Applied ML

We are going to build a classifier of news to directly assign them to 20 news categories. Note that the pipeline that you will build in this exercise could be of great help during your project if you plan to work with text!

1. Load the 20newsgroup dataset. It is, again, a classic dataset that can directly be loaded using sklearn ([link](http://scikit-learn.org/stable/datasets/twenty_newsgroups.html)).  
[TF-IDF](https://en.wikipedia.org/wiki/Tf%E2%80%93idf), short for term frequency–inverse document frequency, is of great help when if comes to compute textual features. Indeed, it gives more importance to terms that are more specific to the considered articles (TF) but reduces the importance of terms that are very frequent in the entire corpus (IDF). Compute TF-IDF features for every article using [TfidfVectorizer](http://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html). Then, split your dataset into a training, a testing and a validation set (10% for validation and 10% for testing). Each observation should be paired with its corresponding label (the article category).


2. Train a random forest on your training set. Try to fine-tune the parameters of your predictor on your validation set using a simple grid search on the number of estimator "n_estimators" and the max depth of the trees "max_depth". Then, display a confusion matrix of your classification pipeline. Lastly, once you assessed your model, inspect the `feature_importances_` attribute of your random forest and discuss the obtained results.


