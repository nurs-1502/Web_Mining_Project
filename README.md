# Web_Mining_Project

The NeuralNetworkApproach folder currently contains two .ipynb files. Both implement a two-tower neural network — one includes textual features among its input columns, while the other does not.

A two-tower neural network model involves building two separate neural networks: one for users and one for items. Each network generates a latent vector — V_u for the user and V_m for the item — based on the provided input features. The dot product of these vectors is then used to predict the score for a given user–item pair.

A third notebook will be added, which will focus on hyperparameter tuning.
