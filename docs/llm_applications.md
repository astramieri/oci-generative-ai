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

RAG systems are also elegant because they provide a **non-parametric mechanism for improvement**. By non-parametric means we don't have to touch the model at all to improve the system. All we have to do is add more documents.

RAG systems are used for a variety of tasks:
- dialogue
- question-answering
- fact-checking
- etc.

## Code Models

**Code Models** are LLMs trained on code, comments, and documentation.  These models have demonstrated amazing capabilities in terms of code completion and documentation completion. 

Arguably, code completion might be easier than general text completion. One potential reason for this is that generating code is narrower in scope than generating arbitrary text. Code is more structured, more repetitive and less ambiguous than natural language.

These models largely eliminate the need to write any boilerplate code and commonly written functions or variables or variations of such functions. Moreover, they also shine when programming in a language that you don't know well. Instead of using a search engine to continually look up language syntax and functions, just ask the model to write the code for you.

## Multi-Modal Models

**Multi-Modal Models** are trained on multiple data modalities, for example text, images, and audio. These models can produce images or even video from textual descriptions and perform similar types of tasks.

**Diffusion Models** can generate images all at once rather than one pixel at a time. The way they do this is by starting with an image that is simply noise (it's not an image of anything at first) and iteratively refining all the pixels in the image simultaneously until a coherent image emerges.

## Language Agents

**Language Agents** are models that are intended for sequential decision-making scenarios, for example playing chess, operating software autonomously, or browsing the web in search of an item expressed in natural language. Language agents are an extension of the classic work on machine learning agents. In this newer rendition, the systems being built also utilize LLMs.

In more detail, these models operate in what's known as an environment and iteratively take actions in pursuit of accomplishing a specific goal. The model continues taking actions until it thinks that it has achieved its goal, at which point, it terminates.

One of the canonical works in this space is known as **ReAct** which proposes a framework for leveraging LLMs as language agents. A key ingredient of this work is to prompt the model to emit what they call thoughts, which are summaries of the goal, what steps the model has already accomplished, and what steps the model thinks it needs to take next.

There has been significant study of teaching LLMs how to leverage tools like APIs or other programs to perform computation. For example, instead of doing some arithmetic by decoding, an LLM could generate some text expressing the intention to use a calculator, formulate an API call to perform the arithmetic, and then consume the result. The ability to use tools promises to greatly expand the capability of LLMs.

Finally, there is a growing body of work developing methods of training LLMs to perform various types of reasoning. LLMs that can reason successfully could be employed as high level planners in these agent systems for accomplishing highly complex, long-horizon tasks. Like humans, agents that can reason could be successful in new environments when trying to accomplish unfamiliar tasks.

