**Fine-Grained Topic Categorization of BBC News Articles using Supervised Classification Model**

**Project Overview**
This project focuses on automatically classifying BBC news articles into specific categories using supervised machine learning techniques combined with Natural Language Processing (NLP).
With the rapid growth of digital news platforms, manually organizing news articles into topics becomes inefficient. This project demonstrates how machine learning can be used to automatically understand and categorize news content based on its textual information.
The system processes BBC news articles, converts them into numerical representations using GloVe word embeddings, and then applies multiple supervised learning algorithms to predict the most relevant topic for each article.
The goal of the project is to build an intelligent system that can **analyze news text and accurately assign it to the correct category, improving content organization and retrieval.

**Dataset:**
The project uses the BBC News Dataset, which contains labeled news articles belonging to different categories.
Categories in the Dataset
The articles are classified into five major topics:
* Business
* Entertainment
* Politics
* Sport
* Technology
Each article contains textual content and a corresponding category label.

**Project Workflow**
The entire project follows a structured machine learning pipeline:
1. Dataset Loading
2. Data Cleaning and Text Preprocessing
3. Exploratory Data Analysis (EDA)
4. Feature Extraction using GloVe Embeddings
5. Model Training
6. Model Evaluation
7. Result Visualization

**Data Preprocessing**
Raw text data cannot be directly used by machine learning models. Therefore, several preprocessing steps are applied.

**Text Cleaning Steps**
* Convert text to lowercase
* Remove punctuation and special characters
* Tokenization (splitting text into words)
* Stopword removal
* Lemmatization (converting words to base form)
These steps help reduce noise in the dataset and improve model performance.
The cleaned text is then stored in a new column for further processing.

**Feature Extraction using GloVe**
To convert text into numerical vectors, this project uses GloVe (Global Vectors for Word Representation).
GloVe is a widely used word embedding technique that captures semantic relationships between words by representing them in a continuous vector space.

**Why GloVe?**
* Captures semantic meaning of words
* Pretrained on large corpora
* Produces meaningful word representations
* Improves NLP model performance

**Process Used**
1. Load pretrained GloVe 100-dimensional vectors
2. Convert each word into its embedding vector
3. Compute the average vector of all words in an article
4. Use this vector as the numerical representation of the document
This transforms each news article into a 100-dimensional feature vector.

**Exploratory Data Analysis (EDA)**
Before training the models, exploratory analysis was performed to better understand the dataset.

**EDA Techniques Used**
* Word frequency analysis
* Word clouds
* Token distribution
* Part-of-speech tagging
* N-gram analysis
These visualizations help identify common words and patterns in different news categories.

**Machine Learning Models**
Multiple supervised learning models were trained and evaluated to compare their performance.

**1. Decision Tree Classifier**
A tree-based model that splits data based on feature values to make classification decisions.

Advantages:
* Easy to interpret
* Handles nonlinear relationships

**2. Naive Bayes (GaussianNB)**
A probabilistic classifier based on Bayes theorem with the assumption of feature independence.

Advantages:
* Fast training
* Works well for text classification

**3. K-Nearest Neighbors (KNN)**
This algorithm classifies a data point based on the categories of its nearest neighbors.

Advantages:
* Simple and intuitive
* Works well with vector representations

**4. Radius Neighbors Classifier**
This algorithm classifies samples based on neighbors within a fixed radius distance instead of a fixed number of neighbors.

Advantages:
* Flexible neighbor selection
* Handles varying data densities

**Model Evaluation**
To measure performance, multiple evaluation metrics were used:
* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix
* ROC-AUC Curves
These metrics provide a complete understanding of how well the models classify news articles.

**Results:**
Each trained model was evaluated on the test dataset and their performance metrics were recorded.
The models were compared based on:
* Classification accuracy
* Precision
* Recall
* F1-score
Results and visualizations were stored in the results directory for analysis.

**Technologies Used**

Programming Language
* Python
  
Libraries
* NumPy
* Pandas
* Scikit-learn
* NLTK
* Matplotlib
* Seaborn
* WordCloud
* Joblib

NLP Techniques
* Tokenization
* Lemmatization
* Stopword Removal
* Word Embeddings (GloVe)

**How to Run the Project**

**Step 1**
Clone the repository

```bash
git clone https://github.com/yourusername/bbc-news-classification.git
```

**Step 2**
Install required libraries

```bash
pip install numpy pandas scikit-learn nltk matplotlib seaborn wordcloud joblib
```

**Step 3**
Download GloVe embeddings and place them in the project folder.
Example:
```
glove.6B.100d.txt
```

**Step 4**
Run the notebook

```bash
BBC.ipynb
```

**Applications**
This project can be applied in many real-world systems:
* News recommendation systems
* Automated news categorization
* Content filtering platforms
* Search engine indexing
* Digital journalism platforms

**Future Improvements**
Several improvements can enhance the system:
* Use deep learning models such as LSTM or BERT
* Train custom word embeddings
* Perform hyperparameter tuning
* Deploy as a web application
* Build a real-time news classification API

**Conclusion**

This project demonstrates how Natural Language Processing and supervised machine learning can be combined to build an automated news classification system.
By using GloVe word embeddings and multiple classifiers, the system can effectively understand textual information and categorize news articles into fine-grained topics. This approach improves the efficiency of managing and organizing large volumes of textual data.
