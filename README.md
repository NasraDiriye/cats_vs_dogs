# cats_vs_dogs

This project demonstrates how to build a convolutional neural network (CNN) and fine-tune a pre-trained model (ResNet18) to classify images of cats and dogs. The dataset is organized into training, validation, and test sets.

Each folder contains images of cats and dogs, separated into their respective class directories.

Link to the dataset:
    https://drive.google.com/file/d/1ecoxWY3babiXsO18NZwr8aaP-ksVsPq-/view?usp=sharing


## Requirements

Install the required Python libraries using:

    !pip install torch torchvision matplotlib tqdm

Additional requirements if running on Kaggle:

- Ensure the dataset is correctly uploaded to Kaggle.

    

## Implementation Steps

### Data Preprocessing:

  - Images are resized to 150x150 pixels.
  - Data augmentation (random horizontal flip) is applied to the training set.
  - Images are normalized using ImageNet statistics

### Model Architecture:

  - A ResNet18 pre-trained on ImageNet is fine-tuned for binary classification (cats vs dogs).
  - The fully connected layer of ResNet18 is replaced with a linear layer for two classes.

### Training:

  - CrossEntropyLoss is used as the loss function.
  - Adam optimizer is employed with a learning rate of 0.001.
  - Training and validation phases alternate per epoch.
  - Losses are tracked for both training and validation.

### Evaluation:

  - Accuracy and a few correctly classified images are displayed.


