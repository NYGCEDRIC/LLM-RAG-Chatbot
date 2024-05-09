# LLM+RAG Workshop Project

Overview

This project is the culmination of the LLM+RAG Workshop, where I learned to integrate Large Language Models (LLMs) with Retrieval-Augmented Generation (RAG) to create a powerful question-answering system. This approach leverages the strengths of both LLMs for natural language processing and RAG for contextually rich information retrieval.

Key Features

Document Indexing: Indexed FAQs from DE Zoomcamp, ML Zoomcamp, and MLOps Zoomcamp using Elasticsearch.
Question Answering: Built a Q&A bot that retrieves relevant information from indexed documents and generates responses using OpenAI's GPT-3.5 model.
Technologies Used: Docker, Python 3.10, Elasticsearch, OpenAI, and Jupyter Notebooks.

# Setup and Installation

Install Dependencies: Use pipenv to manage Python packages.
````
pip install pipenv
pipenv install tqdm notebook==7.1.2 openai elasticsearch
````
Configure OpenAI: Set your OpenAI API key in environment variables.

Run Elasticsearch: Use Docker to start an Elasticsearch instance.
bash
Copy code
docker run -it --name elasticsearch -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" -e "xpack.security.enabled=false" docker.elastic.co/elasticsearch/elasticsearch:8.4.3
Usage
To use the Q&A bot, run the Jupyter notebook elastic-rag.ipynb and input your questions related to the indexed courses. The system retrieves relevant documents and generates responses using the OpenAI model.

Acknowledgments
Special thanks to Alexey Grigorev and DataTalksClub for providing an excellent learning experience in the LLM+RAG workshop. Their guidance and insights were invaluable in understanding and implementing this advanced AI technology.

Next Steps
Experiment with open-source LLMs for further customization.
Develop a user interface, possibly with Streamlit, to enhance interaction.
Deploy the solution for broader accessibility and use.
