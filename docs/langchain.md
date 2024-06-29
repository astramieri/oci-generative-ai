# LangChain

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

![Langchain](../images/langchain.png)

## LangChain Models

 There are two main types of models that LangChain integrates with:
 - **LLMs**
    - they refer to pure text **completion models**
    - they take a string prompt as input and output a string completion
    
 - **Chat Models**
    - they are often backed by LLMs but **tuned specifically for having conversations** (i.e. exchange of messages)
    - they take a list of chat messages as input, and they return a message as output

## LangChaing Prompts

LangChain has pre-built classes to create prompts. These are called as **prompt templates** and they are predefined recipes for generating prompts for language models.

Tipically, language models expect the prompts to either be a *string* or else a *list of chat message*:
- **String Prompt Template** 
    - it creates the input from a combination of fixed text input and variables
- **Chat Prompt Template**
    - it creates the input from a list of chat messages
    - each chat message is associated with *content* and an additional parameter called *role*

E.g. String Prompt Template

    prompt_template = PromptTemplate.from_template(
        "Tell me a {adjective} joke about {content}."
    )

E.g. Chat Prompt Template

    chat_template = ChatPromptTemplate.from_messages(
        [
            ("human", "Hello, how are you doing?"),
            ("ai", "I'm doing well, thanks!")
        ]
    )

## LangChain Chains

LangChain provides framework for creating **chains of component**, including LLMs and other type of components. 

Chains can be composed in two ways:
- **LangChain Expression Language (LCEL)**
    - it is a declarative and preferred way to create chains
- **Legacy** 
    - LangChain Python classes like LLM Chain