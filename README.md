# Naive RAG with LangChain

This is a simple Retrieval-Augmented Generation (RAG) pipeline built using LangChain, open-source embeddings, and a local LLM model via CTransformers.

----------------------------------------

Clone the Repository

git clone https://github.com/wrathog12/Naive-RAG.git
cd Naive-RAG

----------------------------------------

Setup: Jupyter Notebook + Virtual Environment

1. Create a virtual environment (recommended to avoid conflicts):

python -m venv .venv

2. Activate the environment:

- Windows:
.venv\Scripts\activate

- macOS/Linux:
source .venv/bin/activate

3. Install dependencies:

pip install -r requirement.txt

4. Launch Jupyter Notebook:

jupyter notebook

Create a new notebook and start using the modular RAG cells from NaiveRAG.ipynb.

----------------------------------------

What is RAG?

Retrieval-Augmented Generation (RAG) combines:
- A retriever (e.g., FAISS + embedding model) to fetch relevant chunks from source documents
- A generator (LLM) to synthesize answers using that retrieved context

This allows for more accurate, context-aware answers — especially useful when the model itself doesn’t have the knowledge stored.

----------------------------------------

Built With

- LangChain: modular framework for combining LLMs with tools
- FAISS: fast similarity search over dense vectors
- SentenceTransformers: for lightweight embeddings (all-MiniLM-L6-v2)
- CTransformers: runs local .ggml quantized models (e.g., LLaMA 2)
- Open-source PDF/JSON loading with LangChain loaders

----------------------------------------

Model Flexibility

We’re using a local LLaMA 2 model via CTransformers, but you can easily switch to cloud APIs such as:
- OpenAI GPT-4 via langchain.llms.OpenAI
- Anthropic Claude, Google Gemini, or others via LangChain wrappers

----------------------------------------

Folder Structure

Naive-RAG/
├── NaiveRAG.ipynb         <- Main modular notebook
├── requirement.txt        <- Python dependencies
├── data/                  <- Your source documents (.json or .pdf)
├── model/                 <- Local LLM model (e.g., .bin for LLaMA)
└── one/                   <- (Optional) ignored test folder

----------------------------------------

License

MIT — feel free to use and modify.
