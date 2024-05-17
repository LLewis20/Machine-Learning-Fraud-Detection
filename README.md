# Machine Learning: Fraud Detection Model

## Introduction
Financial institutions use machine learning techniques to detect fraud, an area that has always intrigued me. The goal of this project was to develop a model capable of identifying potentially fraudulent transactions based on various features, such as transaction amount, date of birth, Unix time of the transaction, and the location of the transaction relative to the card user's residence. This project provided valuable insights into financial practices, machine learning, and software engineering, as well as the methodologies companies use to develop fraud detection models.

For detailed information, refer to the following documents, below will go over the highlights of the project:
* [RAW_DATA](RAW_DATA.md)
* [DATA](DATA.md)
* [ANALYSIS](ANALYSIS.md)
* [CONCLUSIONS](CONCLUSIONS.md)


## Project Highlights

### Objectives
- **Feature Engineering**: Extracting meaningful features from raw transaction data.
- **Model Selection**: Evaluating different machine learning models to find the best fit for fraud detection.
- **Imbalanced Dataset Handling**: Implementing techniques to manage the class imbalance in fraud detection data.

### Key Learnings
1. **Correlation vs. Causation**
   - One of the fundamental lessons learned was that correlation does not imply causation. Initially, I used gender as a feature due to its high correlation with fraud. However, removing gender from the feature set improved the model's predictive performance, highlighting the importance of careful feature selection.

2. **Accuracy Isn't Everything**
   - Many models boasted 99% accuracy on this dataset. However, given the significant class imbalance (fraud cases constitute only 0.58% of the data), a high accuracy rate can be misleading. It’s crucial to consider other metrics, such as precision, recall, and F1-score, to evaluate model performance accurately.

3. **Model Selection and Overfitting**
   - In the initial iterations, using a decision tree resulted in poor performance due to overfitting and difficulty handling the class imbalance. Switching to a random forest model proved more effective, as it managed the imbalance better and reduced overfitting.

## Conclusion

After working on this project for approximately 2-3 months, I have gained substantial knowledge in handling imbalanced datasets, exploring various machine learning models, and applying different techniques to enhance model performance. Below are some key takeaways:

- Feature selection and engineering are crucial for model success.
- Evaluation metrics beyond accuracy are essential for assessing model performance, especially with imbalanced data.
- Random forest models can provide robust solutions for imbalanced datasets compared to decision trees.

## Future Work
- **Feature Enhancement**: Further exploration of additional features to improve model accuracy.
- **Model Optimization**: Experimentation with advanced models and hyperparameter tuning.
- **Real-world Application**: Testing the model in real-world scenarios to validate its practical effectiveness.
---
