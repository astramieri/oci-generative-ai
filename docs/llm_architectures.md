# LLM Architectures

The are two major architectures for language models:
- **encoders**
- **decoders**

These architectures largely correspond to two different tasks or model capabilities:

- **embedding** 

    Embedding text is the process of converting a sequence of words into a single vector or a sequence of vectors. In other words, an embedding of text is a **numeric representation of the text** that typically tries to capture the semantics or meaning of the text. 

- **text generation**

    Text generation is pretty self-explanatory. The input to a text generation model is a sequence of words, and the output is a generated sequence of words.

These models are based on an underlying **transformer architecture**, which was popularized in the paper *Attention Is All You Need* which came out in 2017.

Encoders and decoders can come in all different kinds of sizes. In the realm of language models, **size refers to the number of trainable parameters** that the model has. The decoder models tend to be pretty large, especially compared to the relatively smaller encoders. 

![Model Ontology](../images/model_ontology.png)