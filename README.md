# PDF-Study-Assistant
An AI-powered study tool that lets you chat with your PDFs and generate personalized study plans — all in a clean Streamlit interface.
✨ Features
🔍 PDF Q&A

Upload one or more PDF files
Ask natural language questions and get context-aware answers
Powered by FAISS vector search + HuggingFace embeddings

🗓️ Smart Study Planner

Upload your syllabus or notes PDF
Set your exam date and daily study hours
Mark your weak topics
Get an AI-generated plan with priority rankings, time allocation, and weak topic tips
Download your study plan as a .txt file

🛠️ Tech Stack
LayerTechnologyFrontendStreamlitEmbeddingsHuggingFace all-MiniLM-L6-v2Vector StoreFAISSText SplittingLangChain RecursiveCharacterTextSplitterLLM (primary)Groq — llama-3.1-8b-instantLLM (fallback)Google Gemini — gemini-2.0-flashPDF ParsingPyPDF2

🚀 Getting Started
1. Clone the repository
bashgit clone https://github.com/your-username/pdf-study-assistant.git
cd pdf-study-assistant
2. Install dependencies
bashpip install -r requirements.txt
3. Set up environment variables
Create a .env file in the root directory:
envGOOGLE_API_KEY=your_google_api_key_here
GROQ_API_KEY=your_groq_api_key_here   # Optional, but preferred

Note: If GROQ_API_KEY is set, it takes priority. Otherwise the app falls back to Google Gemini.

4. Run the app
bashstreamlit run app.py

📦 Requirements
streamlit
PyPDF2
langchain-text-splitters
langchain-huggingface
langchain-community
faiss-cpu
google-genai
groq
python-dotenv
sentence-transformers

You can generate this file with pip freeze > requirements.txt after installing packages.


📖 Usage
PDF Q&A Mode

Select PDF Q&A from the sidebar
Upload your PDF(s) and click Process PDFs
Type your question in the input box and get an answer

Study Planner Mode

Select Study Planner from the sidebar
Set your exam date and daily study hours
Upload your syllabus/notes PDF
(Optional) List topics you're weak in
Click Generate Study Plan
Download your plan with the Download button


🔑 API Keys
KeyWhere to GetGROQ_API_KEYconsole.groq.comGOOGLE_API_KEYaistudio.google.com

⚠️ Known Limitations

FAISS index is saved locally (faiss_index/) and is not persistent across server restarts in cloud deployments
PDF text extraction may be incomplete for scanned/image-based PDFs
Study plan quality depends on how well the syllabus PDF is structured


🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.
