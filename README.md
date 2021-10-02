# Inception-Net-implementation
The purpose of this project is to implement the GoogLeNet CNN architecture, proposed by C. Szegedy et al. (2014). Codenamed “Inception”, the original motivation behind this model was to increase the network depth while keeping the computational budget constant.
## Dataset
The Inception model was used for image classification on resized (224x224) images from the CIFAR10 dataset. The original dataset consists of 60,000 images (32x32) divided into 10 mutually exclusive classes (automobile, bird, cat and so on). 5000 training and 1000 testing images were used.<p/>
<em><b>Sample CIFAR10 images:</b></em> <br/>
<img src="https://github.com/Aadit3003/GoogLeNet-implementation/blob/339fc265254af2fa391c986bb83fd8edc1a48591/demo_images/cifar10.png" width="600"><br/>
## Model Architecture
The basic building block in this architecture is the 'Inception Module' which combines 2 ideas. First, the outputs of 1x1, 3x3, and 5x5 convolutions are concatenated into a single input for the next layers. Second, 1x1 convolutions (ReLU activation) are used before each of these to apply dimension reduction and lower the computation cost. A total of 9 inception modules along with Max Pooling and Fully Connected layers are used in the model. <p/>
<em><b>Inception Module:</b></em> <br/>
<img src="https://github.com/Aadit3003/GoogLeNet-implementation/blob/339fc265254af2fa391c986bb83fd8edc1a48591/demo_images/inception_module.png" width="600"><p/>
<em><b>GoogLeNet Architecture:</b></em> <br/>
<img src="https://github.com/Aadit3003/GoogLeNet-implementation/blob/8a21755d8aae0d0f29cf9b24078fc406dbb4f34c/demo_images/model.png" width="1200"><br/>

## Training
- Loss Function: Sparse Categorical Crossentropy (10 output classes)
- Optimizer: SGD (stochastic gradient descent) with momentum 0.9
- No. of Parameters ~ 5.9 million 
- Metric: Accuracy
- Epochs : 15 <p/>
<em><b>Tensorboard epoch accuracy and loss:</b></em>

<img src="https://github.com/Aadit3003/GoogLeNet-implementation/blob/7339f4da945178950fc84fd2d0837a54c1a1d912/demo_images/combined.png" width="500"><br/>
## Possible Improvements and Applications
- After  a modest 15 epochs of training, the model was able to achieve 77% accuracy. More epochs could greatly enhance the accuracy.
- Using a hardware accelerator (GPU) would allow us to use much larger datasets and improve performance.
- Inceptionv3 is the third edition of Google's Inception CNN and has been included in the TensorFlow Keras API for image analysis and classification.
