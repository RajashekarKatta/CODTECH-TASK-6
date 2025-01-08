Name:RAJASHEKAR KATTA Company:CODETECH IT SOLUTIONS ID: CT08DBJ Domain:Python Programming

Data Loading:
The script loads a CSV file (spam.csv) that contains two main columns: one for the label (ham or spam) and another for the email content (messages).
Error handling is included to catch issues like missing files or parsing errors.

2. Data Preprocessing:
The data is cleaned by selecting only the relevant columns (v1 for the label and v2 for the message).
The label column is mapped to binary values (0 for ham and 1 for spam) to prepare it for model training.

3. Data Splitting:
The dataset is split into training and testing sets using an 80-20 split, where 80% of the data is used for training the model, and 20% is held out for testing.

4. Text Vectorization:
The CountVectorizer from scikit-learn is used to convert the text data into a numerical format using the bag-of-words model.
This creates a matrix where each row represents a document (email), and each column represents a unique word in the entire dataset.

5. Model Training:
A Naive Bayes classifier (specifically the MultinomialNB variant) is trained on the vectorized data.
Naive Bayes is a popular algorithm for text classification tasks like spam detection because of its simplicity and effectiveness in handling word probabilities.

6. Model Evaluation:
After training the model, predictions are made on the test data.
Three evaluation metrics are displayed:

7 Accuracy: The proportion of correct predictions made by the model.
Confusion Matrix: A table showing the counts of true positives, true negatives, false positives, and false negatives, providing insight into the types of errors the model is making.
Classification Report: A summary of precision, recall, and F1-score for both classes (spam and ham).

8. Confusion Matrix Visualization:
A heatmap of the confusion matrix is generated using Matplotlib and Seaborn to visually assess the performance of the model in terms of true and false predictions.
