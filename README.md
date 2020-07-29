# CIFAR10

 CIFAR 10 is a computer vision dataset which contains 60000 images in 10 classes. The dataset is divided into train-49000 images, dev-1000 images and test-10,000 images. 
 This dataset is solved and there should be many models that provide great accuracies on the dataset though most of them have been trained on additional data.
 
 In this repository I have tried to build a model from scratch that can achieve greater that 90% accuracy on the dataset. Several models were tried for the purpose. Starting with a 6-layer Conv-Relu-BatchNorm-Dropout architecture followed by Maxpool on every 3rd layer. This model when trained with many different hyperparameters could achieve accuracies greater than 82% on the dev set when trained for 200 epochs, and even then the progress was very slow. Overfitting was a major issue as the accuracy on the training set was around 99%. To improve the accuracy I tried some basic image augmentation techniques like Random Horizontal Flip, Random Rotation, Random Vertical Flip. Funnily enough the model started to perform poorly with augmentation. But when Random Vertical Flip was removed the model achieved accuracies around 85% on the dev set
 
 So, I decided to try a Residual Network architecture with 9 layers of Conv-Relu-BatchNorm-Dropout with maxpooling followed by 3 fully connected layer. When the training started RESNET architecture started showing its powers. It achieved near 90% accuracy within 70 epochs but achieving accuracies greater than 90 still seems a challenge for resnets with limited data available. The best performance achieved so far on the dev set is 90.2% after a 100 epochs. I have still not tested this architecture on the test set, which i will once my experimentations with CIFAR-10 are over. Maybe I will try ensembling methods to check if an extra 2-3% performance can be squeezed out. All in all this repository will change frequently and by this sunday I will finish this work.
 
 
