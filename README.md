# 🤖 MotiveBot (RAG Support Agent)

This project implements a **retrieval-augmented chatbot** for Motive’s Help Center content using AWS Bedrock + Amazon Titan embeddings. It supports both **single-turn** and **multi-turn** Q&A with context memory, producing **concise, support-style answers**.

---

## ✨ Features

- 📚 Parse and clean Motive Help Center data (`web_content.txt`).
- 🧩 Chunking and de-duplication of content.
- 🔍 Hybrid search (TF-IDF lexical + Titan v1 embeddings).
- 💾 Embedding caching (`embed_cache_titan_v1.pkl`) to avoid repeated API calls.
- 📝 Exports answers into clean CSVs for evaluation.

---

## ⚡ Notes

- 🪣 Embedding cache is stored in `embed_cache_titan_v1.pkl` to reduce AWS Bedrock calls.
- 🧠 Hybrid search combines TF-IDF and Titan v1 embeddings for robust retrieval.
- 🤝 Answers are intentionally short, polite, and factual to mimic a customer support tone.

---

## 🛠 Future Improvements

- 🚀 Replace pickle cache with a vector database (e.g., FAISS, Pinecone) for faster lookups.
- 📝 Enhance semantic follow-up detection with deeper context awareness.
- 📊 Expand evaluation against leaderboard-style test sets.
