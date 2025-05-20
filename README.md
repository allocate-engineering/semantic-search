# 🧠 Semantic Search System – Interview Challenge

Welcome! This is your technical design and coding challenge for the **Lead AI Data Engineer** role.

The focus is on **search and retrieval over unstructured financial documents** using modern semantic search techniques. Time is limited, so take shortcuts where you need to and explain if there are differences to how you would do something in the "real world" versus now.

---

## 📚 Scenario

You've just joined a mid-sized fintech company that provides research tools and analytics to institutional investors. One of the biggest pain points is that **finding insights across investment documents is still too manual**.

You've been tasked to prototype a system that can answer questions like:

- “Show me hedge funds with increased leverage after Q2 2022.”
- “Which funds mentioned exposure to emerging markets in the last two quarters?”

There's a large corpus of unstructured documents (see the $docs/$ folder). Your job is to design how this works end-to-end, and build a basic prototype.

---

## ✅ Your Tasks

### 1. Design the architecture

- Propose how documents and their semantic representations (embeddings) should be stored
- Recommend the appropriate storage (SQL, NoSQL, vector DB, or hybrid)
- Draft a schema and explain trade-offs and edge cases

### 2. Build a simple prototype

- Simulate generating embeddings for a few sample documents (real or mocked)
- Store them in-memory or in a vector DB (e.g. FAISS, Chroma, Qdrant)
- Execute semantic search based on the user queries above

> Keep it focused — we're not expecting a production-ready system, just clear thinking and working code.

### 3. Consider the big picture

- How would you scale this to millions of documents?
- How would you handle document refreshes and re-embedding?
- What cloud services would you use (e.g. AWS/GCP/Azure)?

---

## 🧪 Sample Documents

We've included a few example documents in `docs/` to simulate fund prospectuses, earnings summaries, and internal memos.

You can ingest these from disk and generate embeddings from the raw text.

---

## 🚀 Quick Start (Docker-based)

We've included a simple Docker environment with Python + FAISS + sentence-transformers to get you moving fast.

### Build & Run

```bash
docker-compose up --build

# OR if you just want the Python container
docker build -f docker/python/Dockerfile -t semantic-search .
docker run -it -v $PWD:/app semantic-search bash
```

You can also run this as a DevContainer in VS Code.

---

## 🔍 Bonus Topics (If Time Allows)

- Use a vector DB like Qdrant (included in docker-compose)
- Add document metadata and filter search results
- Return ranked results with source highlights

---

## 💡 Tips

- Use sentence-transformers like `all-MiniLM-L6-v2` for fast, decent embeddings
- Simulate queries like the ones above — you don't need a UI
- Code clarity and reasoning > feature completeness

---

Good luck, and have fun!
