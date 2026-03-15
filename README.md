# 🎬 Sentiment Analysis on IMDB Reviews using RNN

A deep learning based **Natural Language Processing (NLP)** project that classifies IMDB movie reviews as **Positive 😊 or Negative 😞** using a **Recurrent Neural Network (RNN)** built with **PyTorch**.

This project demonstrates a complete **end-to-end NLP pipeline** including text preprocessing, TF-IDF feature extraction, and deep learning model training.

---

# 🚀 Project Overview

The goal of this project is to build a machine learning system capable of predicting the **sentiment of movie reviews**.

The pipeline includes:

📥 Data Loading  
🧹 Text Preprocessing  
🔢 Feature Engineering (TF-IDF)  
🧠 Deep Learning Model (RNN)  
📊 Training & Evaluation  

---

# 📂 Dataset

Dataset used: **IMDB Movie Reviews Dataset**

📊 **Dataset Statistics**

- Total Reviews: **50,000**
- Positive Reviews: **25,000**
- Negative Reviews: **25,000**
- Balanced dataset

Each review contains:

📝 Movie review text  
🏷️ Sentiment label (positive / negative)

---

# 🧹 NLP Preprocessing Pipeline

Several preprocessing techniques were applied to clean the raw text data.

### 1️⃣ Lowercasing
All text reviews were converted to lowercase to maintain consistency.

### 2️⃣ URL Removal
Removed URLs using **regular expressions**.

### 3️⃣ HTML Tag Removal
HTML tags were cleaned using regex.

### 4️⃣ Punctuation Removal
Removed special characters and punctuation symbols.

### 5️⃣ Tokenization
Used **NLTK word_tokenize()** to split sentences into words.

### 6️⃣ Stopword Removal
Removed common English stopwords using **NLTK stopwords corpus**.

### 7️⃣ Stemming
Reduced words to their root form using **Porter Stemmer**.

Example:

running → run  
playing → play  

---

# 🔢 Feature Engineering

Text data cannot be directly used by neural networks, so we convert it into numerical vectors.

### TF-IDF Vectorization

Used **TF-IDF (Term Frequency – Inverse Document Frequency)** to represent reviews numerically.

Parameter used:

max_features = 5000

Each review becomes a **5000-dimensional feature vector** representing important words.

---

# 🧠 Model Architecture

A **Recurrent Neural Network (RNN)** was implemented using **PyTorch**.

### Architecture

Input Layer  
⬇  
RNN Layer  
⬇  
Fully Connected Layer  
⬇  
Sigmoid Activation  
⬇  
Binary Output (Positive / Negative)

### Model Configuration

Hidden Size: **128**  
Number of Layers: **1**  
Loss Function: **Binary Cross Entropy (BCELoss)**  
Optimizer: **Adam**  
Batch Size: **64**  
Epochs: **10**

---

# ⚙️ Training Pipeline

Dataset split:

📚 **Training Set:** 80%  
🧪 **Testing Set:** 20%

PyTorch **TensorDataset** and **DataLoader** were used for efficient batch processing.

### Training Steps

1️⃣ Forward pass through the RNN  
2️⃣ Compute loss using BCELoss  
3️⃣ Perform backpropagation  
4️⃣ Update weights using Adam optimizer  

---

# 📊 Model Evaluation

Model performance was evaluated using **classification accuracy** on the test dataset.

Prediction rule:

sigmoid(output) > 0.5 → Positive  
sigmoid(output) ≤ 0.5 → Negative  

---

# 🛠️ Tech Stack

🐍 Python  
🔥 PyTorch  
📊 Scikit-learn  
📚 NLTK  
🐼 Pandas  
🔢 NumPy  

---

# 📁 Project Structure

sentiment-analysis-rnn

│  
├── IMDB Dataset.csv  
├── sentiment_rnn.py  
├── README.md  
└── requirements.txt  

---

# 💻 Installation

Clone the repository:

git clone https://github.com/rattanvansh/Sentiment-Analysis-using-RNN.git

---

Install dependencies:

pip install -r requirements.txt

---

# ▶️ Run the Project

python sentiment_rnn.py

---

# 🔮 Future Improvements

🚀 Replace TF-IDF with **Word Embeddings (Word2Vec / GloVe)**  
🚀 Use **LSTM or GRU instead of vanilla RNN**  
🚀 Implement **Transformer / BERT based sentiment analysis**  
🚀 Add metrics like **Precision, Recall, F1-Score**

---

# 👨‍💻 Author

**Vansh Rattan**  
AI/ML Engineering Student
Srm Institute of Science and Technology
