# SDS 2024 - Cleantech RAG

By [Daniel Perruchoud](https://www.linkedin.com/in/daniel-olivier-perruchoud-799aaa38/) and [George Rowlands](https://www.linkedin.com/in/georgerowlands/)

## Introduction

This notebook delves into the exciting realm of Cleantech using a [dataset of nearly 10,000 news articles from Kaggle](https://www.kaggle.com/datasets/jannalipenkova/cleantech-media-dataset), all centered around the energy sector. We'll embark on a journey that includes data exploration, text preprocessing, and culminates in the creation of a Retrieval-Augmented Generation Pipeline (RAG). This powerful approach empowers us to construct an LLM (Large Language Model) that can intelligently answer user queries, drawing upon the knowledge from our curated news articles.

### Why RAG? A Cost-Effective and Dynamic Solution

Fine-tuning an LLM can be a resource-intensive and inflexible process. RAG offers a compelling alternative. It leverages a semantic search to pinpoint relevant sections within our news articles that directly address a user's question. These retrieved sections are then provided to the LLM as context, enabling it to deliver informed and insightful responses.

![rag_pipline](https://arxiv.org/html/2312.10997v5/extracted/2312.10997v5/images/RAG_case.png)

### Setup

To run this notebook we recommend downloading the provided [GitHub repository](https://github.com/LuciferUchiha/sds2024-cleantech-rag) and opening this notebook in [Google Colab](https://colab.research.google.com/). To ensure a smooth experience, you'll need:

- An OpenAI API key for GPT-4 and embedding models
- A Google account for Google Colab
- Python packages (automatically installed within the notebook)

At the start of the notebook a `data.zip` will be downloaded from a Google Drive and unzipped. This will then provide you with files that contain checkpoints for all of the expensive processing sections such as chunking, generating embeddings and evaluating the pipeline with an LLM as a judge. This saves you money and a lot of time.

If you can't or don't want to run this notebook you can also view the completed notebook by opening the `cleantech_rag.html` file in your browser.

### Unveiling the Depths of RAG Pipelines

Throughout this notebook, we'll delve into the intricate workings of RAG pipelines. Prepare to explore:

- Building a Robust RAG Pipeline:
  - LLM: GPT-4 turbo
  - Semantic Search: ChromaDB with HNSW for fast retrieval
  - Embedding Models: OpenAI, BGE-M3, all-MiniLM-L6-v2
  - Chunking Strategies: Recursive (256 & 1024 chunk sizes) and Semantic Chunking
- Understanding RAG's Inner Workings:
  - Examining the embedding space of news articles
  - Demystifying the semantic search process
- Visualization and Explanation:
  - Visualizing the impact of advanced strategies like HyDE and Multi-querying
- Evaluation and Comparison:
  - RAGAS for LLM-based evaluation
  - Traditional retrieval metrics

Questions or Issues? We're Here to Help!

If you encounter any roadblocks or have questions, please don't hesitate to reach out to [George Rowlands](https://www.linkedin.com/in/georgerowlands/)
