# machine-learning-f23-project
Repo for all project documents


### Data set
* https://www.kaggle.com/datasets/kartik2112/fraud-detection


## Part A: Initial Exploration
* The pros of this data set is that it is very clean and clear on what things are, also I did not have to add or remove any data.
* The cons of the data is that it is very unbalanced, like I talked about in the initial exploration notebook, out of the 1,296,675 data entries, 1,289,169 of them are not fraud while 7,506 entries are fraud, that is 0.578402452% of the entries. 
* To fix this I am thinking about splitting the data 50/50 so that half is fraud and the other half is not fraud, the other is using a different data set from kaggle.


## Part B: Linear Regression
* The lineaer regression notebook did not go well since the data is so unbalanced, another problem is that many of the string features need to be changed to a int like the state feature.
* The best score that I could get was 5.061638465396934% which is really low, this is after trying different combos with the features, I now that I want to use amt for one of my features because it had the largest correlation coefficient out of all of the features, but it only had a .02.
* I need to figure out a way to train a model that has very unbalanced data like this data set, change the set to be 50/50, or use my other data set on kaggle.
* I'm going to talk to Dr.Hoot about what would be the best for me to do, I'm hoping that there is another method to use for data sets for this.


## Part E: Classification
* The decision tree model gave me a 100% accuracy score which would seem good, but there is some not right if the model is getting that many correct. I believe that the 'Not Fraud' features are completely overfitted. I think that I should go get another dataset to see if the model truely works or if something else is happening with the data.


## Milestone 3
* First I had to scale the data, after I did that I used KMeans and graphed the clusters that I had, the clusters show different parts of the data. The red cluster is scattered and has some outliers, the green and blue clusters have the same type of spread and shows that there might be a pattern to it. With this graph we can guess that anything that isn't within the area of the three clusters are more than likely the fraud data entries.

* Tried a NN and got an accuracy of a 99.8%, but my model never converged. If I had to guess what the model go wrong were the few fraud cases since there is a very small inaccuracy.

* UPDATE is converged within the last 2 minutes of the assinment being open
