

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


## 📑 Dataset Format Explanation

### 1. Knowledge Document

This file is a **JSON array** containing multiple entries.

Each entry is a string representing a specific knowledge point or concept from each chapter of the course.

The format for each entry is:  
`"Number. Knowledge Point Title Content"`

---

### 2. Knowledge Graph

#### 2.1 GraphML File

**GraphML** is an XML format used to describe graphs. This file stores the **knowledge graph** of the dataset, including various **entities** (e.g., processes, semaphores) and the **relationships** (e.g., "uses", "depends on") between them.

Field Descriptions:
- **Nodes**: Each node represents an entity. For example, nodes might represent "Process", "Semaphore", etc.
  - **id**: The unique identifier of the node.
  - **name**: The name of the node, usually the name of the entity (e.g., "Process").
  - **type**: The type of the node, indicating the category of the entity, such as "Concept" or "Method".
  
- **Edges**: An edge represents the relationship between two entities. For example, there could be a "request" relationship between "Process" and "Resource".
  - **source**: The source entity's ID (starting node).
  - **target**: The target entity's ID (ending node).
  - **label**: The relationship's label, describing the connection between the two entities, such as "requests", "depends on", etc.

#### 2.2 vdb_relationships.json File

This file contains the relationship data between entities in the knowledge graph.

Field Descriptions:
- **source_id**: The ID of the source entity in the relationship.
- **target_id**: The ID of the target entity in the relationship.
- **content**: A description of the relationship, such as "Semaphore mechanism uses Wait operation to request resources".
- **type**: The type of relationship, such as "synchronization", "dependency", etc.

#### 2.3 vdb_entities.json File

This file contains the entity data in the knowledge graph. Each entity has detailed descriptive information.

Field Descriptions:
- **entity_id**: The unique identifier of the entity.
- **entity_name**: The name of the entity, such as "Process", "Semaphore", etc.
- **entity_type**: The type of the entity, such as "Method", "Concept", etc.
- **entity_description**: A description of the entity, briefly explaining its function, role, or characteristics.

---

### 3. QA Dataset

Each **question-answer pair** (record) contains the following fields:

- **id**: The unique identifier for the question.
- **type**: The type of the question, including multiple-choice, short-answer, etc.
- **question**: The text of the question.
- **answer_label**: The label for the correct answer (only present for multiple-choice questions).
- **answer_explain**: An explanation of the correct answer, helping to understand why the selected option is correct.
- **answer**: A combined field containing both the answer label and the explanation, formatted as `answer_label || answer_explain`.

---

This completes the dataset format explanation. It should help you understand how to process and use the dataset effectively.

