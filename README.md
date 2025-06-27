# 🚀 PDF QA with Gemini Flash 1.5 + HuggingFace

Welcome to the ultimate, mind-blowing, next-generation PDF Question Answering CLI! This project leverages the power of Google Gemini Flash 1.5, HuggingFace, and LangChain to turn your boring PDFs into an interactive, AI-powered knowledge base. Ask anything, get instant answers, and feel like a true AI overlord! 🤖📚✨

## ✨ Features

- ⚡ **Supercharged PDF Ingestion:** Instantly process any PDF and generate high-quality embeddings using Google Generative AI.
- 🚀 **Lightning-fast QA:** Ask natural language questions about your PDF and get answers in seconds, powered by Gemini Flash 1.5.
- 💾 **Persistent Vectorstore:** Your knowledge base is saved and ready for instant querying.
- 🖥️ **CLI Simplicity:** No web UI, no distractions. Just pure, raw, terminal power.
- 🪟 **Windows-Ready:** Designed and tested for Windows environments.
- 🐍 **Open Source Magic:** 100% Python, 100% hackable.

## 🛠️ Requirements

- 🐍 Python 3.10+
- 📦 pip
- 🔑 Google API Key (for Gemini)

## ⚙️ Installation

1. **Clone this repository:**
   ```bash
   git clone <your-repo-url>
   cd QA-PDF-Gemini
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up your environment variables:**
   - Copy the provided `.env` file or create one in the root directory:
     ```env
     LANGCHAIN_PROJECT=disabled
     ```

## ⚡️ Environment Variable Setup

Before running the project, make sure to set your Google API key in your environment. You can do this in your terminal:

- On Linux/Mac:
  ```bash
  export GOOGLE_API_KEY=your_google_api_key_here
  ```
- On Windows:
  ```cmd
  set GOOGLE_API_KEY=your_google_api_key_here
  ```

Or simply edit the `.env` file as shown above.

## 🚦 Usage

### 🏁 Start the CLI

```bash
python cli.py
```

You will see a beautiful banner and a list of available commands:

```
🧠 PDF QA con Gemini Flash 1.5 + HuggingFace
Comandos disponibles:
  upload <ruta_pdf>   -> Procesa el PDF y genera embeddings (reemplaza vectorstore)
  ask <pregunta>      -> Haz una pregunta sobre el PDF
  exit                -> Salir
```

### 💡 Commands

- 🗂️ **upload <ruta_pdf>**
  - Example:
    ```bash
    upload docs/prueba-teoria.pdf
    ```
  - Processes the PDF, generates embeddings, and creates a new vectorstore. Uploading a new PDF will replace the previous vectorstore.

- ❓ **ask <pregunta>**
  - Example:
    ```bash
    ask What is the main topic of the document?
    ask ¿Cuál es el resumen del PDF?
    ```
  - Ask anything about your PDF! The AI will answer instantly. 🤖

- 👋 **exit**
  - Example:
    ```bash
    exit
    ```
  - Gracefully closes the CLI. You are now an AI master. 🧙‍♂️

## 🧩 Troubleshooting

- 🛑 **File lock errors on Windows:**
  - If you see errors about files being in use, simply close and reopen the CLI. Windows sometimes holds file locks longer than expected.
- 📄 **No PDF loaded:**
  - Make sure to upload a PDF before asking questions.
- 🔑 **API Key issues:**
  - Double-check your `.env` file and ensure your Google API key is valid.

## 🧬 How it Works (Under the Hood)

- 📄 **PDF Ingestion:** Uses PyMuPDF to load and split your PDF into chunks.
- 🧠 **Embeddings:** GoogleGenerativeAIEmbeddings creates vector representations of each chunk.
- 🗃️ **Vectorstore:** ChromaDB stores the embeddings for fast retrieval.
- 🤖 **QA Chain:** LangChain's RetrievalQA with Gemini Flash 1.5 answers your questions using the most relevant chunks.

## 🏆 Why is this Project Awesome?

- It turns static PDFs into living, breathing, AI-powered documents. 🦾
- It uses the latest in LLM and vector search technology. 🧬
- It's blazing fast, easy to use, and highly extensible. ⚡
- You can finally get answers from your PDFs without reading them! 📖➡️🤖

## 🤝 Contributing

Feel free to fork, hack, and submit PRs. The more, the merrier! 🎉

## 📜 License

MIT. Use it, abuse it, make it better.

---

**Unleash the power of Gemini Flash 1.5 on your PDFs. Become the oracle of your own documents! 🔮**
