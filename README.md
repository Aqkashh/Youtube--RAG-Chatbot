# YouTube RAG Chatbot

This project is an AI-powered chatbot that answers questions based on the transcript of any YouTube video, using a RAG (Retrieval-Augmented Generation) pipeline built with LangChain, Hugging Face, and ChromaDB.


 Features
 
1. Fetches transcripts from any YouTube video (with captions)

2. Splits transcripts into overlapping chunks for better context

3. Stores chunks in a Chroma vector database

4. Embeds user questions and performs similarity search

5. Sends context + question to an LLM (DeepSeek-R1-0528 or any Hugging Face model)

6. Supports local DB persistence and multi-video ingestion


Tech Stack

1. Python 3.10+

2. LangChain (core, community, HuggingFace)

3. Hugging Face Transformers

4. ChromaDB (Vector DB)

5. YoutubeTranscriptApi

6. dotenv


Setup Instructions

1. Clone the repository
   
   git clone https://github.com/Aqkashh/Youtube--RAG-Chatbot


2. Create and activate a virtual environment
   
    python -m venv venv
    venv\Scripts\activate

4. Install all dependencies
   
     pip install -r requirements.txt
 
6. Add your Hugging Face API key to .env

     Create a .env file in the app/ directory:

     HUGGINGFACEHUB_API_TOKEN=your_huggingface_token_here


How to Use

Step 1: Ingest YouTube Transcript and Store in DB

python app/run_ingest_and_split.py

Paste a YouTube URL with subtitles when prompted.

Step 2: Ask Questions Based on That Video

python app/test_rag.py

Type your question and get an answer based on the video transcript.

Notes

Make sure the YouTube video has subtitles (captions) available.

ChromaDB automatically persists vectors in the db/ folder.

License

MIT License — feel free to use and build upon this project!

