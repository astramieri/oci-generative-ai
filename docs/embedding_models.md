# Embedding Models

Embeddings are **numerical representations** of a piece of text converted to number sequences. Embeddings make it easy for computers to understand the relationship between pieces of text.

A piece of text could be:
- a word
- a phrase
- a sentence
- a paragraph
- an entire document

**Encoders** are designed to take a piece of text and convert it into a vector. In the image, there is a vector for each of the words, and there is also a vector representation for the sentence. 

The real use case is **translation**, which is a sequence-to-sequence task. 

![Embedding](../images/embedding.png)


## Word Embeddings

Word Embeddings capture **properties** of the world.

Actual embedding represent more properties (coordinates) that just two. 

The rows of coordinates are called vectors and represented as numbers.

![Word embeddings - Example](../images/word_embeddings_graph.png)

![Word embeddings - Table](../images/word_embeddings_table.png)

## Semantic Similarity

The **numerical similiarity** is a number that measures the similarity between two embeddings (which are numbers). *Cosine Similarity* and *Dot Product Similarity* can be used to compute the numerical similiarity.

Embeddings that are numerically similar are also **semantically similar**. Semantically similar basically means how close their meaning is or how closely they are related. 

![Semantic Similarity](../images/semantic_similarity.png)
 
