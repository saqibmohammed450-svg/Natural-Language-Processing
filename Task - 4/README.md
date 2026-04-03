# 🚀 BERT IMDb Sentiment Analysis

## 📌 Project Overview
This project demonstrates how to fine-tune a BERT (Bidirectional Encoder Representations from Transformers) model for sentiment analysis using the IMDb movie review dataset.

The model classifies reviews into two categories:
- Positive
- Negative

The goal of this project is to build an NLP pipeline that can understand movie reviews and predict their sentiment accurately.

---

## 🧠 Key Features
- Fine-tuning the **BERT base uncased model**
- Binary sentiment classification (positive vs negative)
- Training on the **IMDb dataset**
- Complete NLP workflow implementation
- Achieved approximately **92% accuracy** on test data

Dataset size:
- 25,000 training reviews  
- 25,000 testing reviews  

---

## 🛠️ Technologies Used
- Python  
- PyTorch  
- Hugging Face Transformers  
- Hugging Face Datasets  
- Scikit-learn  
- Matplotlib  
- Seaborn  

---

## 🔄 Project Workflow

### 1️⃣ Data Loading
The IMDb dataset is loaded using the Hugging Face datasets library.

```python
from datasets import load_dataset
dataset = load_dataset("imdb")
```

### 2️⃣ Data Preprocessing
Basic preprocessing steps include:
- Converting text to lowercase
- Cleaning the input text
- Preparing data for tokenization

### 3️⃣ Tokenization
The BERT tokenizer converts text into tokens that the model can process.

```python
from transformers import BertTokenizer
tokenizer = BertTokenizer.from_pretrained("bert-base-uncased")
```

### 4️⃣ Model Training
The pre-trained BERT model is fine-tuned for sentiment classification.

```python
from transformers import BertForSequenceClassification
model = BertForSequenceClassification.from_pretrained("bert-base-uncased", num_labels=2)
```

### 5️⃣ Model Evaluation
The trained model is evaluated using the following metrics:

- Accuracy  
- Precision  
- Recall  
- F1 Score  
- Confusion Matrix  

---

## 📊 Results

### Accuracy
The model achieved approximately **92% accuracy** on the test dataset.

### Confusion Matrix Insights
- High number of correct predictions
- Balanced classification performance
- Low misclassification rate

---

## 📚 Key Learnings
This project helped in understanding:

- Transformer-based NLP models
- Fine-tuning pre-trained models
- Handling large text datasets
- Evaluating classification models using different metrics

---

## 🔮 Future Improvements
Possible enhancements for this project include:

- Hyperparameter tuning
- Using larger models such as **RoBERTa** or **DistilBERT**
- Deploying the model as a **web application** using Streamlit or Flask

---

## ▶️ How to Run the Project

Install the required dependencies:

```bash
pip install transformers datasets torch scikit-learn matplotlib seaborn
```

Then open the notebook:

```bash
jupyter notebook bert-imdb-sentiment-analysis.ipynb
```
