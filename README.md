# Document-Embedding-and-Retrieval-System-Using-ChromaDB

## 1. Installation of Required Libraries
The notebook starts by installing several Python libraries:

chromadb: The main library for working with ChromaDB.

tiktoken: A library for tokenizing text, which is useful for splitting text into manageable chunks.

langchain: A framework for building applications with large language models (LLMs). It provides tools for text splitting, embeddings, and vector storage.

langchain-community: A community-driven extension of LangChain that includes additional tools and integrations.

##✔ Installation process in the Jypter Notebook
!pip install chromadb
!pip install tiktoken
!pip install langchain
!pip install -U langchain-community
## 2. Loading Data
The notebook uses the DirectoryLoader from LangChain to load text files from a directory. In this case, it loads text files from the /content/new_articals2 directory.
DirectoryLoader: Loads all files in a directory that match a specific pattern (e.g., .txt files).
TextLoader: Loads the content of text files into a list of Document objects.
## 3. Splitting Text into Chunks
The notebook uses the CharacterTextSplitter from LangChain to split the loaded text into smaller chunks. This is important because large text documents need to be broken down into smaller pieces for processing and embedding.
chunk_size=1000: Each chunk will contain up to 1000 characters.
chunk_overlap=200: There will be a 200-character overlap between consecutive chunks to ensure context is preserved.
## 4. Converting Text to Vectors
The notebook uses OpenAI embeddings to convert the text chunks into vectors.
These vectors are numerical representations of the text that can be stored and queried in ChromaDB.
## 5. Storing Vectors in ChromaDB
The notebook then stores the embeddings in ChromaDB, a vector database optimized for fast similarity searches.
## 6 .Implement  model : 
model_name = 'all-MiniLM-L6-v2'
## 7 . Querying the Vector Database
Once the vectors are stored in ChromaDB, you can query the database to find documents that are semantically similar to a given query.
query = "how much money did Microsoft raise? "
response = query_model(query)
print(response)
## 8 . Finally output : 
$45 billion


