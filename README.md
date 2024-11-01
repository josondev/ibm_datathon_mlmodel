
# AI vs Human Text Classification

This project focuses on building a machine learning model to classify whether a given piece of text is generated by AI or written by a human. By leveraging Natural Language Processing (NLP) techniques and machine learning models, the project aims to create a robust classifier that can differentiate between these two types of text.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Data Preprocessing](#data-preprocessing)
- [Model Training](#model-training)
- [Evaluation](#evaluation)
- [Results](#results)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
With the increasing use of AI-generated content, distinguishing between AI-generated and human-written text has become an important task in various fields like content moderation, plagiarism detection, and fake news identification. This project applies machine learning models like LightGBM, Logistic Regression, and others to classify text as either AI-generated or human-generated.

## Features
- Preprocessing and vectorizing text data using **TfidfVectorizer**.
- Implementation of multiple classifiers including:
  - **LightGBM** (Light Gradient Boosting Machine)
  - XGBoost
- Hyperparameter tuning using **GridSearchCV** to find the best-performing model.
- Cross-validation and model evaluation using various metrics like accuracy and classification report.
- Handling imbalanced datasets using class weighting techniques.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/josondev/ai-vs-human-text-classification.git
   cd ai-vs-human-text-classification
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Data Preprocessing
The dataset used consists of pre-labeled text samples classified as either **AI-generated** or **Human-written**. The key preprocessing steps include:
- Cleaning and tokenizing the text data.
- Vectorizing the text using **TfidfVectorizer** with a maximum of 5000 features.
- Splitting the dataset into training and testing sets with an 80/20 split.
  
## Model Training
Multiple machine learning models are trained on the preprocessed data:
1. **LightGBM**: A fast, efficient gradient boosting framework used for text classification.
2. **XGBoost**: Additional boosting models to compare performance.

Key techniques:
- Hyperparameter tuning using **GridSearchCV** to optimize model performance.
- Cross-validation to ensure generalization across the data.
- Early stopping for LightGBM to prevent overfitting.

## Evaluation
The models are evaluated on various metrics:
- **Accuracy**: The proportion of correct predictions.
- **Classification Report**: Precision, recall, F1-score, and support metrics for each class.
- **Confusion Matrix**: To visualize the performance of the classifier.

Example code for evaluation:
```python
accuracy = accuracy_score(y_test, y_pred)
print("Accuracy: ", accuracy)
print(classification_report(y_test, y_pred))
```

## Results
After training and evaluation, the project compares the performance of various classifiers. The **LightGBM** model, after hyperparameter tuning and early stopping, provides the best accuracy and is chosen as the final model.

- Best Accuracy: **X.XX**
- Confusion Matrix: Available in the report

## Future Work
- Extend the model to handle more types of AI-generated text from different sources.
- Fine-tune the model further using more advanced hyperparameter optimization techniques.
- Explore deep learning-based approaches (e.g., LSTM, transformers) for better performance on larger datasets.

## Contributing
Feel free to fork this repository, make enhancements, and submit a pull request. Contributions are welcome!

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to customize it based on your specific details or additional features!
