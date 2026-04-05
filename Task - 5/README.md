# 🧠 POS Tagging and Chunking with BERT (Token Classification)

## 📌 Project Summary

This project demonstrates how Transformer-based models can be used for token classification tasks in Natural Language Processing.

The system performs two important linguistic tasks:

- Part-of-Speech (POS) Tagging  
- Chunking (Phrase Identification)

A DistilBERT model is fine-tuned to recognize grammatical roles of words and identify phrase boundaries within sentences.

---

## 🎯 Project Goal

The main purpose of this project is to:

- Explore token classification using Transformer models
- Implement sequence labeling tasks such as POS tagging and chunk detection
- Address issues like subword tokenization and label mapping
- Measure performance using sequence evaluation metrics

---

## 🛠️ Tools & Technologies

The project was developed using the following technologies:

- Python  
- Hugging Face Transformers  
- PyTorch  
- NLTK (for accessing the dataset)  
- SeqEval (evaluation library)  
- Google Colab  

---

## 📂 Dataset Information

The project uses the **CoNLL-2000 dataset**, accessed through NLTK.

Each record in the dataset contains:

- A word/token  
- Its POS tag  
- Its chunk tag  

Example:

```
Confidence   NN   B-NP
in           IN   B-PP
the          DT   B-NP
```

---

## ⚙️ Workflow / Pipeline

Raw Dataset → Tokenization → Label Alignment → Model Training → Model Evaluation → Prediction → Task Comparison

---

## 🔍 Data Preparation

Before training the model, the dataset goes through several preprocessing steps:

- Tokenization using the BERT tokenizer  
- Aligning POS and chunk labels with tokenized words  
- Handling special cases such as:
  - Subword tokens using `-100`
  - Special tokens
  - Padding and truncation

These steps ensure that labels correctly correspond to each token.

---

## 🤖 Model Details

- Model Used: `distilbert-base-uncased`  
- Task: Token Classification  
- Library: `AutoModelForTokenClassification` from Hugging Face Transformers  

DistilBERT provides a lighter and faster version of BERT while maintaining strong performance.

---

## 🚀 Training Configuration

- Epochs: 3  
- Batch Size: 16  
- Learning Rate: 2e-5  
- Optimizer: AdamW (default Hugging Face optimizer)

---

## 📊 Model Performance

### POS Tagging Results

- Precision: 0.9650  
- Recall: 0.9670  
- F1 Score: 0.9660  
- Accuracy: 0.9754  

The model achieved strong results using a Transformer-based approach.

---

## 🧪 Example Prediction

**Input Sentence**

```
John works at Google in California
```

**Predicted POS Tags**

```
John        → NNP
works       → VBZ
Google      → NNP
California  → NNP
```

---

## 🔄 POS Tagging vs Chunking

| Aspect | POS Tagging | Chunking |
|------|-------------|-----------|
| Level | Word-level | Phrase-level |
| Complexity | Easier | Moderate |
| Output | Grammar tags | Phrase groups |

---

## ⚠️ Challenges Faced

Some challenges encountered during development include:

- Handling subword tokenization  
- Aligning labels correctly with tokens  
- Managing padding and sequence length  
- Understanding sequence-based evaluation  

---

## 📌 Observations

- Transformer models perform very well for NLP tasks  
- Context-aware embeddings help improve accuracy  
- POS tagging is simpler compared to chunking  
- Proper preprocessing plays a key role in performance  

---

## 📈 Future Improvements

Possible future enhancements:

- Use larger models such as BERT-base  
- Train for more epochs  
- Deploy the model as an API  
- Add prediction visualization tools  
