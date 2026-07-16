# TidyMail: An Email Segregator 

**Created by:** Jivin Nayak

## 📌 Project Overview
TidyMail is a Machine Learning and Natural Language Processing (NLP) project built to accurately classify emails as either spam or non-spam. The primary goal of this project is to differentiate between regular emails and junk mail with an accuracy of over 90%. 

**View the Code:** [Google Colab Notebook](https://drive.google.com/file/d/10N8kVpsOjLW6TH8-KL1kU3JtMJOvkCaf/view?usp=sharing)

## 🛠️ Technologies Used
* **Python** * **Scikit-learn:** For the core Machine Learning frameworks and model training.
* **NLTK & SpaCy:** As the main Natural Language Processing toolkits for text interpretation.
* **Pandas & NumPy:** For dataset manipulation, handling arrays, and numerical operations.
* **Matplotlib:** For visualizing the data and model decision boundaries.

## ⚙️ The Approach & Methodology
1. **Dataset:** Used a real-world email dataset (CSV file) to train the models.
2. **Preprocessing:** * Processed the raw email text using **Tokenization** to extract words while removing HTML tags and punctuation.
   * Applied **Lemmatization** to reduce words to their base forms (e.g., changing "running" to "run").
3. **Feature Engineering:** * Analyzed the top 50 most frequently occurring tokens for both spam and non-spam emails.
   * Created a custom `spam_tokens` list filled with common words that trigger spam filters.
4. **Data Formatting:** * Split the dataset into 80% training data and 20% testing data.
   * Converted the text emails into numerical representations (count vectors).
   * Scaled the data using `MinMaxScaler` to ensure all feature values fell evenly between 0 and 1.

## 🧠 Models Evaluated
To find the most accurate classifier, four different models were trained and evaluated:
1. Logistic Regression
2. Random Forest Classifier
3. Support Vector Classifier (SVC)
4. Multinomial Naive Bayes

## 📊 Results
After comparing all models, the **Random Forest Classifier** performed the best. 
* **Accuracy:** 95%
* **Precision & Recall:** 95%

Data visualization was also used to map out the decision boundaries of these models using PCA-reduced data.

## 🚧 Challenges & Obstacles
During development, the original model encountered an **overfitting** issue. Because the `spam_tokens` list was too selective, the model performed well on the training data but failed to accurately classify clear spam emails that weren't in the original dataset. 

To fix this, the `spam_tokens` list was adjusted. This prevented overfitting and ensured the model was ready for real-world, generalized scenarios.

## 🚀 Future Scope & Next Steps
* Integrate this machine learning model into a real-world mail system.
* Learn about email system APIs to fetch and send live emails.
* Deploy the trained classification model as a live microservice or API endpoint.
