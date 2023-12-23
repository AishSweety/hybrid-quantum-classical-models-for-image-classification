## hybrid-quantum-classical-models-for-image-classification

The python code implements the hybrid quantum-classical models from the paper "Quantum machine learning for image classification" by Arsenii Senokosov et al (https://arxiv.org/pdf/2304.09224.pdf) 

The paper proposes two hybrid quantum-classical models for image classification:

1. **Hybrid Quantum Neural Network with parallel quantum dense layers, HQNN-Parallel**:

HQNN-Parallel is a hybrid quantum-classical model that utilizes multiple parallel quantum dense layers for image classification tasks. The classical convolutional block reduces the dimensionality of the input image, and the parallel quantum dense layers extract and process features from the reduced representation.

The model is evaluated on the MNIST dataset of handwritten digits and compared with the performance of the classical convolutional neural networks (CNNs) with similar architectures.

The classical convolutional neural network is implemented in `` ImgClass-Classical.ipynb `` and the HQNN-Parallel is implemented in `` ImgClass-Hybrid.ipynb ``

**Result**: The classical convolutional neural network gives an accurancy of 99.20% and the HQNN-Parallel (with ``n_layers = 1`` instead of ``n_layers = 3`` as used in the paper) gives an accuracy of 99.17%

3. **Hybrid Quantum Neural Network with quanvolutional layer, HQNN-Quanv**:

HQNN-Quanv is a hybrid quantum-classical model that combines a quanvolutional layer with classical fully connected layers to address the image classification task. The quanvolutional layer utilizes quantum mechanics to extract features from the input image, while the classical fully connected layers process and classify these features.

The model is evaluated on the MNIST dataset of handwritten digits and compared with the performance of the classical convolutional neural networks (CNNs) with similar architectures.


