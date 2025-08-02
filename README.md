# 🗣️ Echo Chamber: Conversational AI Fine-Tuning Project

This project is about fine-tuning a conversational AI model using movie dialogues.

## 📌 Overview

I am using **DialoGPT** (a transformer-based conversational model from Hugging Face) as our base model. It is already pretrained on a large Reddit conversation dataset.

I fine-tuned it further using the **Cornell Movie Dialogues Corpus**, which contains over 220,000 lines of movie conversations.

---

## 📁 Project Structure

EchoChamber-SoC/
│
├── dialogpt-finetuned/
│   └── final/                    # Fine-tuned model 
│       ├── config.json
│       ├── vocab.json
│       ├── merges.txt
│       └── ...                  # Other model/tokenizer files
│
├── .gitattributes               # Git LFS tracking config for large model files
├── app.py                       # Main Python app (Streamlit)
├── requirements.txt             # Python dependencies
└── README.md                    


## 📊 Dataset: Cornell Movie Dialogues Corpus

- `movie_lines.txt`
- `movie_conversations.txt` 

In this i have used **10,000 dialogue pairs** to train the model.

---

## 🛠️ Changes Made

### 1. 🔄 Increased Dataset Size

### 2. 🔁 Increased Epochs
Reduced loss from 0.7 to 0.5
### 3. 🧠 Tokenization Update
- Added `"human:"` and `"bot:"` labels to each training sample.
```python
formatted_text = f"human: {prompt}\nbot: {response}"
