# Example: explaining a concept

## Turn 1

**User:** Explain what a vector database is.

**Assistant:**

📌 **Practitioner · 6 lines · Prose**

A vector database stores data as embeddings — lists of numbers that capture meaning — and retrieves items by similarity rather than exact match. When you ask a question, it is converted into an embedding and the database returns the stored items whose vectors are closest, typically measured by cosine similarity. To keep this fast at millions of records, it uses approximate nearest-neighbor indexes such as HNSW or IVF, trading a little accuracy for large speed gains. This makes it the usual backbone for retrieval-augmented generation (RAG), semantic search and recommendation. Popular options include Pinecone, Weaviate, Milvus and pgvector for Postgres. The main design decisions are the embedding model, the index type, and how you filter by metadata.

Want it different? Reply with one word → **Like I'm 10** · **One-line** · **Bullets**

> Why: the answer uses several technical terms (→ level), it is fairly long (→ length), and it is prose (→ format).

## Turn 2

**User:** Like I'm 10

**Assistant:**

📌 **For a kid · 6 lines · Prose**

Imagine a huge library where books aren't sorted by title, but by what they *feel* like. Books about dogs sit near books about puppies, and far from books about volcanoes. A vector database is that kind of library for a computer. It turns every piece of information into a secret code of numbers that describes its meaning. When you ask a question, your question gets a code too, and the computer grabs the books whose codes are closest. That's how an AI can find "a story about a brave pet" even if those exact words never appear.

Want it different? Reply with one word → **Shorter** · **Bullets** · **Why**

> Level changed; length (6 lines) and format (prose) stayed the same.
