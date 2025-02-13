# Retrieval-Augmented Generation (RAG) System Using LlamaIndex
This project implements a Retrieval-Augmented Generation (RAG) system that retrieves relevant information from a PDF document and generates responses to user queries using LlamaIndex.

# Key Components
* Document Processing: A PDF file (transformers.pdf) is loaded and indexed using LlamaIndex’s SimpleDirectoryReader.
- Embedding Model: Instead of OpenAI embeddings, the project uses a HuggingFace embedding model "BAAI/bge-small-en" for document vectorization.
- Vector Store Index: The indexed documents are stored in a VectorStoreIndex, allowing efficient retrieval of relevant passages.
- Custom LLM Wrapper: A custom GPT4All model is integrated using CustomLLM, ensuring compatibility with LlamaIndex.
- Query Engine: A retriever-based query engine (RetrieverQueryEngine) is created, which first retrieves the most relevant document fragments and then passes them to the LLM for response generation.
- Response Generation: The retrieved text is processed by the GPT4All model, providing meaningful answers based on the document contents.
