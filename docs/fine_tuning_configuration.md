# Fine-Tuning Configuration in OCI

- **Training Methods**
    - Vanilla: traditional fine-tuning method
    - T-Few: efficient fine-tuning method
- **Hyper-parameters**
    - (Vanilla) Numbers of last layers
    - (T-Few) Total training epochs
        - number of iterations through the entire training dataset
        - default: 3
    - (T-Few) Batch size
        - number of samples processed before updating the model
        - default 8-16
    - (T-Few) Learning rate
        - rate at which model parameters are updated after each batch
        - it has a **significant impact on training dynamics** and the final performance of the model
        - default 0.1
    - (T-Few) Early stopping threshold
        - minimum improvement in loss required to prevent premature termination of the training process
        - default: 0.01
    - (T-Few) Early stopping patience
        - tolerance for stagnation in the loss metric before stopping the training process  
        - it is a technique to **prevent overfitting** during the training
        - default: 6
    - (T-Few) Log model metrics interval in steps
        - it determines how frequently to log model metrics
        - default: 10

## Understanding Fine-Tuning Results

These are the two measures by which we determine whether our model is giving good results or not:
- **Accuracy**
    - it is a measure of how many predictions the models made correctly out of all the prediction in an evalutation
    - *for example, an accuracy of 0.95 means that 95% of the output tokens matched the tokens in the training dataset*
- **Loss**
    - it is a measure that describes how bad or wrong a prediction is 
    - accuracy does not describe how incorrect the wrong predictions are
    - it should decrease as the model improves 
    - *for example, a loss of 0 means that all outputs were perfect, while a large number indicated highly random outputs*