# twitter-sentiment-analysis
Twitter sentiment analysis using trending classification techniques. Each project implements a solution for the same classification task based on a twitter dataset for covid-19

# Project 1
In this exercise you will develop a vaccine sentiment classifier using softmax regression.
The classifier will be trained on twitter data and will distinguish 3 classes (neutral, antivax and pro-vax). You will train your classifier using the datasets provided. The datasets are CSV files with the tweet texts and the labels 0
(neutral), 1 (anti-vax) or 2 (pro-vax). The first dataset is the training dataset and the
second one is the validation dataset. Your model will be evaluated by us on a test set that
will not be provided to you, but will be of the same format as the training and validation
datasets. Your code should be written in such a way so that the model can be evaluated
on the test simply by changing the name of the file to load.
Start by reading about softmax regression from the slides of the course, the relevant
chapters 4 and 5 of the “Speech and Language Processing” book of Jurafsky and Martin
(http://web.stanford.edu/~jurafsky/slp3) or any other relevant literature which
you may find. You should use the toolkit Scikit-Learn for your implementation. You should plot learning
curves that show that your models are not overfitting or underfitting. You should also
evaluate your classifiers on the validation set using precision, recall and F-measure.
Finally, we would like to stress that the goal of this exercise is not to simply create a
classifier that can achieve a good score, but to get acquainted with the methodology of an
NLP project, to experiment with different options and to deliver a report that presents
your solution along with a brief performance comparison between the different options
that you have tried.

# Project 2

Develop a vaccine sentiment classifier with 3 classes (neutral, anti-vax and pro-vax) using
feed-forward neural networks and the datasets of the previous homework provided on eclass. We expect you to experiment with at least two models and compare them using
F1 score, recall and precision. For the development of the models, you are expected to
experiment at least with the following hyperparameters:
* the number of hidden layers and the number of their units
* the activation functions
* the loss function
* the optimizer

Furthermore, in at least one of your models, you must use pre-trained word embedding
vectors using [GloVe](https://nlp.stanford.edu/projects/glove).
For your best model, you must also provide the loss vs epochs plot along with the [ROC curve](https://en.wikipedia.org/wiki/Receiver_operating_characteristic)
(on the validation set, after training has been completed) and explain what you see.
Also, compare your best model with the model you obtained using softmax regression in
Homework 1. Your solution should be implemented in PyTorch and we expect your report
to be well-documented.

# Project 3

a. Develop a sentiment classifier with 3 classes (pro-vax, anti-vax, neutral) using a bidirectional stacked RNN with LSTM/GRU cells for the Twitter vaccine sentiment dataset of
the previous two assignments. For the development of the models, you can experiment
with the number of stacked RNNs, the number of hidden layers, type of cells, skip connections, gradient clipping and dropout probability. Document the performance of different
configurations on your final report. Use the Adam optimizer and the cross-entropy loss
function. You should also utilize [GloVe](https://nlp.stanford.edu/projects/glove) pre-trained word embeddings as the embeddings
of the inputs of your models.
For the best model you will find:
* Compute precision, recall and F1 for each class.
* Plot the loss vs. epochs curve and the [ROC curve](https://en.wikipedia.org/wiki/Receiver_operating_characteristic) (on the validation set, after training
has been completed) and explain what you see.
* Compare with your best model from Homeworks 1 and 2.

Your solution should be implemented in PyTorch and we expect your report to be well
documented.

b. Add attention to the best model you developed in the previous question. Evaluate the
improvements that you might have from its introduction.

# Project 4

Develop a sentiment classifier with 3 classes (pro-vax, anti-vax, neutral) by fine-tuning the
pretrained BERT-base model available on [Hugging Face](https://huggingface.co/models). You have to compute precision, recall and F1 for each class.
