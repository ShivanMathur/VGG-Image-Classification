# VGG-Image-Classification
The project's objective is to utilize the VGG-13 architecture to classify images within a dataset consisting of three categories: Dogs, Cars, and Food.

### Implementation:
- **Data Preprocessing:** Implemented a data preprocessing pipeline that included extracting, normalizing, and transforming the dataset, ensuring images were converted to a consistent format and scale for optimal model performance.
- **Model Architecture:** Implemented VGG-13 architecture, featuring 10 convolutional layers with batch normalization and ReLU activation, followed by max-pooling layers. The model's fully connected network (FCN) consists of two dense layers with 4096 units each, leading to a final output layer tailored for the 3-class classification task. 
- **Training and Evaluating the VGG-13 Model:**
  - **Training Process:** The architecture was optimized using the Adam optimizer and CrossEntropyLoss, ensuring efficient training and robust performance across the dataset. Monitored training loss and accuracy throughout the epochs, ensuring model improvements with each iteration.
  - **Validation and Testing:**  Integrated validation at each epoch to monitor the model's performance on unseen data, ensuring generalization. After training, the model was thoroughly evaluated on the test set to assess its robustness, overall performance, and accuracy.
- **Model Evaluation:** Created plots to visualize training and validation accuracy and loss trends. Generated performance metrics including accuracy, precision, recall, F1 score, and confusion matrix for thorough evaluation and analysis of model effectiveness.

### Model Performance:
- Basic Model: Initially developed the model without optimization techniques, serving as a baseline for further improvements.
- Optimization Techniques:
  - Regularization: Introduced L2 regularization by adding a weight decay parameter of 1e-5 to the optimizer. This technique helps prevent overfitting by penalizing large weights, which improved model generalization and increased accuracy to 92.00%.

  - Dropout: Added dropout layers with a probability of 0.5 between the fully connected layers to reduce overfitting by randomly dropping neurons during training. Although this technique slightly decreased test accuracy to 90.84%, it enhanced model robustness.

  - Early Stopping: Implemented early stopping to monitor validation loss and halt training if improvement ceased for a specified number of epochs (patience value of 4). The training concluded at epoch 19, with saved model weights showing a training accuracy of 92.71% and loss of 0.0018, and validation accuracy of 94.167% and loss of 0.0019. This approach significantly increased test accuracy to 93.02% and reduced test loss to 0.1995.

  - Image Augmentation: Applied image augmentation techniques including resizing images to 64x64 pixels and random horizontal flipping with a probability of 0.5. Despite these alterations, test accuracy was 87.46% with a loss of 0.3422, indicating the impact of dataset variation on model performance.
