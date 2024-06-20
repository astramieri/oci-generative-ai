# Summarization Models

- `command` model from Cohere
    - highly performant, instruction-following conversational model 
    - model parameter: 52B
    - context window(*): 4096 tokens
    - it generates a succinct version of the original text that relays the most important information
    - it is the same as one of the pre-trained foundational text generation models, but it has a separate set of parameters
    - use cases:
        - news articles
        - blog posts
        - chat transcripts
        - scientific articles
        - meeting notes
        - etc.

## Summarization Models Parameters

- **Temperature**
    - it determines how creative the model should be 
    - default is 1 and the maximum is 5
- **Length**
    - it approximates the length of the summary
    - you can choose among: *short, medium, long*
- **Format**
    - you can choose among: *free-form paragraph* or *bullet points*
- **Extractiveness**
    -  it  determines how much to reuse the input in the summary
    - summaries with high extractiveness lean towards reusing sentences verbatim
    - summaries with low extractiveness tend to paraphrase