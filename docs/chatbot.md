# Chatbot

One of the most popular and useful LLM application is a **chatbot** that can answer questions given a set of custom documents.

## Chatbot Architecture

1. Ask chatbot a question
2. Relevant documents from storage are retrieved and used as context
3. Prior questions and answes are also used as context
4. LLM answers using context and question

![Chatbot Architecture](../images/chatbot_architecture.png)

## Langchain

**LangChain** is one of the most popular LLM application development framework to build a chatbot.

It enables applications that are context aware and rely on language model to answer given the question and the context. 

It offers multitude of components that help us build LLM-powered applications with minimal effort.

A few components are:
- LLMs
- prompts
- memory
- chains
- vector stores
- document loaders 

These components are **easily exchangeable** as well. For example, we can switch between, say, one LLM with another LLM with minimal code changes.