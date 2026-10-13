---
layout: post
title: "RAG: what actually matters"
date: 2026-12-01
tags: [AI, LLM, RAG]
read: 6
---
Replace this text with your own writing. Everything below shows what a post can hold.

## The question

How do you make a model answer questions about *your* documents? That is what RAG is for.

## The big picture

![RAG pipeline]({{ '/assets/images/rag-pipeline.png' | relative_url }})
*The four steps of a RAG system.*

## Under the hood

```python
def chunk(text, size=500, overlap=50):
    chunks = []
    start = 0
    while start < len(text):
        chunks.append(text[start:start + size])
        start += size - overlap
    return chunks
```

| Choice | Why it matters |
|--------|----------------|
| Chunk size | Too small loses context, too large adds noise |

> Measure first. Most RAG problems are retrieval problems.

## Key takeaways

- Retrieval quality limits answer quality.
