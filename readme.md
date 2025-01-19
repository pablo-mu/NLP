# NLP Repository

This repository will contain resources and projects related to Natural Language Processing (NLP).

## Resources

* [AI Agents by Google](AI-Agents-GooglePaper.pdf): This paper presents includes an AI agent overview which covers everything you need to know about this new wave.
    - Introduction to AI Agents
    - The Role of tools in Agents
    - Enhancing model performance with targented learning.
    - Quick start to Agents with LangChain
    - Production applications with Vertex AI agents.

* [Agentic RAG](RAG/Agentic_RAG.ipynb): This notebooks creates a LangChain agentic RAG system using the IBM Granite-3-8b-Instruct model that can answer complex queries about the 2024 US Open Using external information. This is extracted from [github][https://github.com/ibm-granite-community/granite-snack-cookbook/blob/main/recipes/AI-Agents/Agentic_RAG.ipynb]

* [RAG](RAG/RAG_with_Langchain.ipynb): This notebook contains instruction for performing RAG. Also extracted from [github][https://github.com/ibm-granite-community/granite-snack-cookbook/blob/main/recipes/AI-Agents/Agentic_RAG.ipynb].

## Projects

* [Few-Shot Learning](Projects/NLP_Exploration.ipynb): This projects explores the use of few-shot learning in NLP within a 100 sentence dataset. It starts by using spaCy to extract the main topics of each sentence.

Then, sentence embeddings of the main topics are created, and soft-clustering is performed to group similar sentences together. Later, with Hugging Face's `transformers` library and API, the **"Mixtral-8x7B-Instruct-v0.1"** model is used to generate labels for the generated clusters. Moreover, this model is used to generate more sentences for each cluster to increase the dataset size and perform a more realistic few-shot learning.

Finally, the fine-tune with contrastive learning is performed using [SetFit](https://github.com/huggingface/setfit) Model together with [BAAI/bge-small-en-v1.5](https://huggingface.co/BAAI/bge-small-en-v1.5), in order to classify the sentences into the generated clusters.