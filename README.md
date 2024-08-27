# Animal Classification Model Improvement

## Overview
This project aims to enhance the accuracy and efficiency of an animal classification model. The dataset used contains 6,270 images across 151 different animal classes. The objective is to optimize the baseline model, a convolutional neural network (CNN), to achieve better accuracy and efficiency in classifying these images.

## Project Structure

- **Animal_Classification.ipynb**: The main Jupyter Notebook containing the code for data preprocessing, model training, evaluation, of the final model.
- **Animal_Classification_Report.pdf**: A detailed report explaining the methodology, modifications to the baseline model, experimental results, and future work recommendations.
- **animal.zip**: A zipped file containing all the images used in the project. The images belong to 151 different animal classes.
- **Graphs**: The decompressed directory from `animal.zip` containing the images used for training and testing.
- **animal**: This directory contains plots of the accuracy and loss curves for various models.

## Key Components

1. **Baseline Model**:
   - A CNN built with PyTorch.
   - Utilizes 4 sampling layers and a fully connected layer.
   - Uses ReLU activation, MaxPooling, and the Adam optimizer.
   - Initially trained with a learning rate of 0.001 and evaluated using the cross-entropy loss function.

2. **Model Enhancements**:
   - **Learning Rate Scheduling**: Implemented using `ExponentialLR` to decrease the learning rate exponentially during training.
   - **Data Augmentation**: Introduced `RandomResizedCrop` and `RandomRotation` to improve model robustness.
   - **Batch Normalization**: Incorporated to stabilize and speed up training by normalizing activations between layers.
   - **ResNet Architecture**: Experimented with ResNet18 for deeper model evaluation but noted higher computational costs.

3. **Experimental Results**:
   - Conducted an ablation study to compare the performance of various model configurations.
   - Achieved the best results with a combination of Batch Normalization, data augmentation, and learning rate scheduling, yielding an accuracy of 63.5% with 0.69 GFLOPS and an efficiency of 92.03.
