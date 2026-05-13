# Financial-Sentiment-Analysis
Financial Sentiment Analysis Dataset from kaggle
-Link Dataset https://www.kaggle.com/datasets/ankurzing/sentiment-analysis-for-financial-news\
## 📖 Description
This project focuses on analyzing the sentiment of financial texts or tweets. It classifies the text into three distinct categories:
* **Positive**: Mapped to label `0`
* **Negative**: Mapped to label `1`
* **Neutral**: Mapped to label `2`

## ✨ Key Features
* **Data Preprocessing**: Cleans text data using Regular Expressions (removing special characters and numbers), converts text to lowercase, and removes stop words using the NLTK library.
* **Feature Extraction**: Converts text into numerical vectors using TF-IDF (`TfidfVectorizer`), limited to a maximum of 5,000 features to reduce noise.
* **Handling Class Imbalance**: Addresses the imbalanced dataset issue by applying SMOTE (Synthetic Minority Over-sampling Technique).
* **Machine Learning Models**: Trains and compares the performance of three different models: 
  * Multinomial Naive Bayes
  * Logistic Regression (Hyperparameter tuning via `GridSearchCV` to find the best `C` value)
  * Random Forest Classifier
* **Evaluation & Error Analysis**: Evaluates models using Accuracy, Precision, Recall, F1-score, and Confusion Matrix. It also includes an error analysis section that extracts the top 5 misclassified texts to identify the model's weaknesses.
* **Data Visualization**: Visualizes label distribution using a Pie Chart, displays the Logistic Regression's Confusion Matrix via a Heatmap, and highlights the most frequent words in each class using a Word Cloud.

## 🛠️ Technologies & Tools
* **Language**: Python 3
* **Data Manipulation**: Pandas, NumPy
* **Machine Learning & NLP**: Scikit-learn, Imbalanced-learn (SMOTE), NLTK
* **Data Visualization**: Matplotlib, Seaborn, WordCloud
