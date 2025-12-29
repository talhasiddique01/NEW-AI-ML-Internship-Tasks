# Task 4: Context-Aware Chatbot Using LangChain / RAG

## Objective
The goal of this task is to build a conversational chatbot that can:
- Maintain conversation context over multiple interactions.
- Retrieve relevant information from an external knowledge base or document corpus.
- Generate accurate, contextually aware responses using Retrieval-Augmented Generation (RAG).

## Methodology / Approach
1. **Data Preparation:**  
   - Collected a custom corpus (e.g., Wikipedia pages, internal documentation).  
   - Cleaned and preprocessed the text for embedding.

2. **Document Embedding:**  
   - Converted the text into vector embeddings using OpenAI embedding models (`text-embedding-ada-002`).  
   - Stored embeddings in a FAISS vector database for fast similarity search.

3. **Retrieval-Augmented Generation (RAG):**  
   - When a user asks a question, the system retrieves the most relevant documents from the vector store.  
   - The retrieved context and user query are fed into an LLM to generate accurate answers.

4. **Context Memory:**  
   - Implemented conversational memory to track the chat history.  
   - Short-term memory retains the last few interactions for context-aware responses.  
   - Long-term memory (optional) can store important facts for personalized interactions.

5. **Chatbot Deployment:**  
   - Used LangChain to orchestrate the RAG pipeline.  
   - Deployed the chatbot on Streamlit for an interactive interface where users can input queries and see responses in real-time.

## Key Results / Observations
- The chatbot maintains context across multiple interactions effectively.  
- Retrieval from vectorized documents ensures answers are accurate and grounded in the source material.  
- RAG improves the quality and relevance of responses compared to generative-only LLMs.  
- Streamlit provides a simple, interactive UI to test and deploy the chatbot.

## Skills Gained
- Conversational AI development  
- Document embedding and vector search  
- Retrieval-Augmented Generation (RAG)  
- LLM integration and deployment using Streamlit
