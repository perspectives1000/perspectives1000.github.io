---
title: RAG - Methodologies and retrieval techniques
date: 2024-05-10
categories: [llm-pipeline]
tags: [general]
author: perspectives1000
---

### RAG methodologies

While this area is rapidly evolving and the techniques could be grouped in several different ways, below is one take on it from the blog reference.

Here's a breakdown of different Retrieval-Augmented Generation (RAG) methodologies. 

**1. Naive RAG:**

- This is the most basic form of RAG. It retrieves documents based on the user query using a search method like vector retrieval (finding documents with similar vector representations to the query).
- The retrieved documents are then simply concatenated (joined together) and fed to the large language model (LLM) for generation.
- **Advantages:** Simple to implement, computationally efficient for smaller datasets.
- **Disadvantages:** May lack context or miss relevant information due to basic retrieval methods.

**2. Agent-assisted RAG:**

- This approach introduces an "agent" that acts as an intermediary between the user query and the LLM.
- The agent can perform various tasks:
    - **Query reformulation:** Rephrase or expand the user query to improve retrieval accuracy.
    - **Active learning:** The agent might ask clarifying questions to the user to better understand their intent.
    - **Document filtering:** The agent can filter retrieved documents based on relevance or additional criteria.
- **Benefits:** Improves the quality and focus of retrieved information for the LLM.
- **Challenges:** Designing and training the agent effectively can be complex.

**3. Guardrails RAG:**

- This method incorporates mechanisms to guide the LLM's generation process and prevent unwanted outputs.
- Guardrails can take various forms:
    - **Safety filters:** Flag or block outputs containing harmful content or biases.
    - **Factual consistency checks:** Ensure generated text aligns with factual information from retrieved documents.
    - **Style guides:** Enforce specific writing styles or tones for the generated text.
- **Benefits:** Improves the reliability and control over the generated outputs.
- **Considerations:** Defining appropriate guardrails depends on the specific application and desired outcomes.

**4. Knowledge Graph Aided RAG (KG-RAG):**

- This approach leverages knowledge graphs (networks of interconnected entities and relationships) to enhance the context understanding of the LLM.
- Techniques:
    - **Entity Linking:** Connect entities mentioned in the query and retrieved documents to relevant nodes in the knowledge graph.
    - **Relation Reasoning:** The LLM can utilize the relationships within the knowledge graph to infer additional information and generate more comprehensive outputs.
- **Advantages:** Leads to richer and more informative text generation by incorporating background knowledge.
- **Requirements:** Access to a well-defined and relevant knowledge graph for the specific domain.

**5. Time-Based RAG:**

- This method incorporates time-awareness into the retrieval and generation process.
- Considerations:
    - **Temporal Information Retrieval:** Focus retrieval on documents relevant to a specific time period mentioned in the query or related to the topic's evolving nature.
    - **Time-based LLM Prompting:** The LLM prompt can be adjusted to consider the temporal context of the query for more relevant generation.
- **Benefits:** Improves the factual accuracy and temporal relevance of generated outputs, especially for topics that change over time.
- **Challenges:** Requires effective methods for identifying and handling temporal information within the data.

Choosing the right RAG methodology depends on your specific needs and application. Consider factors like the complexity of the task, dataset size, and desired level of control over the generation process.

### **RAG Improvements & Optimization:**

- **Generate Multiple Queries:** Explore generating similar queries based on the user prompt to potentially improve retrieval results.
- **Retrieval Methods:**
    - **Chunk Decoupling:** Separate retrieval (similarity search) from generation steps for efficiency.
    - **Document Summary:** Summarize documents, embed them, and store them for retrieval. During retrieval, relevant summaries with linked chunks are provided to the LLM.
    - **Sentence Text Windows:** Split documents into sentences, embed them, and store them. During retrieval, relevant sentences with surrounding context are provided to the LLM.
    - **Parent Document Retriever:** Chunk documents, store their embeddings, and link them back to parent documents for retrieval. This ensures granular retrieval and detailed context for generation.
- **Structured Retrieval:**
    - **Metadata Filters & Auto-Retrieval:** Tag documents with metadata and use it to filter retrieved information, improving its relevancy.
    - **Document Hierarchy:** Chunk documents, tag them with metadata, and summarize the original document. During retrieval, relevant document summaries with linked chunks are returned to the LLM.
- **Reranking:** Use a reranking model to improve the accuracy of retrieved information by analyzing a larger subset of data from the initial vector search.
- **Recursive Retrieval:** Leverage retrieval from different sources like documents, databases, and specialized tools for a more comprehensive information gathering process.

----
**Reference:**  https://kdb.ai/learning-hub/articles/understanding-rag-approaches/
