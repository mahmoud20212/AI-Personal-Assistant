# AI Personal Assistant

## Short Description
AI Personal Assistant is a lightweight question-answering app built on top of OpenAI and LangChain. It reads content from `data.txt` and answers user questions using retrieval over that local data.

## Technologies
- Python 3
- OpenAI API (`openai`)
- LangChain (`langchain`, `langchain-community`, `langchain-openai`)
- Streamlit (`streamlit`, `streamlit_chat`)
- tiktoken
- httpx

## Features
- Answers questions based on the local knowledge file (`data.txt`)
- Retrieval-based responses using embeddings and vector search
- Streamlit chat interface with conversation history
- Command-line script for quick one-shot prompts

## The Process
1. Load text data from `data.txt`.
2. Create embeddings for the loaded content.
3. Build a vector index from the embedded data.
4. Retrieve the most relevant chunk for each user question.
5. Generate a final answer using an OpenAI-powered model.

## Running the Project
### 1. Install dependencies
```bash
pip install -r requirements.txt
```

### 2. Set environment variable
Windows (Command Prompt):
```bat
set OPENAI_API_KEY=your_api_key_here
```

Windows (PowerShell):
```powershell
$env:OPENAI_API_KEY="your_api_key_here"
```

### 3. Run the Streamlit chat app
```bash
streamlit run chatbot.py
```

### 4. Run the command-line version
```bash
python app.py "Your question here"
```
