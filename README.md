# Fraud Detection Model: Machine Learning Final Project

### Introduction

* Some things that have always interested me are the ways in which financial institutions use Machine Learning techniques to detect fraud. The goal of this project was to create a model that identifies potentially fraudulent transactions based on various features, such as transaction amount, date of birth, Unix time of the transaction, and the location of the transaction compared to the card user's residence. Throughout this project, I have learned not only about financial practices within machine learning and software engineering but also about how companies develop fraud detection models.
    * [RAW_DATA](RAW_DATA.md)
    * [DATA](DATA.md)
    * [ANALYSIS](ANALYSIS.md)
    * [CONCLUSIONS](CONCLUSIONS.md)


### Conclusion
* After working on the project for approximately 2-3 months, I have gained knowledge about managing imbalanced datasets, explored various models within machine learning, and learned how to apply different techniques to enhance my model. Here are some of the biggest things I have learned from this project:
    * Correlation doesn't equal causation - one of the first things we were taught in class was how just because something has a correlation doesn't mean that that is the reason something happens. When I was first trying to find features for this model I was using gender as one of my features since it seemed to have a pretty high correlation. Later when I would try other features when I would get rid of gender my model would predict fraud transactions better.
    * Accuracy isn't everything - when looking how others have approached this dataset many would claim that they had 99% accuracy with their models, after further research into the dataset you realize that there is a massive imbalance with the fraud and not fraud classes. The fraud cases only account for 0.58% of the data, so even if you got all the fraud cases incorrect you could still have a 99% accuracy which is not a good thing.
    * When using different models I would try using a decision tree for the first interation which would not do well with the imbalance of data and would easily overfit.
    * I decided to use a random forest model for this project, the random forest model seems to have a better time with the imbalance of data and does overfit as often as a decsion tree.