Problem Statement

The goal of this project is to build a Convolutional Neural Network (CNN) that classifies grayscale images of clothing items from the Fashion-MNIST dataset into one of ten predefined categories. The model aims to accurately recognize apparel types such as shirts, sneakers, and bags based on their visual features.

Dataset Used

Dataset Name: Fashion-MNIST
Source: TensorFlow/Keras built-in datasets

Data Composition:

60,000 training images

10,000 testing images

Image Dimensions: 28 × 28 pixels (grayscale)

Number of Classes (10):
0 — T-shirt/top
1 — Trouser
2 — Pullover
3 — Dress
4 — Coat
5 — Sandal
6 — Shirt
7 — Sneaker
8 — Bag
9 — Ankle boot

Preprocessing Steps:

Pixel values normalized to range [0,1]

Reshaped to (28, 28, 1) for CNN compatibility

Model Architecture

A Sequential CNN model was implemented with the following layers:

Conv2D (32 filters, 3×3, ReLU) – Extracts low-level features such as edges.

MaxPooling2D (2×2) – Reduces spatial dimensions and computation.

Conv2D (64 filters, 3×3, ReLU) – Captures deeper and more complex patterns.

MaxPooling2D (2×2) – Further dimensionality reduction.

Flatten – Converts 2D feature maps into a 1D feature vector.

Dense (128 neurons, ReLU) – Learns high-level representations.

Dense (10 neurons, Softmax) – Outputs class probabilities for each category.

Compilation Settings:

Optimizer: Adam

Loss Function: Sparse Categorical Crossentropy

Metrics: Accuracy

Instructions for Running the Code

Open Google Colab or any Python environment with TensorFlow installed.

Copy and paste the provided code into a new notebook cell.

Run all cells sequentially.

The model will:

Load and preprocess the Fashion-MNIST dataset.

Train for 10 epochs with validation on the test set.

Display the final test accuracy.

Plot training vs. validation accuracy over epochs.

Evaluation Metrics and Results

After training for 10 epochs, the model achieved the following performance:

Training Accuracy: approximately 92%

Validation Accuracy: approximately 89–91%

Test Accuracy: around 90%

Loss Function: Sparse Categorical Crossentropy

Observations:

The model generalizes well, maintaining consistent performance across training and validation sets.

Accuracy could be further improved using techniques such as data augmentation, dropout, or additional convolutional layers.
