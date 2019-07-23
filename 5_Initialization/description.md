## Initialization and their effects

The first step that we have to do when starting training a deep neural network is to initialize our parameters.

We can do initialization in three ways:

### 1. Zero Initialization

This is not at all recommended. Initializing all the parameters with zeros will essentially make the neural network a symmetric
one which means that a DNN will do the same activations in each layer. There seems to be no point then to use a DNN for
the application.


### 2. Random Initialization

Random initialization works way better than zero initialization. However, there seems to be a problem with this type of
initialization too: Exploding and Vanishing gradients. If the initialized parameters are too large or too small, it is
expected that the algorithm will succumb to exploding or vanishing gradients respectively.


### 3. Xavier Initialization

In Xavier initialization we first randomly initialize the paramters and multiply them by $\sqrt{\frac{1}{\text{dimension of the previous layer}}}$ This gives much better remedy for exploding and vanishing gradients.


### 4. He Initialization

He initialization is similar to Xavier initialization but we multiply the randomly initialized weights with $\sqrt{\frac{2}{\text{dimension of the previous layer}}}$ instead of $\sqrt{\frac{1}{\text{dimension of the previous layer}}}$ . Also helps with gradients (exploding and vanishing). Better than Xavier initialization.