# SQL Query Helper
An AI-Powered Chatbot for SQL Learning and Assistance

# Project Overview
The SQL Query Helper is an AI-driven chatbot designed to support SQL learners and educators. Leveraging Retrieval-Augmented Generation (RAG), the chatbot provides precise, contextually relevant answers to SQL-related questions while enhancing the learning experience for students and easing the workload for educators.

# Key Features
### For Students:
1. **24/7 Support**: Assistance with SQL queries, syntax guidance, and SQL problem-solving.
2. **File Interactions**: Upload files (CSV, DOCX, PDF) for batch processing of questions and answers.

### For Teachers:
1. **Automated Workflows**: Save time with automated question generation, grading, and feedback.
2. **File Interactions**: Process multiple SQL questions and evaluate student responses in bulk.

### Shared Features:
- **Role-Based Access**: Custom features for students and teachers.
- **User-Friendly Interface**: Built using Streamlit for seamless interaction.


# Architecture
The SQL Query Helper architecture uses a Retrieval-Augmented Generation (RAG) approach to assist users with SQL-related questions. This setup combines retrieval and generation components to create an efficient and accurate response system.

![ARCHITECTURE DIAGRAM](https://github.com/user-attachments/assets/80b29e46-5eaa-4c82-8348-b173e5efe763)

1. **Large Corpus:** A dataset with SQL docs, examples, and learning materials is split into smaller, manageable chunks.
2. **Chunk Embeddings:** Each chunk is converted into a vector representation using an embedding model like MiniLM, capturing its semantic meaning.
3. **Storage:** The embeddings are stored in a NumPy array, serving as a lightweight knowledge base.
4. **User Query:** When a question is asked, it is embedded similarly to match the format of stored embeddings.
5. **Similarity Search:** A cosine similarity search identifies chunks most relevant to the query.
6. **Response Generation:** Mistral-7B processes the query and relevant chunks to generate a detailed answer.
7. **CHAT Interface:** The tailored response is returned to the user for interaction.

# Features in detail
### Student Features:
- **Ask Questions**: Type SQL queries for instant responses.
- **Generate Responses**: Upload SQL question files and download AI-generated answers.

### Teacher Features:
- **Ask Questions**: Type SQL queries for instant responses.
- **Generate Responses**: Upload SQL question files and download answers.
- **Check Responses**: Upload student answers for evaluation and feedback.
- **Generate Questions**: Create SQL-related questions automatically based on topics.


# Technologies Used
- **Backend**: Python, Hugging Face Transformers, SentenceTransformer, NumPy
- **Frontend**: Streamlit
- **Cloud Storage**: Google Drive
- **Computation**: Google Colab

# Project Sturcture
LLM Project/

├── Dataset.zip               # Compressed dataset for the project

├── load_llm_model_py.py      # Script for loading LLM models

├── model_test_py.py          # Script for testing the LLM

├── ui.py                     # Script for the user interface

# Future Enhancements
1. Integration of a vector database for faster retrieval.
2. Regular updates to the SQL knowledge base for best practices.
3. Improved error handling for complex queries.

# LICENSE
This project is licensed under the MIT License. See the LICENSE file for details.

