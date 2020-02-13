# housing-price
Regression using CNN 1D for House price prediction on California Housing Dataset

Input Layer: The input data has been preprocessed and doesn’t contain any missing values that can affect the prediction model. Every instance of the dataset has eight features, hence the input is 8 to provide a holistic impression per instance. The first layer in the network must reshape it to a single dimension.

Batch Normalisation: Batch normalization is a technique for training very deep neural networks that stan- dardizes the inputs to a layer for each mini-batch. This has the effect of stabilizing the learning process and dramatically reducing the number of training epochsrequired to train deep networks.

1D CNN layer: The first layer defines a kernel of height 1. One filter would allow the neural network to learn a single feature in the first layer which is not adequate, hence 64 filters are defined to detect 64 features.

Pooling layer: A pooling layer is usually used after a CNN layer in order to subsample the input to provide a simpler output that helps prevent overfitting of the data. The proposed model uses max-pooling layer after two consecutive CNN layers followed by an average-pooling layer after two consecutive CNN layers.

Fully Connected Layers: The FC layers use the flat- tened output from the CNN layers in the vector of height 64. The proposed model has three FC layers and the last FC layer is responsible for providing a single output since we have a single value to predict, the house price (i.e. regression).
