### Description
This project focuses on classifying the sentiment expressed in tweets about the presidential candidates Barack Obama and Mitt Romney into positive, negative, or neutral categories. The main objective is to build and evaluate models for sentiment analysis using various machine learning techniques.


### Introduction
The aim of this project is to classify tweets related to the 2012 presidential candidates Barack Obama and Mitt Romney into three sentiment categories: positive, negative, and neutral. The training data includes labeled tweets, while the test data without labels is used for model evaluation.

### Techniques Used
We explored several techniques for sentiment analysis, focusing on data preprocessing, feature representation, and model selection. The following techniques were used:
- **Data Preprocessing**: Normalizing case, removing punctuation, URLs, and lemmatizing text.
- **Feature Representation**: TF-IDF and Word2Vec.
- **Models**: Naive Bayes, Logistic Regression, Support Vector Machines (SVM), Multilayer Perceptron (MLP), and Random Forest.

### Data Preprocessing
1. **Loading Data**: Data was loaded from an Excel file containing tweets about Obama and Romney, labeled for sentiment.
2. **Preprocessing Steps**:
    - Case normalization
    - Punctuation removal
    - URL removal
    - Lemmatization

### Model Evaluation
Several models were evaluated based on their performance:
- **Naive Bayes**: Accuracy of 54.22%
- **Logistic Regression**: Accuracy of 56.8%
- **SVM**: Accuracy of 58.22% in the first run, 59.62% in the second run
- **MLP**: Accuracy of 53.8%
- **Random Forest**: Accuracy of 57.4%

### Results
SVM emerged as the top-performing model with an accuracy of 59.62% in the second run. TF-IDF was used for feature representation due to its effectiveness in transforming text data into numerical vectors while preventing overfitting.

### Lessons Learned
1. **Model Selection**: SVM was the top performer.
2. **Evaluation Metrics**: Balancing precision and recall is crucial for imbalanced datasets.
3. **Feature Representation**: TF-IDF and Word2Vec complement each other.
4. **Hyperparameter Tuning**: Further exploration could enhance performance.
5. **Data Quality**: The quality and representativeness of the training data significantly affect model performance.
6. **Scalability**: Consider model scalability when dealing with large datasets.

### Future Work
To enhance accuracy, consider:
- **Deep Learning Architectures**: Exploring models like RNNs or BERT.
- **Transfer Learning**: Utilizing pre-trained models like GPT or BERT for sentiment analysis.
