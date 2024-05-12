# Trigram-Models
Comparison of two approaches of Trigram Models
I will use these Trigram models to produce realistic names.
By Trigram model I mean that the model takes in two input characters and generates a third output character to produce text.

The first approach consists of building a probability matrix for the next character given a combination of input characters
and then sampling from that matrix to generate names.

The second approach consists of using a Neural Net consisting of 27 Neurons that will take as input a one-hot encoded vector signaling
which two-character input is currently being fed to the network. The Neural Net will then produce an output in the form of a probability
distribution over the next character and we will then sample from this distribution to actually generate names.

I will compare the two approaches by calculating the Negative Log-Likelihood.
My dataset is in the names_dataset.txt containing a little more than 32K names.
I will use an 80/20 train-test split.
