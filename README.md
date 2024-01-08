## Hybrid quantum classical models for image classification

The python code implements the hybrid quantum-classical models from the paper "Quantum machine learning for image classification" by Arsenii Senokosov et al (https://arxiv.org/pdf/2304.09224.pdf) 

The paper proposes two hybrid quantum-classical models for image classification:

1. **Hybrid Quantum Neural Network with parallel quantum dense layers, HQNN-Parallel**:

HQNN-Parallel is a hybrid quantum-classical model that utilizes multiple parallel quantum dense layers for image classification tasks. The classical convolutional block reduces the dimensionality of the input image, and the parallel quantum dense layers extract and process features from the reduced representation.

The model is evaluated on the MNIST dataset of handwritten digits and compared with the performance of the classical convolutional neural networks (CNNs) with similar architectures.

The classical convolutional neural network is implemented in `` ImgClass-Classical.ipynb `` and the HQNN-Parallel is implemented in `` ImgClass-Hybrid.ipynb ``

**Result**: The classical convolutional neural network gives an accurancy of 99.20% and the HQNN-Parallel (with ``n_layers = 1`` instead of ``n_layers = 3`` as used in the paper) gives an accuracy of 99.17%


2. **Hybrid Quantum Neural Network with quanvolutional layer, HQNN-Quanv**:

HQNN-Quanv is a hybrid quantum-classical model that combines a quanvolutional layer with classical fully connected layers to address the image classification task. The quanvolutional layer utilizes quantum mechanics to extract features from the input image, while the classical fully connected layers process and classify these features.

The model is evaluated on the MNIST dataset of handwritten digits and compared with the performance of the classical convolutional neural networks with similar architectures. Particularly with, CNN1- Convolutional kernel with 1 input channel, 1 output channel and CNN4- Convolutional kernel with 1 input channel, 4 output channels. 4 x 4 kernels are used. 

The classical convolutional neural network is implemented in `` CNN1.ipynb `` and `` CNN4.ipynb ``, the HQNN-Quanv is implemented in `` HQNN-Quanv.ipynb ``

**Result**: CNN1 gives an accuracy of 79%, CNN4 gives an accuracy of 67% and the HQNN-Quanv had an accuracy of 70% (see ``dataset_indices_500.pt``). 

Note that HQNN-Quanv model uses Initial_lr = 0.003, and the model's loss function seems to be very sensitive to small changes (+/- 0.0005) to Initial_lr, significantly impacting the accuracy (which gets to 58% for Initial_lr = 0.0035, or 45% for Initial_lr = 0.0025, for example). See ``hqcnn quanv output.txt`` for some outputs of HQNN-Quanv model training run). 
