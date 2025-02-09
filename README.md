<h1 align="center">LLM Engineering</h1>

<p align="center">
Notebooks and small apps I built while learning to work with large language models (2024 to 2025): fine-tuning, dataset generation, RAG, agents and serving.
</p>

Some notebooks are written in French.

## Contents

| Folder | What's here |
|---|---|
| [finetuning](finetuning) | Fine-tuning notebooks: Phi-2 with LoRA and TRL's `SFTTrainer` (two versions), Llama 2 for sentiment analysis of financial news, Llama 3 8B with Unsloth on the Alpaca dataset, and representation fine-tuning (ReFT) with `pyreft`. |
| [data-curation](data-curation) | Building instruction datasets from raw text with [augmentoolkit](https://github.com/e-p-armstrong/augmentoolkit) (a copy of the tool and a notebook), and a script that converts JSONL conversations to the Alpaca format. |
| [agentic-ai](agentic-ai) | The LangGraph quickstart (a support chatbot with web search and memory) and [dockerize-langraph-app](agentic-ai/dockerize-langraph-app): a LangGraph ReAct agent on Groq models with Tavily search, served by FastAPI, with a Streamlit UI and a Dockerfile. |
| [deployment](deployment) | [qwen25vl-api](deployment/docker-hf-space/qwen25vl-api): a FastAPI endpoint for Qwen2.5-VL-3B-Instruct, deployed as a Docker Space on Hugging Face. |
| [langchain](langchain) | LangChain experiments from June 2024, listed below. |
| [inference-tests](inference-tests), [multimodal-llms](multimodal-llms), [rag-workflows](rag-workflows) | Placeholders with a README only. |

### LangChain experiments

| Folder | What it does |
|---|---|
| [simple-chatbot](langchain/simple-chatbot) | A Streamlit chatbot on Qwen2 0.5B served by Ollama. |
| [api](langchain/api) | A LangServe API that exposes two prompts on Ollama models (Qwen2 and DeepSeek Coder), with a client. |
| [groq](langchain/groq) | A Streamlit app that answers questions about PDFs with Llama 3 on Groq, a Flask assistant for farmers (prompts in French) on Mistral with a Chroma retriever, and small test scripts. |
| [scraping](langchain/scraping) | Web scraping with BeautifulSoup and Playwright followed by LLM extraction, plus a ScrapeGraphAI version. |
| [simple-rag](langchain/simple-rag) | A RAG notebook with Ollama models and Chroma or FAISS as the vector store. |
| [huggingface](langchain/huggingface) | RAG over a PDF with Hugging Face embeddings and models and FAISS. |
| [Ollama_Server_setting.ipynb](langchain/Ollama_Server_setting.ipynb) | Runs an Ollama server on Colab so the apps above can call it remotely. |

## Running the code

Each app lists its packages in a `requirements.txt` or at the top of the notebook. API keys are read from environment variables (`GROQ_API_KEY`, `TAVILY_API_KEY`, `LANGCHAIN_API_KEY`, `OLLAMA_HOST`). Put them in a `.env` file, which git ignores.

## Credits

[data-curation/augmentoolkit](data-curation/augmentoolkit) is a copy of [e-p-armstrong/augmentoolkit](https://github.com/e-p-armstrong/augmentoolkit) by Evan Armstrong, under the MIT license kept in that folder.
