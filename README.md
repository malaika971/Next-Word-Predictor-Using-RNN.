# Next-Word-Predictor-Using-RNN.
- Simple application using RNNs predicting the next word in a paragraph.
- Model Accuracy 90%

_______________

## Objective
This project aims to build a simple Next Word Prediction model using a Recurrent Neural Network (RNN). The model predicts the next word in a given sentence or paragraph based on the previously inputted words.

## Recurrent Neural Networks (RNN)
Recurrent Neural Networks (RNNs) are designed to handle sequential data, such as text. RNNs use the information from previous steps in the sequence to produce the current output. They are particularly useful for problems where context over time or sequence is important, such as in language modeling or time-series forecasting.

### Key Features of RNNs:
- **Memory**: RNNs retain information from past steps in a sequence and use it for future steps.
- **Types of RNN**:
  - **LSTM (Long Short-Term Memory)**: LSTMs are a special type of RNN designed to combat the vanishing gradient problem by enabling the network to remember or forget certain pieces of information.
  - **Gated Mechanisms**: LSTM networks use gates such as Forget, Input, and Output gates to manage memory and control information flow.

## Building the Next Word Predictor
This project uses LSTM-based RNNs to predict the next word in a sentence. We will train the model on a sample text and then use it to generate predictions.

### Text Input
We use the following sample text to train the model:

```
It was November. Although it was not yet late. The sky was dark when I turned into Laundress Passage. Father had finished for the day, switched off the shop lights, and closed the shutters. But so I would not come home to darkness, he had left on the light over the stairs to the flat.
```

### Steps to Build the Model:
1. **Importing Libraries**: We use TensorFlow, Keras, and Numpy for model creation, training, and text processing.
2. **Tokenization**: The text is tokenized into integer sequences where each unique word is assigned a unique integer.
3. **Padding**: All sequences are padded to the same length to ensure they are compatible with the LSTM model.
4. **Model Creation**:
   - Embedding Layer: Converts words into dense vectors.
   - LSTM Layers: Two LSTM layers process the input sequence and help in sequence prediction.
   - Dense Layer: Outputs a probability distribution over the vocabulary for the next word prediction.
5. **Model Compilation**: The model is compiled using categorical cross-entropy loss and Adam optimizer.
6. **Training**: The model is trained using the prepared data for multiple epochs.
7. **Prediction**: After training, we use the model to predict the next word given an input sequence.

### Example of Text Generation:
Given an input text like `"the sky was dark"`, the model predicts the next words one by one, such as:

```
the sky was dark when
the sky was dark when I
the sky was dark when I turned
...

This project demonstrates how to use an RNN, specifically LSTM, to predict the next word in a sequence based on previously seen words. With further enhancement and more data, the model could be expanded to handle longer contexts and more complex tasks like text generation, dialogue systems, or writing assistants.


## Acknowledgements
- TensorFlow and Keras for the deep learning framework.
- The dataset for training the model was custom-created for this demonstration.
