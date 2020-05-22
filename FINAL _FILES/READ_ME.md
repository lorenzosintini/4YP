## READ ME

All the final versions of the code are saved in the directory "FINAL_FILES". The directory conttains 6 files:

### MNIST_VAE:
Contains a simple Variational Autoencoder (VAE) network that is trained with the MNIST number dataset. This is just a code to test VAEs architectures, loss functions and see if the model works as intended. 

### MNIST_CVAE:
Contains a simple Conditional Variational Autoencoder (CVAE) network that is trained with the MNIST number dataset. This is just a code to test CVAEs architectures, loss functions and see if the model works as intended (inclusing reconstruction of particular classes)

### Fashion_MNIST_VAE:
Code to use VAEs to classify the Fahion-MNIST dataset. Contains different sections:
* Standard classification: selecting the class with the highest probability. This can be tested on a normal balanced dataset (with 6000 images for each training class) or on an imbalanced dataset (significantly reducing the amount of data in some classes)
* Solution approaches to the imbalanced dataset bias problem:
    * ROC curve method
    * Cost-sensitive loss function method (algorithm-based)
    * Random Over Sampling (ROS) method (data-based)

### Fashion_MNIST_CVAE:
Code to use CVAEs to classify the Fahion-MNIST dataset. Only used for standard classification (selecting the class with the highest probability).

### Mastcam_DS1_Experiment
VAE novelty detection for the DS1 Mastcam dataset. Includes all the loss functions and both models:
* Unsupervised model: uses one-dimensional losses
* Semi-supervised model: uses high-simensional losses and 4 possible classifiers:
    * Classifier 1: error-map (high dimensional loss from reconstruction image)
    * Classifier 2: error-vector (high dimensional loss from latent space)
    * Classifier 3: combination of all error-vectors
    * Classifier 4: combination of one error-map and one error-vector


### Mastcam_DS2_Experiment
VAE novelty detection for the DS1 Mastcam dataset. Test performed on the best loss for unsupervised model (Loss_R7) and the best loss for the semi-supervised model (Classifier 4 with Loss_R4 + Loss_L1)
The classification is also checked for each novel class individually (because DS2 provides labelled data for the novel dataset)
