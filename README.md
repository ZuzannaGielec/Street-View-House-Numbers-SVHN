# Deep Learning Models for Number Recognition on SVHN Dataset

**Collaborators:** [Zuzanna Gielec], [Hubert Wodziak]

This repository contains the code and report for our project on developing and evaluating Deep Learning models for recognizing numbers from images in the SVHN dataset.

## Introduction

This report showcases our work, conducted collaboratively by [Zuzanna Gielec] and [Hubert Wodziak], in developing and evaluating Deep Learning models for recognizing numbers from images in the SVHN dataset. We tested two models: a pretrained MobileNetV2 model and our custom CNN approach. The report includes details of data preprocessing, model training, and evaluation for both approaches.

## Data Preprocessing

After loading the data from the torchvision library, we performed data preparation for implementing the models. For the MobileNetV2 model, we resized images to 224x224 format to match the required size. Then, we applied random horizontal flips for data augmentation and normalized the images using mean and standard deviation.

For our CNN model, we resized images to 32x32 pixels, applied random horizontal flip and rotation for data augmentation, and normalized the images using mean and standard deviation.

After these steps, we created data loaders to load the training and test datasets.

## Network Structure

For the MobileNetV2 model, the final layer was modified to match the number of classes in the SVHN dataset.

For the CNN model, we designed an architecture containing 3 convolutional layers (with 32, 64, and 128 filters respectively) and a fully connected layer with ReLU activation.

## Training

After defining the device (GPU), loss function, and optimizer, we created training loops. Both loops are similar, with the only difference being the number of epochs. The MobileNetV2 model was trained for 5 epochs, while our CNN approach was trained for 20 epochs.

## Evaluation

The evaluation function is the same for both models. We decided to present the results in the form of confusion matrices.

## Results

The pretrained MobileNetV2 model achieved a test accuracy of approximately 94.8% with a loss function value of around 0.239 after 5 epochs.

Our custom CNN model achieved a test accuracy of 88.5% with a loss function value of 0.207 after 20 epochs.

## Conclusions

We successfully trained and evaluated two Deep Learning models for number recognition on the SVHN dataset. The MobileNetV2 model demonstrated the effectiveness of transfer learning, achieving high accuracy. However, it took a significant amount of time to compile, possibly due to issues in our code. The CNN model also performed well, showing the potential of tailored architectures. In future work, we would experiment with different model architectures and investigate ensemble methods to further improve performance. We are pleased with our results.
