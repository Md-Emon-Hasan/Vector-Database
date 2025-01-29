# Vector Database Mastery: ChromaDB, Pinecone, and Weaviate

Welcome to the **Vector Database Mastery** repository! This repository contains code and examples demonstrating how to use three powerful vector database technologies: **ChromaDB**, **Pinecone**, and **Weaviate**. These databases are essential for building scalable, high-performance vector search engines, which are key for AI applications like semantic search, recommendation systems, and more.

![Image](https://github.com/user-attachments/assets/b6f2c381-1bdd-46b9-ae3e-16797b747e28)

## Table of Contents
- [Introduction](#introduction)
- [Technologies Covered](#technologies-covered)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [License](#license)
- [Contact](#contact)

## Introduction

This repository aims to guide you through the process of mastering ChromaDB, Pinecone, and Weaviate, from beginner to advanced levels. It includes practical examples, usage guides, and configuration instructions to help you integrate and leverage these vector databases for your own machine learning and AI-driven projects.

## Technologies Covered

### ChromaDB
[ChromaDB](https://www.trychroma.com/) is an open-source vector database optimized for machine learning models, offering powerful embedding storage and retrieval capabilities. In this repository, you'll find examples on how to interact with ChromaDB to store and query embeddings efficiently.

### Pinecone
[Pinecone](https://www.pinecone.io/) is a fully managed vector database service that provides fast, scalable similarity search and indexing for high-dimensional data. This repository includes examples of how to integrate Pinecone into your applications for vector search tasks.

### Weaviate
[Weaviate](https://weaviate.io/) is an open-source vector search engine designed for storing, indexing, and querying high-dimensional data. It also supports multimodal data types like text, images, and audio. You'll find examples of how to set up Weaviate for semantic search and other AI-driven use cases.

## Installation

To get started with the code in this repository, you'll need to install a few dependencies:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/vector-database-mastery.git
   cd vector-database-mastery
   ```

2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

   Make sure you have Python 3.6+ installed.

3. Set up any necessary environment variables (API keys for Pinecone, Weaviate, etc.).

## Usage

### ChromaDB
1. Set up ChromaDB using the following commands:
   ```python
   from chromadb import Client
   client = Client()
   ```

2. Insert embeddings:
   ```python
   collection = client.create_collection("my_collection")
   collection.add([embedding1, embedding2])
   ```

3. Perform a similarity search:
   ```python
   results = collection.query(embedding_query)
   ```

### Pinecone
1. Initialize Pinecone:
   ```python
   import pinecone
   pinecone.init(api_key="your-pinecone-api-key", environment="us-west1-gcp")
   ```

2. Create an index and insert vectors:
   ```python
   index = pinecone.Index("example-index")
   index.upsert([(id1, vector1), (id2, vector2)])
   ```

3. Query Pinecone for nearest neighbors:
   ```python
   query_results = index.query([query_vector], top_k=5)
   ```

### Weaviate
1. Set up Weaviate client:
   ```python
   import weaviate
   client = weaviate.Client("http://localhost:8080")
   ```

2. Create a class and insert data:
   ```python
   client.schema.create_class({
       "class": "Document",
       "properties": [
           {"name": "content", "dataType": ["text"]},
           {"name": "embedding", "dataType": ["vector"]},
       ]
   })
   client.data_object.create({"content": "Some text", "embedding": embedding_data}, class_name="Document")
   ```

3. Perform a search:
   ```python
   response = client.query.get("Document", ["content"]).with_near_vector({"vector": query_vector}).do()
   ```

## Examples

The repository includes various example scripts demonstrating the integration of ChromaDB, Pinecone, and Weaviate. Check out the following files:
- `chroma_example.py` — Example code for working with ChromaDB.
- `pinecone_example.py` — Example code for using Pinecone for vector search.
- `weaviate_example.py` — Example code for integrating Weaviate.

## License

This repository is licensed under the MIT License. See [LICENSE](LICENSE) for more information.


## Contact

- **Email:** [iconicemon01@gmail.com](mailto:iconicemon01@gmail.com)
- **WhatsApp:** [+8801834363533](https://wa.me/8801834363533)
- **GitHub:** [Md-Emon-Hasan](https://github.com/Md-Emon-Hasan)
- **LinkedIn:** [Md Emon Hasan](https://www.linkedin.com/in/md-emon-hasan)
- **Facebook:** [Md Emon Hasan](https://www.facebook.com/mdemon.hasan2001/)

---

Feel free to contribute, open issues, or suggest improvements!
