
# 🤖 Review-QA Assistant – AI-Powered Insight Generator using RAG

An intelligent assistant that answers natural language questions based on real-world reviews using **Retrieval-Augmented Generation (RAG)**. This project is built using **LangChain**, **Ollama**, and **ChromaDB** to provide meaningful, context-rich responses grounded in actual review data.

> 🍕 **Example Use Case**: This demo uses pizza restaurant reviews, but you can replace the dataset with any domain (e.g., product feedback, hotel reviews, course feedback).

---

## 🌟 Features

- ⚡️ Answers questions based on context from your own data.
- 🧠 Uses embeddings to understand and retrieve relevant information.
- 🔄 Combines retrieval and generation (RAG pipeline).
- 🔌 Easily replaceable dataset (CSV).
- 💻 Runs locally using Ollama – no need for cloud LLM APIs.

---

## 🧱 Tech Stack

- **[LangChain](https://www.langchain.com/)** – LLM orchestration framework.
- **[Ollama](https://ollama.com/)** – Local LLM runtime with support for various models.
- **[ChromaDB](https://www.trychroma.com/)** – Vector database for storing and retrieving embeddings.
- **Pandas** – Data preprocessing and manipulation.
- **Python** – Core language for backend logic.

---

## 📁 Project Structure

```
.
├── main.py                          # Main interface – asks questions via CLI
├── vector.py                        # Sets up vector store from CSV data
├── realistic_restaurant_reviews.csv # Example dataset: Pizza reviews
├── requirements.txt                 # Required Python packages
```

---

## 🚀 Getting Started

### ✅ Prerequisites

- Python 3.8+
- [Ollama](https://ollama.com) installed locally
- Git

Ensure Ollama is running, and these models are available:

- `llama3.1` – For answering questions
- `mxbai-embed-large` – For embedding reviews

> 📌 You can download them using:
> ```bash
> ollama run llama3
> ollama run mxbai-embed-large
> ```

---

### 📦 Installation

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/review-qa-assistant.git
cd review-qa-assistant
```

2. **Install dependencies**

We recommend using a virtual environment.

```bash
pip install -r requirements.txt
```

---

### ▶️ Run the Assistant

```bash
python main.py
```

You'll see a prompt:

```
Ask your question (q to quit):
```

Type your question based on the review data and get AI-powered responses.

---

## 🧪 Sample Questions

Try asking:

- "What do people say about the crust?"
- "Is the restaurant good for families?"
- "Are customers satisfied with the service?"

You can adapt these to any dataset (e.g., "What do students say about the Python course?" if using course reviews).

---

## 🛠️ Customize with Your Own Data

Want to use your own reviews or documents?

1. Replace `realistic_restaurant_reviews.csv` with your dataset.
2. Ensure the CSV has the following columns:
   - `Title`
   - `Review`
   - Optionally: `Rating`, `Date`

3. On first run, the script will create vector embeddings and save them in a local ChromaDB directory (`./chrome_langchain_db`).

---

## ⚙️ Configuration

The app uses:

- `llama3.1` via Ollama for LLM
- `mxbai-embed-large` for embeddings
- `ChromaDB` to retrieve top 5 relevant documents per question

If needed, you can tweak the prompt or retriever settings inside `main.py` and `vector.py`.

---

## 👨‍💻 Author

Developed with ❤️ by Rishi Raj

If you like this project, give it a ⭐️ on GitHub and feel free to contribute!

---
