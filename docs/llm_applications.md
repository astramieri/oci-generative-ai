# LLM Applications

Here are listed some LLM applications.

## Retrieval Augmented Generation (RAG)

**Retrieval Augmented Generation (RAG)** are primarily used in QA where the model has access to support documents for a query.

In a RAG system, typically:
1. a system user provides an input (e.g. a question)
2. the system transforms the input into a query which will be used to search a database (e.g. a corpus of documents)
3. the search returns documents that contain the answer to the question (or are otherwise relevant)
4. the returned documents are provided to the LLM as input in addition to the question
5. the model generates the correct answer

RAG systems, as opposed to systems that do not leverage an external corpus of documents, **tend to hallucinate less**. If we give the LLM a question and then some text that contains the answer, it should be easier to answer the question by leveraging the text than answering it based solely on the documents it has seen during pre-training.

RAG systems are also elegant because they provide a **non-parametric mechanism for improvement**. By non-parametric, what I mean is that we don't have to touch the model at all to improve the system. All we have to do is add more documents.

RAG systems are used for a variety of tasks:
- dialogue
- question-answering
- fact-checking
- etc.

## Code Models

