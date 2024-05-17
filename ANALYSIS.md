# ANALYSIS

### Intro
* When I first started this project, I noticed that many people on Kaggle threads were using decision trees and claiming to achieve 99% accuracy, which made me think I was set for this project. However, upon reviewing their code, I identified a problem: none of them included a confusion matrix in their posts and solely focused on accuracy. The issue with this approach is that in a dataset with 1.2 million entries, where only 7,500 are fraudulent (about 0.58% of the total entries), it's possible to get all the fraud entries wrong and still achieve 99% accuracy. This led me to consider other metrics such as precision and recall, and to pay closer attention to the confusion matrix for my models.

### Decision Tree
* I decided to still try a decision tree to see if I could effectively classify fraud cases while maintaining high accuracy. However, I encountered problems since decision trees are prone to overfitting much of the time. Due to the massive imbalance in the data, the decision tree struggled with classifying fraud versus non-fraud cases. My model correctly classified fraud cases only 31% of the time, which was a major issue.

![Decision Tree Matrix](dtmatrix.png)

### Random Forest
* I also experimented with a random forest model for this project, inspired by a student's thesis from the Rochester Institute of Technology on machine learning for fraud detection. The thesis discussed the use of random forest models with cross-validation, so I decided to focus exclusively on a random forest model. After training my new model, I saw a significant improvement in its ability to classify the fraud class. The accuracy increased from 31% with the decision tree to approximately 65% with the random forest model. My next step involved adjusting the model's threshold to see if it would yield further improvements. After several adjustments, the best outcome I achieved was the model correctly classifying 71% of the fraud entries.

![Random Forest Report](classreport.png)
![Random Forest Matrix](rfmatrix.png)

### Challenges / Limitations / Improvements
* As I mentioned earlier, I was adjusting the threshold of the model's predictions. If the threshold was set too high, the model would classify fraud entries as non-fraud. Conversely, setting the threshold too low resulted in some non-fraud entries being misclassified as fraud. Approaching this project from the perspective of a financial institution, I preferred a model that leans on the side of labeling non-fraud entries as fraud, rather than the opposite. This is because the risk associated with mislabeling fraud as a normal transaction is significantly higher.

* I believe a key limitation of this project is my limited experience in handling datasets with such significant imbalances, combined with my lack of professional experience. Fraud detection, which I perceive as a more expert-oriented area, presents unique challenges that require specialized knowledge and skills.

* For future improvements, I am considering introducing cross-validation into my model. This approach was utilized in the paper I read from Rochester, where they applied cross-validation with their random forest models. Additionally, I would like to deepen my understanding of Neural Networks and explore their application in projects like this. However, my primary concern with Neural Networks is their tendency to overfit more than Random Forest models. In the Neural Network I experimented with, I implemented dropout to mitigate overfitting, but even then, the Random Forest model still outperformed the Neural Network.
