# ISIS Tweet Classification

## Project Overview

This project focuses on classifying tweets to determine their association with ISIS supporters. The dataset contains about 140,000 tweets, with approximately 17,000 labeled as ISIS-related. The goal is to develop a Python function that outputs a probability score (0 to 1) indicating the likelihood that a tweet is pro-ISIS.

## Files Included

- `Tweets.csv`: Contains the dataset with around 140,000 tweets, including 17,000 labeled as ISIS-related.
- `ISIS_Tweet_Classification.ipynb`: Jupyter Notebook demonstrating data preprocessing, feature extraction, model training, evaluation, and probability scoring.

## Methodology

1. **Data Preprocessing**: Clean and normalize tweet text.
2. **Feature Extraction**: Convert text to numerical features using TF-IDF.
3. **Model Training**: Train classification models on the data.
4. **Model Evaluation**: Evaluate models using precision, recall, and F1-score.
5. **Probability Scoring**: Develop a function to output the pro-ISIS probability score for tweets.

## Conclusion

The project aimed to classify tweets as pro-ISIS or non-ISIS. The models showed varying precision, with `RandomForestRegressor` and `GradientBoostingRegressor` achieving high precision but lower recall, while `XGBRegressor` also showed high precision with lower recall.

### Insights

- **Class Imbalance**: The imbalance between ISIS-related and non-ISIS tweets led to high precision but often lower recall. This imbalance can bias performance metrics and affect the detection of minority class instances.

### Recommendations

1. **Advanced Resampling Techniques**: Use methods like ADASYN or hybrid resampling to better address class imbalance.
2. **Model Ensembling**: Apply techniques such as stacking or boosting to combine multiple models for improved performance.
3. **Contextual Embeddings**: Utilize models like BERT or GPT to capture the sequential nature of text and improve classification accuracy.

### Model Suitability

The current models treat text as a "bag of words," which does not account for the order or context of words. This limitation affects the model's ability to understand the nuanced meaning of tweets.

**Future Work**:
- **Recurrent Neural Networks (RNNs)**: For capturing sequential data.
- **Long Short-Term Memory (LSTM) Networks**: To handle long-term dependencies in text.
- **Transformer Models**: Such as BERT or GPT, to understand word order and context, which can significantly enhance classification performance.

### Critique and Reflection

- **Workflow**: Initial baseline performance should be established before applying resampling techniques.
- **Evaluation**: Incorporate additional metrics like ROC-AUC for a comprehensive assessment.

Overall, while the models provided a functional classification tool, incorporating techniques that understand text sequence and context, and addressing class imbalance more effectively, will enhance performance.
