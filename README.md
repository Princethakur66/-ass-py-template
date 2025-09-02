# -ass-py-template
RAG-QA is a free, containerised question-answer framework that allows you to ask questions to your documents in an intuitive way.
This app uses a method called retrieval augmented generation (RAG) to retrieve information that is relevant to your question from your uploaded document. It then uses a large language model (LLM) to answer the question with the retrieved context.

The current implementation uses the following components:

LLM: Google Gemini Pro
Embedding Model: all-MiniLM-L6-v2
Vector Database: Chroma DB
Frontend: Streamlit
Backend: FastAPI
Demo
This demo shows the app answering a question related to Alphabet Inc's Q3 financial result from 2023. Notice the app frontend is shown on the left; the logs are shown on the upper right; the PDF report is shown on the bottom left.
https://github.com/ruankie/rag-qa/blob/main/assets/demo.gif
Usage
Note: The first time you run this, it might take a while to build all the images and download the embedding models.

You will need an API key from OpenAI or Google. You can create one for free here:

Google - to use models like Gemini (Recommended since it's free)
OpenIA - to use models like GPT4
Set up your API keys in a file called .env (see .env.example for an example)

Now set up the backend and frontend

docker compose up
Navigate to the frontend in your browser: http://localhost:8501/

Upload a PDF document that you would like to ask a question about

Ask a question in the chat input section and wait for a response

Development
(Optional) Download and install asdf on your machine to manage the version of Python and Poetry used in this project. Once done, run asdf install to install the versions specified in .tool-versions. Alternatively, install them manually as described below:
Install Poetry on your machine
Install Python 3 on your machine
Create a virtual environment for your project using the command poetry install. This will install all the basic dependencies specified in your pyproject.toml file.
Set up your API keys in a file called .env (see .env.example for an example)
When you run your backend and frontend containers locally, use docker compose up --build to ensure the latest changes are reflected in the containers.
