# Simple AI Workflow with RAG using OpenRouter and Supabase
#### Tiziana Ligorio for *AI Agents - CSCI 395.32* taught at Hunter College of The City University of New York

In this demo, we build a simple AI workflow that demonstrates the Retrieval Augmented Generation (RAG) pattern by creating a FastHTML tutor that can answer questions about the FastHTML library.

The workflow consists of the following stages:
1. **Document Loading** — Load the FastHTML documentation from a text file
2. **Chunking** — Split the documentation into manageable pieces
3. **Embedding** — Create vector embeddings for each chunk using OpenAI embeddings
4. **Storage** — Store the embeddings in a Supabase vector database (Postgres + pgvector)
5. **Retrieval** — Query the database for relevant chunks based on user questions
6. **Generation** — Use the retrieved context to generate accurate answers

This pattern illustrates how to ground LLM responses in specific documentation, reducing hallucinations and enabling the model to answer questions about information not in its training data.

## Getting Started

### Option 1: Run in Google Colab (Recommended for quick start)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/tligorio/ai_workflow_rag_tutorial/blob/main/AI_Workflow_with_RAG.ipynb)

Click the badge above to open the notebook directly in Google Colab.

### Option 2: Run Locally

For local installation, clone this repository and follow the instructions in [SETUP.md](SETUP.md).
