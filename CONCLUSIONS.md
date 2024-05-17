# CONCLUSIONS

### Main Notebook: [Notebook](fraudDetectionProject.ipynb)

Working on this project over the span of 2-3 months provided me with extensive experience in machine learning techniques, particularly in the context of fraud detection. This period allowed me to delve deep into the intricacies of handling imbalanced datasets, experimenting with various models and techniques, and refining my overall approach. Reflecting on this journey, several key learnings stand out:

1. **Correlation vs. Causation**
   - One of the earliest lessons, both in class and in practice, was the distinction between correlation and causation. Initially, I included gender as a feature in my model due to its apparent high correlation with fraud. However, a deeper analysis revealed an interesting twist: removing gender as a feature actually improved my model's predictive performance. This was a clear reminder that correlation does not inherently imply causation in machine learning projects.

2. **Accuracy Isn't Everything**
   - Many approaches to this dataset boasted 99% accuracy. However, further research into the dataset revealed a massive class imbalance: fraud cases only accounted for 0.58% of the data. This meant that achieving 99% accuracy could still be possible even if all fraud cases were incorrectly classified. Therefore, it was crucial to consider other metrics such as precision, recall, and the confusion matrix to evaluate model performance accurately.

3. **Model Selection and Overfitting**
   - My initial attempt to use a decision tree revealed significant challenges due to the data's imbalance and the model's tendency to overfit. This experience led me to explore the random forest model, which proved to be more robust, handling the data imbalance better and exhibiting less overfitting. This shift was a pivotal point in my work, leading to more accurate and reliable predictions.

4. **Exploring Neural Networks**
   - Later, I attempted to use a neural network, but with limited exposure and understanding from class, I encountered significant challenges, including overfitting and long computational times on my school laptop. Additionally, I did not save many of the experimental notebooks, as I was primarily experimenting and did not anticipate their importance. This experience highlighted the need for more computational resources and deeper knowledge to effectively leverage neural networks for this type of project.

### Key Takeaways

- **Feature Selection**: The importance of selecting and validating features based on their actual contribution to the model’s predictive performance.
- **Evaluation Metrics**: The need to look beyond accuracy and consider precision, recall, and the confusion matrix, especially when dealing with imbalanced datasets.
- **Model Robustness**: Random forest models can offer better performance and less overfitting compared to decision trees when handling imbalanced data.
- **Resource Constraints**: Effective machine learning experimentation requires sufficient computational resources and a thorough understanding of the models being used.

### Future Work

For future improvements, I plan to introduce cross-validation into my model, as recommended in the Rochester thesis. Additionally, I aim to deepen my understanding of neural networks and explore their application in fraud detection projects. Addressing the computational constraints and gaining more practical experience with neural networks will be crucial for these future endeavors.

---
