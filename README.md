# Oscars 2023 Query and Chat System (Retrieval augmented generation)

## Project Description
In this project, the Retriever-Augmented Generation (RAG) process is utilized to enhance the text-based query system to answer questions about the 2023 Oscars ceremony. RAG works by employing a two-step approach: firstly, the "retriever" component uses a sentence transformer model to convert the input query text into a dense vector, or embedding. These embeddings effectively capture the semantic essence of the text. This embedding is then used to search a ChromaDB database collection, which retrieves a set of documents that are contextually relevant to the query. The documents returned by ChromaDB act as an augmented knowledge base for the second step of the process.

The "generator" component then takes over, which in this case, is the LLAMA 2 model, an open-source language model adept at generating contextually rich text. The LLAMA 2 model receives the query along with the relevant documents retrieved by the ChromaDB as input. Using this combined information, the LLAMA 2 model generates an answer by synthesizing the information from the retrieved documents with the query context, producing a coherent and contextually relevant response. This integrated approach ensures that the answers provided by the chat interface are not just based on the LLAMA 2 model's pre-trained knowledge but are also informed by the specific details contained within the documents relevant to the Oscars 2023. The result is an accurate response that leverages both the depth of the retrieved documents and the generative capabilities of the LLAMA 2 model.
## How to Clone and Deploy

### Prerequisites
- Python 3.6 or later
- pip (Python package manager)

### Clone the Repository

### Installation
Before running the application, install the required packages using pip:

pip install chromadb, sentence-transformers,  pandas, numpy, huggingface_hub, openai, transformers


### Usage
To use the system, run the provided scripts after making sure you have the `oscars.csv` data file in the `/content` directory (check your respective directory)
This code has been built from scratch 


## Functionality

### What Works
- Text embedding generation using SentenceTransformer.
- Creation and querying of a ChromaDB collection with processed Oscars data.
- Chat system that uses the generated context to answer questions about the 2023 Oscars.

### What Does Not
- The code assumes the presence of a service running at the given URI, which may not be publicly accessible.
- Real-time updating of the Oscars database with new entries is not implemented.
