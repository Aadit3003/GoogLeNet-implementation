# GoogLeNet-implementation
The purpose of this project is to implement the GoogLeNet CNN architecture, proposed by C. Szegedy et al. (2014). Codenamed “Inception”, the original motivation behind this model was to increase the network depth while keeping the computational budget constant.
## Dataset
The Inception model was used for image classification on resized (224x224) images from the CIFAR10 dataset. The original dataset consists of 60,000 images (32x32) divided into 10 mutually exclusive classes (automobile, bird, cat and so on). 5000 training and 1000 testing images were used.
## Model Architecture
The basic building block in this architecture is the 'Inception Module' which combines 2 ideas. First, the outputs of 1x1, 3x3, and 5x5 convolutions are concatenated into a single input for the next layers. Second, 1x1 convolutions (ReLU activation) are used before each of these to apply dimension reduction and lower the computation cost. A total of 9 inception modules along with Max Pooling and Fully Connected layers are used in the model.
## Training
- Loss Function: Sparse Categorical Crossentropy (10 output classes)
- Optimizer: SGD (stochastic gradient descent) with momentum 0.9
- No. of Parameters ~ 5.9 million 
- Epochs : 15
## Test Set Performance
## Improvements
## Applications
