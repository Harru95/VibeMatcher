# 🎯 Nexora Vibe Matcher — Fashion Recommendation System

This project is a **mini AI recommender system** built for the **Nexora Artificial Intelligence Internship assignment**.  
It uses **text embeddings** and **cosine similarity** to match fashion products to an input “vibe” or mood (e.g., _energetic urban chic_, _cozy relaxed winter_).

---

## 🧩 Overview

The **Vibe Matcher** takes a short vibe description as input and recommends the top-3 matching fashion items from a small dataset.  
It works by converting both product descriptions and the vibe query into numerical **embeddings** using the `text-embedding-ada-002` model (via OpenAI or Euron API)  
and computing their **cosine similarity** to find the most similar items.

---

## ⚙️ Tech Stack

- **Language:** Python  
- **Frameworks/Libraries:**  
  - `pandas`, `numpy` – data handling  
  - `openai` – embeddings via API (Euron proxy supported)  
  - `scikit-learn` – cosine similarity  
  - `matplotlib` – evaluation plots  
  - `python-dotenv` – secure API key loading  

---

## 📂 Project Structure

Nexora-VibeMatcher/
├── Nexora_VibeMatcher.ipynb # Main notebook (with outputs)
├── README.md # You are here
├── requirements.txt # Dependencies
└── .gitignore # Hides .env & cache files


## 🚀 Run in Google Colab

You can open and run the notebook directly here:  
👉 **[Open in Colab](https://colab.research.google.com/drive/18t0ynkcG7KwH9lX0DObN_tz6TZg7muPK?usp=sharing)**

### Steps:
1. Upload your `.env` file or manually input your API key when prompted:
   ```python
   from getpass import getpass
   import os
   os.environ["OPENAI_API_KEY"] = getpass("Enter your Euron/OpenAI API key: ")
Run all cells (Runtime → Run all).

Enter your vibe queries (e.g., "beach vacation outfit") to see the top-3 product matches with similarity scores.

📊 Evaluation & Metrics
Queries tested:

Energetic urban chic

Cozy relaxed winter

Beach vacation outfit

Metrics logged:

Similarity score (> 0.7 → “good match”)

Latency per query (measured using timeit)

Visual outputs:

PCA-based embedding clusters

Similarity score distribution

Query latency comparison

🛡️ Security Note
The .env file containing API keys is not uploaded for security reasons.
The .gitignore ensures all sensitive files (like .env) remain private.
If running locally, create a .env file containing:

ini
Copy code
OPENAI_API_KEY=your_key_here
💡 Reflection & Improvements
Could integrate Pinecone or FAISS for scalable vector search.

Expand dataset to include multi-modal inputs (e.g., product images).

Add user feedback loop for better personalization.

👨‍💻 Author
Harsh Soni
AI/ML Enthusiast 
📧 hsharshsoni95@gmail.com

🪪 License
MIT License – free to use and adapt for learning purposes.
