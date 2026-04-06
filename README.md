# Azure Text Embedding Model - Overview 

Costa Rica

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/) [Cloud2BR OSS - Learning Hub](https://github.com/Cloud2BR-MSFTLearningHub)

Last updated: 2026-04-06

-----------------------------

<details>
<summary><b>List of References</b> (Click to expand)</summary>

-  [voyage-3-large: the new state-of-the-art general-purpose embedding model](https://statics.teams.cdn.office.net/evergreen-assets/safelinks/2/atp-safelinks.html)
-  [text-embedding-3-large](https://platform.openai.com/docs/models/text-embedding-3-large#:~:text=text-embedding-3-large%20is%20our%20most%20capable%20embedding,english%20and%20non-english%20tasks.)
-  [Embedding Leaderboard](https://huggingface.co/spaces/mteb/leaderboard) - reports
-  [The Legacy MTEB Leaderboard repository](https://github.com/embeddings-benchmark/leaderboard?tab=readme-ov-file) - explanation and relevant links 
-  [Massive Text Embedding Benchmark](https://github.com/embeddings-benchmark/mteb) - open source how it was created
-  [Model leaderboards in Azure AI Foundry portal (preview)](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/model-benchmarks)
-  [Find the best model by comparing model performance across various criteria](https://ai.azure.com/explore/models/leaderboard?tid=cc34547a-d117-4060-9c6e-1c8d622c8d02)
-  [Chunk large documents for vector search solutions in Azure AI Search](https://learn.microsoft.com/en-us/azure/search/vector-search-how-to-chunk-documents)

</details>


<details>
<summary><b>Table of Contents</b> (Click to expand)</summary>

- [Recommendations for Alternative & Upcoming Embedding Models in Azure](#recommendations-for-alternative--upcoming-embedding-models-in-azure)
    - [Azure OpenAI](#azure-openai)
    - [Azure AI Foundry](#azure-ai-foundry)
    - [Azure Marketplace](#azure-marketplace)
- [How Azure AI Search Can Help Optimize Embedding Performance](#how-azure-ai-search-can-help-optimize-embedding-performance)

</details>


## Recommendations for Alternative & Upcoming Embedding Models in Azure

> Current Options: 

| **Model** | **Platform** | **Strengths** | **Limitations** | **Best Use Cases** |
|-----------|--------------|---------------|------------------|---------------------|
| `voyage-3` | Azure Marketplace | Balanced performance, tuned for enterprise domains, cost-efficient | No native integration with Azure AI Foundry, limited multilingual support | Internal search, domain-specific retrieval, enterprise RAG |
| `voyage-3-lite` | Azure Marketplace | Lightweight, fast, low latency and compute cost | Slightly reduced semantic precision, less robust for long-form text | Mobile apps, real-time classification, edge deployments |
| `voyage-finance-2` | Azure Marketplace | Specialized for financial language and jargon, tuned for structured documents | Poor generalization outside finance, narrow scope | Financial document analysis, compliance, financial RAG |
| `voyage-law-2` | Azure Marketplace | Legal-specific, optimized for contracts and statutes | Limited cross-domain utility, narrow vocabulary | Legal search, contract parsing, regulatory compliance |
| `voyage-multilingual-2` | Azure Marketplace | Multilingual support, tuned for global corpora | Slightly lower precision in English, not ideal for domain-specific tasks | Multilingual semantic search, global content indexing |
| `text-embedding-ada-002` | Azure OpenAI / AI Foundry | Legacy model, fast and inexpensive, widely supported | Lower semantic quality, outdated compared to newer models | Lightweight search, prototyping, low-cost RAG |
| `text-embedding-3-small` | Azure OpenAI / AI Foundry | Fast, cost-effective, configurable, good for short texts | Lower accuracy on nuanced or complex queries | Chat summarization, real-time applications, indexing |
| `text-embedding-3-large` | Azure OpenAI / AI Foundry | High semantic fidelity, multilingual, robust across domains | Higher latency and cost, batch quirks | Semantic search, multilingual corpora, recommendation systems |
| `embed-v-4-0` | Azure AI Foundry | High-performance, optimized for retrieval and RAG, scalable | Newer model with limited public benchmarks | Advanced RAG pipelines, enterprise search, hybrid retrieval |
| `Cohere-embed-v3-multilingual` | Azure AI Foundry | Strong multilingual alignment, semantic robustness | Slightly slower, less tuned for English-only tasks | Multilingual indexing, global search, translation-aware retrieval |
| `Cohere-embed-v3-english` | Azure AI Foundry | High precision for English, optimized for semantic tasks | Not suitable for multilingual content | English-centric semantic search, document clustering |

> [!NOTE]
> `Upcoming Models to Watch:`
- **Voyage-3-Large**: Expected to outperform OpenAI v3-large with flexible dimensions and quantization. [voyage-3-large: the new state-of-the-art general-purpose embedding model](https://statics.teams.cdn.office.net/evergreen-assets/safelinks/2/atp-safelinks.html)

### Azure OpenAI

> - `text-embedding-ada-002`
> - `text-embedding-3-large`
> - `text-embedding-3-small`

1. Go to your Azure OpenAI Platform:

     <img width="1916" height="840" alt="image" src="https://github.com/user-attachments/assets/424f2d85-37e4-4e74-b303-2e8c5a23a864" />

2. Under `Model catalog`, filter by `Inference task` > `Embeddings`:

     <img width="1905" height="848" alt="image" src="https://github.com/user-attachments/assets/8747ad65-bf2b-4fdd-bdb8-6ad505b4ebdf" />

     <img width="1893" height="695" alt="image" src="https://github.com/user-attachments/assets/8d822c1d-04fd-49ba-a514-1a3f74e24cdc" />

### Azure AI Foundry

> - `embed-v-4-0`
> - `Cohere-embed-v3-multilingual`
> - `Cohere-embed-v3-english`
> - `text-embedding-ada-002`
> - `text-embedding-3-large`
> - `text-embedding-3-small`

1. Go to your Azure AI Foundry Platform:

    <img width="1897" height="791" alt="image" src="https://github.com/user-attachments/assets/f56fc29b-2276-4998-9f0c-226e4329ca78" />

2. Under `Model catalog`, filter by `Inference task` > `Embeddings`:

    <img width="1907" height="847" alt="image" src="https://github.com/user-attachments/assets/45b1676c-8c5b-4084-be19-4eeb56e8f961" />

### Azure Marketplace

> [Azure Marketplace](https://azuremarketplace.microsoft.com/en-us/marketplace/apps?search=embedding&page=1):
> - `voyage-3 Embedding Model`
> - `voyage-3-lite Embedding Model`
> - `voyage-finance-2 Embedding Model`
> - `voyage-law-2 Embedding Model`
> - `voyage-multilingual-2 Embedding Model`

<img width="1900" height="837" alt="image" src="https://github.com/user-attachments/assets/0eac2f90-bf75-45cf-aa06-5e4420dc8be5" />

## How Azure AI Search Can Help Optimize Embedding Performance

> Azure AI Search doesn’t generate embeddings from third-party models, but it **amplifies their value** through advanced indexing, retrieval, and hybrid search capabilities.

> [!TIP]
> Use Azure AI Foundry to experiment with multiple embedding models and benchmark their performance before committing to production.

<details>
<summary><b>Vector Search Capabilities</b> (Click to expand)</summary>

> Azure AI Search supports robust vector search features that allow you to fully leverage embeddings generated externally (e.g., from OpenAI, Voyage, Cohere):

- Accepts **custom embeddings** from any model, making it agnostic and flexible across providers.
- Supports **semantic similarity search** using metrics like cosine similarity and dot product, enabling nuanced matching beyond keyword overlap.
- Handles **large-scale indexing** and **low-latency retrieval**, ideal for enterprise-grade applications with millions of documents.
- Integrates with **hybrid search pipelines**, combining vector and keyword search to improve both precision and recall.

> Example Use Cases:

- Intelligent document retrieval for legal or financial archives.
- FAQ matching and chatbot grounding using semantic similarity.
- Product recommendation systems based on user intent embeddings.

</details>

<details>
<summary><b>Performance Optimization Tips</b> (Click to expand)</summary>

> To maximize efficiency and relevance in embedding-based search, consider these strategies:

1. **Choose embedding size wisely**: Smaller embeddings (e.g., 512–1024) reduce latency and storage costs, ideal for mobile or real-time apps.
2. **Batch embedding generation**: Pre-process documents in bulk to reduce API calls and improve throughput.
3. **Use domain-specific models**: Models like `voyage-finance-2` or `voyage-law-2` yield better semantic relevance in specialized contexts.
4. **Monitor vector DB costs**: Larger embeddings increase storage and query costs, balance precision with efficiency.
5. **Leverage hybrid search**: Combine keyword and vector search to handle both exact and fuzzy matches, especially in noisy datasets.
6. **Normalize and deduplicate embeddings**: Ensure consistent vector quality and avoid redundant indexing.

</details>

<details>
<summary><b>Integration Strategy</b> (Click to expand)</summary>

> Azure AI Search is designed to integrate seamlessly with external embedding pipelines. Here's how to build a modular and scalable setup:

- **Generate embeddings externally** using models from Azure OpenAI (`text-embedding-3-large`, `text-embedding-3-small`), Voyage AI (`voyage-3`, `voyage-multilingual-2`), or Cohere (`embed-v3` series).
- **Store embeddings** in Azure AI Search vector fields, which are optimized for fast similarity search and scalable indexing.
- **Query using embedded vectors** to perform semantic matching, enabling intelligent document retrieval, contextual search, and RAG workflows.
- **Automate updates**: Use Azure Functions or Logic Apps to refresh embeddings when documents change, keeping your index up-to-date.

> Example Workflow:

1. Use `text-embedding-3-large` to embed support tickets.
2. Store vectors in Azure AI Search.
3. Query with user questions to retrieve semantically similar tickets.
4. Combine with keyword filters for precision.

</details>


<!-- START BADGE -->
<div align="center">
  <img src="https://img.shields.io/badge/Total%20views-1301-limegreen" alt="Total views">
  <p>Refresh Date: 2026-04-06</p>
</div>
<!-- END BADGE -->
