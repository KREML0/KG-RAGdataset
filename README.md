

## 📚 Educational Knowledge Graph and QA Dataset for RAG / KG-RAG Evaluation

This dataset is constructed from real university textbooks and provides aligned knowledge documents, knowledge graphs, and QA datasets. It addresses the long-standing issue where knowledge graphs and evaluation datasets are inconsistent or mismatched in content.

---

## 🎯 Purpose of the Dataset

- Serves as a benchmark for evaluating various **RAG models**, including dense retrieval, hybrid retrieval, and KG-based RAG (GraphRAG).  
- Provides a solid data foundation for **KG-RAG applications in intelligent education**, such as textbook QA, tutoring systems, and knowledge reasoning.  
- Supports tasks that require **multi-hop reasoning**, **evidence grounding**, and **knowledge tracing**.

---

## 📂 Components of the Dataset

The dataset consists of three major components:

1. **Knowledge Documents**  
   Structured content extracted from real textbooks.

2. **Knowledge Graph**  
   Entity–relation–entity triples aligned with textbook knowledge points.

3. **QA Dataset**  
   Includes multiple-choice, short-answer, and multi-hop questions with evidence paths.

---

## 📘 Textbooks Included

The current version contains three computer science textbooks:

- *Computer Organization*  
- *Computer Networking*  
- *Operating Systems*

For the textbooks:

- *Computer Organization*  
- *Operating Systems*

which contain large amounts of content, **each chapter** can generate its own:

- Knowledge graph  
- QA dataset  

This allows **fine-grained, chapter-level evaluation** of RAG and KG-RAG models.
