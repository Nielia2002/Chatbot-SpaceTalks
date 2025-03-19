# **RAG-Based Space Chatbot** 🛸🌌

A retrieval-augmented chatbot integrating **vector search**, **NLP**, and **generative models** to deliver human-like answers about space, astronauts, exoplanets, and more. Perfect for cosmic exploration fans! 🪐

---

## **Overview**

1. **Data Collection & Preprocessing** ✨
   - Merged multiple space datasets (astronauts, exoplanets, rovers) into a single repository.
   - Generated **384-dimensional embeddings** for each text chunk.

2. **Vector Database (Pinecone)** 🔭
   - Stores embeddings for fast semantic search.
   - Returns top chunks for user queries.

3. **Generative Model (Hugging Face)** 🤖
   - Uses `all-MiniLM-L6-v2` for embeddings and a FLAN-T5 model for answers.
   - Hugging Face’s **InferenceClient** for high-quality text generation.

4. **RAG Workflow** 🎯
   - **Retrieve**: Convert query → embedding → Pinecone → relevant text chunks.
   - **Augment**: Combine retrieved context + query.
   - **Generate**: Send it to the model → get a conversational answer.

---

## **Key Features**

- **Interactive Q&A** 🗨️: Ask space-related questions in real time.
- **Semantic Search** 🔎: Embeddings for more accurate chunk retrieval.
- **Modular & Scalable** 🛠️: Easily swap models, update data, or re-index.
- **No Vendor Lock-In** 🧩: Choose local inference or Hugging Face.

---

## **Architecture**

1. **Data & Embeddings** 📝
   - Preprocessed CSVs covering astronauts, exoplanets, missions.
   - 384-d embeddings with `all-MiniLM-L6-v2`.

2. **Vector Database** 🏦
   - Pinecone index `bbc-384` holding all embeddings.
   - Queries provide text chunk metadata.

3. **Generative Model** 🤖
   - Hugging Face FLAN-T5.
   - Inference with `InferenceClient` for natural language output.

---

## **Project Setup**

1. **Clone or Download** this repository.
2. **Install Dependencies** 🛠️:
   ```bash
   pip install -r requirements.txt
   ```
3. **Set Up API Keys** 🔑:
   - Pinecone (for vector DB) & Hugging Face (for inference).
4. **Run the Chat** 🕹️:
   ```bash
   python rag_chat.py
   ```
   Type questions in the console.

---

## **Usage**

- **Sample Queries**:
  - "Who was the first astronaut in space?"
  - "Give me details on the Mars rovers."
  - "Which exoplanet has the largest mass?"
- **Quit**: Type `exit` or `quit`.

---

## **Project Status**

- **Currently**: Provides real-time Q&A with relevant context.
- **Potential Enhancements**:
  - Fine-tune for more specialized knowledge.
  - Re-ranking or advanced prompt engineering.
  - Add a web UI.

---

## **Contributing** 🪐
1. **Fork** & **Clone**.
2. Create a feature branch.
3. Commit & push changes.
4. Submit a PR.

---

## **License**

Released under the [MIT License](LICENSE). Feel free to modify and distribute.

---

## **Acknowledgments**

- Pinecone for vector search.
- Hugging Face for Transformers & InferenceClient.
- NASA & ESA for open space data.

---

**Enjoy your cosmic Q&A adventures!** 🌠🛰️

