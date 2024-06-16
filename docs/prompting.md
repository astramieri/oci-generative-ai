# Prompting

To exert some control over the LLM, we can affect the probability over vocabulary in two ways:
- prompting
- training

## Prompting

The simplest way to affect the distribution over the vocabulary is to change the **prompt**. The prompt is the text provided to an LLM as input, sometimes containing instructions and or examples.

Very large decoder-only models are initially trained in a procedure called *pre-training*. During pre-training, a model is fed a tremendous amount of text that is typically quite varied.

## Prompt Engineering 

**Prompt Engineering** is the process of iteratively refining the prompt for the purpose of elicing a particular style of response.

A couple of notes about prompt engineering:
- it is **challenging**, often **unintuitive**, and **not guaranteed to work**
    - Even adding a *whitespace* can have a large effect on the distribution over vocabulary words!
- it **can be effective**
    - Multiple tested prompt-desing strategies exist

## Prompt Engineering Strategies

**In-context learning** means conditioning (prompting) an LLM with instructions and or demonstrations of the task it is meant to complete. The phrase *in-context learning* does not actually involve learning in the traditional sense, none of the parameters of the model are changing.

**K-shot prompting** means explicitly proving *k* examples of the intended task in the prompt. Few-shot prompting is widely believed to improve results over 0-shot promtping.

**Chaing-of-Thought** refers to prompt the LLM to emit intermediate reasoning steps. It is not reasoning, but it imitates reasoning in a nice and convincing way.

**Least-to-most** refers to prompt the LLM to decompose and solve, easy first.

**Step-back** refers to prompt the LLM to identify high-level concepts pertinent to a specific task.

## Issues with Prompting

**Prompt injection (jailbreaking)** is the process to deliberately provide an LLM with input that attemps to cause it to ignore instructions, cause harm, or behave contrary to deployment expectations. 

For example, text that reveals private informations.

Prompt injection is a concern any time an external entity is given the ability to contribute to the prompt.
