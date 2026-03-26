# 🧠 NLP Preprocessing Engine (Internship Assignment)

## 📌 Overview

This project focuses on building a **robust NLP preprocessing pipeline** capable of handling real-world noisy text data.

The solution is implemented using Python and demonstrates how raw text can be transformed into clean, structured tokens suitable for machine learning applications.

---

## 🎯 Objectives

* Handle noisy real-world text (emojis, URLs, numbers)
* Perform text normalization
* Generate clean tokens
* Analyze token-level statistics
* Build a reusable NLP pipeline

---

## ⚙️ Features Implemented

### ✅ Task 1: Conceptual Understanding

* Difference between "Love" vs "love"
* Importance of stopwords
* Stemming vs Lemmatization
* Real-world NLP considerations

---

### ✅ Task 2: Advanced Preprocessing Function

Implemented `preprocess_text()` with:

* Lowercase conversion
* URL & email removal
* Number removal
* Handling repeated characters
* Removing special characters
* Removing short tokens (≤2 except "no", "not")
* Extra space removal

---

### ✅ Task 3: Stress Testing

Tested the function on diverse inputs:

* Emojis
* Slang
* URLs
* Numbers
* Repeated characters

Displayed:

* Original text
* Cleaned tokens
* Cleaned sentence

---

### ✅ Task 4: Token Analytics

Computed:

* Total tokens
* Unique tokens
* Average token length

---

### ✅ Task 5: Frequency Analysis

* Top 10 most frequent words
* Top 5 least frequent words

Used:

```python
from collections import Counter
```

---

### ✅ Task 6: Full Pipeline

Created reusable function:

```python
def full_pipeline(text_list):
```

Output:

* Clean sentences
* Combined tokens

---

### ✅ Task 7: Error Handling

Handled edge cases:

* Empty string
* Only emojis
* Only numbers

Ensured:

* No crashes
* Clean outputs

---

## 🧪 Example Input

```python
"I absolutely looooved this product 😍😍"
```

## ✅ Output

```python
"absolutely loved this product"
```

---

## 🛠️ Technologies Used

* Python
* Regular Expressions (re)
* Collections (Counter)
* Jupyter Notebook

---

## 📁 Project Structure

```text
nlp_preprocessing.ipynb
README.md
```

---

## 🚀 How to Run

1. Open the notebook in Jupyter / Google Colab
2. Run all cells sequentially
3. View outputs for each task

---

## 📊 Conclusion

This project demonstrates how to build a **scalable and robust NLP preprocessing engine** capable of handling real-world text data. The pipeline is modular, reusable, and suitable for various NLP applications such as sentiment analysis, classification, and search systems.

---
