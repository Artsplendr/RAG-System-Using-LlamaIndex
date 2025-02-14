# Retrieval-Augmented Generation (RAG) System Using LlamaIndex
This project implements a Retrieval-Augmented Generation (RAG) system, based on using LlamaIndex, that retrieves relevant information from a PDF document and generates responses to user queries.

# Key Components
- Document Processing: A PDF file (transformers.pdf) is loaded and indexed using LlamaIndex’s SimpleDirectoryReader.
- Embedding Model: Instead of OpenAI embeddings, I use HuggingFace embedding model "BAAI/bge-small-en".
- Vector Store Index: The indexed documents are stored in a VectorStoreIndex, allowing efficient retrieval of relevant passages.
- Custom LLM Wrapper: A custom GPT4All model is integrated using CustomLLM, ensuring compatibility with LlamaIndex.
- Query Engine: A retriever-based query engine (RetrieverQueryEngine) is created, which first retrieves the most relevant document fragments and then passes them to the LLM for response generation.
- Response Generation: The retrieved text is processed by the GPT4All model, providing meaningful answers based on the document contents.

# Workflow
1. Load & Preprocess Documents: The PDF file is read and converted into an indexed format.
2. Embed & Store: Documents are vectorized using HuggingFace embedding model "BAAI/bge-small-en" and stored in VectorStoreIndex.
3. Retrieve & Generate: When a user asks a query, the system retrieves relevant context and generates a response using the GPT4All model.
4. Display Results: The final response is printed for the user.

This system enables offline, cost-efficient, and private retrieval-augmented generation without relying on cloud-based models like OpenAI’s GPT-4. However, the speed of generating a response is quite slow.

# References
This project is based on the course "Building Your first RAG System using LlamaIndex" by Prashant Sahu / Analytics Vidhya and is available at the following [link](https://www.google.com/url?q=https%3A%2F%2Fcourses.analyticsvidhya.com%2Fcourses%2Fbuilding-your-first-rag-system-free-course).

### If you found this repository helpful, drop it a &#11088; :)!
