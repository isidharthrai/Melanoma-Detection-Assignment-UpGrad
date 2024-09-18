# Melanoma-Detection-Assignment-UpGrad

### Skin Cancer Detection using CNN

## Problem Statement

Melanoma is a type of cancer that can be deadly if not detected early, accounting for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists to the presence of melanoma has the potential to significantly reduce manual effort in diagnosis.

## Dataset

The dataset contains 2,357 images of various skin cancer types, organized into 9 sub-directories within both the train and test sets. Each sub-directory represents one of the 9 types of skin cancer.

## Model

The model is a Convolutional Neural Network (CNN) designed to accurately detect melanoma.

## Model Architecture

The CNN consists of the following layers:
- **Rescaling layer** to normalize pixel values between (0,1)
- **Conv2D layer** with 32 filters, kernel size 5, padding 'Same', activation 'relu'
- **Conv2D layer** with 32 filters, kernel size 5, padding 'Same', activation 'relu'
- **MaxPool2D layer** with pool size (2,2)
- **Conv2D layer** with 64 filters, kernel size 5, padding 'Same', activation 'relu'
- **MaxPool2D layer** with pool size (2,2)
- **Conv2D layer** with 64 filters, kernel size 5, padding 'Same', activation 'relu'
- **MaxPool2D layer** with pool size (2,2)
- **Dropout layer** with a dropout rate of 0.25
- **Flatten layer**
- **Dense layer** with 9 units, activation 'softmax'

## Model Compilation

The model is compiled with the following hyperparameters:
- **Optimizer**: Adam
- **Loss function**: Sparse Categorical Crossentropy
- **Metrics**: Accuracy

## Model Training

The model is trained on the dataset with the following settings:
- **Batch size**: 32
- **Image size**: 180x180
- **Epochs**: 50

## Model Evaluation

The model is evaluated on the validation dataset using the following metrics:
- **Accuracy**
- **Loss**

## Results

The model achieves an accuracy of 96.45% on the training dataset and 76.70% on the validation dataset.

## Visualizing Model Results

The results of the model are visualized using matplotlib.

## Analyzing Results

The model is currently overfitting, which could be addressed by adding more layers, neurons, or dropout layers. Further improvements can be made by tuning hyperparameters.

## Class Rebalance

To rebalance the dataset, the Augmentor library is used to generate additional samples across all classes.

## Visualizing Class Rebalance

The class rebalance process is visualized using matplotlib.

## Analyzing Class Rebalance

Using the Augmentor library has improved the model's accuracy on the training dataset.

## Conclusion

This model is a solid starting point for skin cancer detection using CNNs. However, improvements are needed to address overfitting and further refine performance.
