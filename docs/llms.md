# Introduction to Large Language Models (LLMs)

A language model (LM) is a **probabilistic model of text**.

"Large" in LLM refers to the **numbers of parameters** in the model, but there is no agreed upon threshold at which a language model becomes *large* or *extra large* or *not large*.

A LM gives a probability to every word in its vocabulary of appearing in the blank. For example:

    I wrote to the zoo to send me a pet. 
    They sent me a _______.


| Word | Probability | 
| - | - | 
| lion | 0.10 | 
| elephant | 0.10 |
| dog | 0.30 |
| cat |  0.20 |
| panther | 0.05 |
| alligator | 0.02 |

## Sub-topics

- **LLM Architectures**
    - How are the models built ?
    - What do they look under the hood ?
    - What the model can do or it's supposed to do ?
- **Prompting and Training**
    - How do we affect the distribution over the vocabulary ?
        - *Prompting* does not change any of the model's parameters
        - *Training* change the model's parameters
- **Decoding**
    - *Decoding* is the technical term for generating text from an LLM


