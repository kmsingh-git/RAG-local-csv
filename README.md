# RAG-local-csv
Exploration of local RAG capabilities on CSV data

## General components
- LangChain
    - Document Loader - to load CSV into memory
    - Text splitter - chunk the data before feeding to LLMs coz they have input size limits
    - Embeddings model - to convert chunks into vectors
        - from Hugging Face or Nomic
    - Vector store - this is called retriever in LangChain

Is text split and vectorization really needed even for already tabular data? Say you have 20 columns, and after one hot encoding, say 100. That's not a lot. So maybe you don't need this

- 
    - PromptTemplate - {context} and {question} format
    - QA Chain

- Ollama - to run models locally
    - what model to use? mistral?