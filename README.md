
# 🤖 Generative AI-Powered YouTube Video Q&A System

This project is a web application that allows users to ask questions about the content of any YouTube video. It uses a Retrieval-Augmented Generation (RAG) pipeline to fetch the video's transcript, create a knowledge base, and then answer queries based **only** on the information within that video.

## ✨ Key Features

* **YouTube Transcript Fetching:** Automatically retrieves the English transcript for a given YouTube video URL.
* **Context-Aware Q&A:** Answers user questions using a Generative AI model, with the answers grounded strictly in the video's content.
* **Semantic Search:** Uses a vector store to perform efficient searches for the most relevant parts of the transcript.
* **Intuitive Web UI:** A user-friendly interface built with **Streamlit** for easy interaction.

## ⚙️ Technology Stack

* **Framework:** **Streamlit** for the web application UI.
* **Orchestration:** **LangChain** for building the RAG pipeline.
* **Embeddings:** **Hugging Face**'s `sentence-transformers/all-MiniLM-L6-v2` model.
* **Vector Store:** **FAISS** for a high-performance in-memory index.
* **Language Model (LLM):** **Hugging Face**'s `HuggingFaceH4/zephyr-7b-beta`.
* **Transcript API:** `youtube-transcript-api`.
* **Language:** Python 3.8+

## 🚀 Setup and Installation

### Step 1: Clone the Repository

git clone [https://github.com/your-username/your-project-name.git](https://github.com/your-username/your-project-name.git)
cd your-project-name
Step 2: Create a Virtual Environment
It is recommended to use a virtual environment to manage dependencies.


python -m venv venv
# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate

Step 3: Install Dependencies
Install all the required libraries from the requirements.txt file.

pip install -r requirements.txt

Step 4: Set Your API Token
You will need a Hugging Face API token to use the model and embeddings.

Go to the Hugging Face settings page and create a new token.

Set this token as an environment variable.

On Windows:

PowerShell

$env:HUGGINGFACEHUB_API_TOKEN="your_huggingface_token_here"
On macOS/Linux:

Bash

export HUGGINGFACEHUB_API_TOKEN="your_huggingface_token_here"
▶️ How to Run the App
With your virtual environment active and the API token set, run the Streamlit application:

Bash

streamlit run app.py
Your web browser will automatically open to the application, typically at http://localhost:8501.

### requirements.txt

You can generate this file from your environment, or just create a new file named `requirements.txt` with the following content:

streamlit

youtube-transcript-api

langchain

langchain-huggingface

langchain-community

faiss-cpu

sentence-transformers
