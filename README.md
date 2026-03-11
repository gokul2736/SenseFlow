# SenseFlow: Phishing & Social Engineering Detector

**TLead:** Markandeyan Gokul  
**TMemb:** Kanamarlapudi Sai Charithanjali 

## 📌 Problem Statement
Traditional antivirus systems use signature-based detection, which fails against "Clean Attacks" (Business Email Compromise). SenseFlow uses **Semantic Analysis (BERT)** to detect psychological triggers like Urgency and Authority.

## 🚀 Tech Stack
* **AI Engine:** Google BERT (via Hugging Face Transformers)
* **Explainability:** LIME (Local Interpretable Model-agnostic Explanations)
* **Frontend:** Streamlit
* **Backend:** PyTorch & Python 3.9+

## 📂 Project Structure
* `data/`: Raw and processed datasets (Ignored by Git).
* `src/`: Production-grade source code.
* `notebooks/`: Experimental labs for model training.
* `docs/logs/`: Weekly trial & error logs for PBL review.


<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/d709223e-6332-41d6-94db-ca39de2df32e" />




## Pipeline
              +----------------------+
              |   Email Input        |
              | (User Email Text)    |
              +----------+-----------+
                         |
                         v
              +----------------------+
              |   Text Preprocessing |
              | remove html, urls,   |
              | lowercase, cleaning  |
              +----------+-----------+
                         |
                         v
              +----------------------+
              |     Tokenization     |
              |  RoBERTa Tokenizer   |
              +----------+-----------+
                         |
                         v
              +----------------------+
              |   Transformer Model  |
              | DistilBERT / RoBERTa |
              |     / DeBERTa        |
              +----------+-----------+
                         |
                         v
              +----------------------+
              |   Phishing Detector  |
              |  Safe vs Phishing    |
              | Probability Score    |
              +----------+-----------+
                         |
                (If phishing detected)
                         |
                         v
              +----------------------+
              |   LLM Reasoning      |
              |      Llama 3.1       |
              | Detect manipulation  |
              +----------+-----------+
                         |
                         v
              +----------------------+
              |   Explainable Output |
              | Urgency / Authority  |
              | Financial request    |
              +----------+-----------+
                         |
                         v
              +----------------------+
              |  User Interface      |
              | Web App / Extension  |
              | Warning Message      |
              +----------------------+
