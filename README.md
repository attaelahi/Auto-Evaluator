# `Auto-Evaluator` :brain: :memo:
The Auto-Evaluator is a sophisticated tool designed to automate the evaluation process for question-answering systems. Leveraging advanced natural language processing (NLP) techniques and machine learning models, this tool streamlines the assessment of a system's performance on a given set of documents and associated questions.

# Features
Document Processing: The Auto-Evaluator can ingest documents in various formats, including PDF and plain text, extracting relevant text for evaluation.

Question Generation: It automatically generates a set of evaluation questions based on the content of the provided documents, ensuring comprehensive coverage.

Model Evaluation: The tool employs state-of-the-art language models to answer the generated questions, providing insights into the system's ability to comprehend and respond accurately.

Retrieval Assessment: In addition to answering questions, the Auto-Evaluator evaluates the relevance of retrieved documents, offering a holistic view of the system's performance.

Configurability: Users can customize various parameters such as chunk size, overlap, model type, retriever type, and embedding type to tailor the evaluation process according to their requirements.

Grading: The tool employs grading prompts to assess the quality of both answers and retrieved documents, providing detailed feedback on performance.

Visualization: It offers visual representations of evaluation results, including latency, retrieval scores, and answer scores, facilitating easy interpretation and comparison.

This is a lightweight evaluation tool for question-answering using Langchain to:

- Ask the user to input a set of documents of interest

- Apply an LLM (`GPT-3.5-turbo`) to auto-generate `question`-`answer` pairs from these docs

- Generate a question-answering chain with a specified set of UI-chosen configurations

- Use the chain to generate a response to each `question`

- Use an LLM (`GPT-3.5-turbo`) to score the response relative to the `answer`

- Explore scoring across various chain configurations

**Run as Streamlit app**

`pip install -r requirements.txt`

`streamlit run auto-evaluator.py`

**Inputs**

`num_eval_questions` - Number of questions to auto-generate (if the user does not supply an eval set)

`split_method` - Method for text splitting

`chunk_chars` - Chunk size for text splitting
 
`overlap` - Chunk overlap for text splitting
  
`embeddings` - Embedding method for chunks
 
`retriever_type` - Chunk retrieval method

`num_neighbors` - Neighbors for retrieval 

`model` - LLM for summarization of retrieved chunks 

`grade_prompt` - Prompt choice for model self-grading

# Here are the Screenshots

<img width="955" alt="1" src="https://github.com/attaelahi/Auto-Evaluator/assets/72361631/e4be5f44-8686-4eea-b66c-e18938d59c19">
<img width="956" alt="2" src="https://github.com/attaelahi/Auto-Evaluator/assets/72361631/a146997e-f38b-4c39-95a1-a5641f85147b">
<img width="960" alt="3" src="https://github.com/attaelahi/Auto-Evaluator/assets/72361631/0c6a4bc8-adff-4ab4-9dad-e89c558bd4da">
<img width="958" alt="4" src="https://github.com/attaelahi/Auto-Evaluator/assets/72361631/72c973d9-6720-439b-a69a-c6b1265c12e9">




