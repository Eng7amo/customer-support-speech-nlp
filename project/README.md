# Customer Support Speech Recognition & NLP Project

## Objective
The goal of this project is to design and implement an end-to-end pipeline that transforms customer support audio calls into actionable insights using Natural Language Processing (NLP).

Specifically, the project focuses on:
- Transcribing customer support audio calls into text
- Performing sentiment analysis on call transcripts
- Extracting named entities to identify common themes and issues
- Finding semantically similar customer calls based on a textual query

---

## Dataset & Inputs
- `sample_customer_call.wav`  
  Sample customer support audio call used for speech-to-text transcription.

- `customer_call_transcriptions.csv`  
  Pre-transcribed customer calls containing:
  - Call text
  - Ground-truth sentiment labels

---

## Methodology

### 1. Speech Recognition
- Used the `SpeechRecognition` library to convert audio calls into text
- Extracted audio metadata such as frame rate and number of channels using `Pydub`

### 2. Sentiment Analysis
- Applied VADER sentiment analysis from NLTK
- Classified customer sentiment into:
  - Positive
  - Neutral
  - Negative

### 3. Named Entity Recognition (NER)
- Used spaCy's `en_core_web_sm` model
- Extracted frequently occurring entities across customer calls

### 4. Semantic Similarity Search
- Represented customer calls using spaCy embeddings
- Retrieved the most similar call based on cosine similarity to a query

---

## Technologies Used
- Python
- SpeechRecognition
- Pydub
- spaCy
- NLTK (VADER)
- Pandas

---

## Output
- Transcribed customer call text
- Sentiment predictions for customer calls
- Most frequently mentioned named entities
- Most similar customer call for a given query

---

## Notes
This project emphasizes clarity, reproducibility, and real-world applicability of NLP techniques in customer support analytics.
