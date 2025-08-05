# 📄 Chat with PDF (Open Source Model)

A simple web app that lets you upload a PDF and ask questions about its content using open-source machine learning models. No OpenAI API key or paid service required!

---

## 🚀 Features

- **Upload any PDF** and ask questions about its content.
- Uses **open-source NLP models** for question answering (`distilbert-base-cased-distilled-squad`).
- **Semantic search** with sentence embeddings to find relevant sections in the PDF.
- Powered by [Gradio](https://gradio.app/) for an interactive and user-friendly web interface.
- Runs locally or in Colab — **no secrets or paid keys required**.

---

## 🛠️ How It Works

1. **PDF Upload**: The user uploads a PDF file via the Gradio interface.
2. **Text Extraction**: The PDF is read and split into manageable chunks.
3. **Semantic Chunk Search**: Each chunk is embedded using a sentence transformer. When a question is asked, the app finds the most relevant chunks using semantic similarity.
4. **Question Answering**: The selected chunks and the question are passed to an open-source QA model to generate an answer.
5. **Response**: The answer is displayed to the user.

---

## 📦 Installation

You can run this project in [Google Colab](https://colab.research.google.com/) or locally.

### Requirements

- Python 3.8+
- pip

### Dependencies

- `transformers`
- `sentence-transformers`
- `gradio`
- `PyPDF2`
- `scikit-learn`
- `numpy`

### Quickstart (Colab)

Just open the notebook in Colab and run all cells!

### Quickstart (Locally)

```bash
pip install transformers sentence-transformers gradio PyPDF2 scikit-learn numpy
python Chat_with_pdf.ipynb
```
Or convert the notebook to a script:
```bash
jupyter nbconvert --to script Chat_with_pdf.ipynb
python Chat_with_pdf.py
```

---

## 📝 Usage

1. Launch the app (`iface.launch()` will display a link or open a local browser window).
2. Upload your PDF.
3. Ask any question about its content in natural language.
4. Get instant answers!

---

## 🧠 Models Used

- **QA Model:** [`distilbert-base-cased-distilled-squad`](https://huggingface.co/distilbert-base-cased-distilled-squad)
- **Embedding Model:** [`all-MiniLM-L6-v2`](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2)

Both models are available for free from [Hugging Face Hub](https://huggingface.co/).

---

## 🔒 Security

- **No API keys or secrets required.**
- Your data stays local (unless you run on Colab or share the Gradio link).
- Do **not** upload confidential PDFs to public/shared demos.

---

## 💡 Customization

- Swap out the QA model with any other Hugging Face-compatible question-answering model.
- Adjust chunk size or top-k search as needed for your use case.

---

## 🤝 License

This project is open source under the [MIT License](LICENSE).

---

## 🙋‍♂️ Acknowledgements

- [Gradio](https://gradio.app/)
- [Hugging Face](https://huggingface.co/)
- [Sentence Transformers](https://www.sbert.net/)
- [PyPDF2](https://pypdf2.readthedocs.io/)

---

## ⭐️ Star this project if you find it useful!
