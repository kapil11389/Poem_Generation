# Poem Generation

A Deep Learning Model that writes poems based on Shakespeare's work.

# Requirements

Intel i5 processor is used for training the model.
Python 3.3+ , Keras 2+ , Tensorflow 1.15+ , Pandas 0.24+, Numpy 1.5+

# Contents

Poem Generation.ipynb :  Contains the Deep Learning model ,data preprocessing and training of Model.

Sonnets.txt :  The full compilation of Shakespeare's literary works containing poems.

Weights.h5 :  Contains the weights associated with the Trained Model.

# RNN VS LSTM

This project utilizes the concept of Recurrent Neural Networks and the uses the benefits of LSTM over Recurrent Neural Networks(RNN).

The reason behind using LSTM is because while generating text, context is important. Which word comes after whom differentiates the sentence from being deep or profound to downright non-sensical.

# Character Mapping
This step is required as the RNN's work much better with numbers than with text. And moreover text is anyway converted to numerical representation anyway.

![image](https://user-images.githubusercontent.com/41421032/91052724-7ba59a00-e63f-11ea-99c5-14a1a0fca747.png)

# Data Preprocessing

The data that is input to the network must be preprocessed to get relevant data.

Here 100 characters are being used to predict 101th character.

![image](https://user-images.githubusercontent.com/41421032/91053168-12725680-e640-11ea-9d32-9a51021d559b.png)

# Model

![image](https://user-images.githubusercontent.com/41421032/91053516-8d3b7180-e640-11ea-9f6e-3dc6b4dca89f.png)

# Training the Model


# Generating text

We finally use the generated model to predict one character at a time. We use this characters and generate another character and the cycle goes on.

![image](https://user-images.githubusercontent.com/41421032/91055783-bfe66980-e642-11ea-96b1-5598ec0551fc.png)

# Observations:

Due to the limitations of the machine I am using and no GPU support, the model currently is able to :

    1. Create words with proper spelling (most of time)
    2. Understands rhyming and tries to incorporate a rhyme scheme
    3. Understands the spaces and newlines such that it doesn't create very long sentences.

I am sure better results can be expected by tinkering around with the number of neurons and number of layers while thinking about the vanishing gradient problem.
