# Fashion MNIST CNN Classification

## Project Overview

This project builds a Convolutional Neural Network (CNN) to classify Fashion MNIST clothing images into 10 categories.

The goal of this project is to practice deep learning image classification using TensorFlow/Keras and create an interviewer-friendly machine learning project that demonstrates a complete model development workflow.

The model classifies grayscale clothing images into one of ten classes:

`T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot`

---

## Dataset

This project uses the Fashion MNIST dataset, which contains grayscale images of clothing items.

The dataset includes:

- 60,000 training images
- 10,000 testing images
- Image size: 28 × 28 pixels
- Image type: grayscale
- Classes: 10 clothing categories

The dataset is loaded directly from TensorFlow/Keras:

```python
keras.datasets.fashion_mnist.load_data()
```

No manual dataset download is required.

---

## Class Labels

Fashion MNIST labels are stored as numeric values from 0 to 9. Each number represents one clothing category.

| Label | Class Name |
|---:|---|
| 0 | T-shirt/top |
| 1 | Trouser |
| 2 | Pullover |
| 3 | Dress |
| 4 | Coat |
| 5 | Sandal |
| 6 | Shirt |
| 7 | Sneaker |
| 8 | Bag |
| 9 | Ankle boot |

---

## Project Workflow

The notebook follows these main steps:

1. Import required libraries
2. Load the Fashion MNIST dataset
3. Define and verify class names
4. Display sample Fashion MNIST images
5. Normalize image pixel values
6. Reshape images for CNN input
7. Build the CNN model
8. Compile the model
9. Train the model
10. Evaluate the model on test data
11. Plot training and validation accuracy/loss
12. Generate predictions
13. Review the classification report
14. Display the confusion matrix
15. Visualize sample model predictions
16. Review misclassified images
17. Summarize findings

---

## Tools and Libraries

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Model Architecture

The CNN model is designed to classify 28 × 28 grayscale Fashion MNIST images into 10 clothing classes.

| Layer | Purpose |
|---|---|
| Input | Defines the input image shape as 28 × 28 × 1 |
| Conv2D | Extracts visual patterns such as edges, curves, textures, and clothing shapes |
| MaxPooling2D | Reduces feature map size while keeping important information |
| Conv2D | Learns deeper image patterns |
| MaxPooling2D | Further reduces feature size |
| Conv2D | Extracts more complex clothing features |
| Flatten | Converts 2D feature maps into a 1D vector |
| Dense | Learns classification patterns from extracted features |
| Dropout | Reduces overfitting by randomly disabling neurons during training |
| Dense with Softmax | Outputs probability scores for the 10 clothing classes |

The final `softmax` layer is used because this is a multi-class classification problem. The class with the highest probability becomes the model's final prediction.

---

## Model Evaluation

The model was evaluated using:

- Test accuracy
- Test loss
- Classification report
- Confusion matrix
- Prediction visualization
- Misclassified image review

The CNN model achieved approximately **90% test accuracy** on the Fashion MNIST test dataset.

---

## What I Learned

Through this project, I practiced:

- Loading image data using TensorFlow/Keras
- Understanding numeric class labels and class-name mapping
- Displaying grayscale image data
- Normalizing pixel values for neural network training
- Reshaping image data for CNN input
- Building a CNN model with convolutional and pooling layers
- Training and validating a deep learning model
- Evaluating model performance using classification metrics
- Interpreting confusion matrices
- Reviewing incorrect predictions for error analysis
