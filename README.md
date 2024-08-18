# Cyber Attack Detection using Neural Network

This project implements a neural network model to detect cyber attacks using data collected from a simulated environment. The model is built using TensorFlow and Keras, and the project includes data preprocessing, model training, and evaluation.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Model Architecture](#model-architecture)
- [Evaluation](#evaluation)
- [Visualization](#visualization)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Screenshots](#screenshots)

## Introduction

The goal of this project is to develop a neural network model that can effectively detect cyber attacks by analyzing network traffic and system logs. The model is trained on datasets that simulate different types of cyber threats, including attack, noise, and normal scenarios.

## Features

- Data preprocessing and extraction from `.mat` files
- Model training using TensorFlow and Keras
- One-hot encoding of target labels
- Visualization of training and validation loss and accuracy
- Evaluation of the model's performance on training and testing data

## Installation

To run this project locally, follow these steps:

1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/cyber-attack-detection.git
    cd cyber-attack-detection
    ```

2. **Install necessary libraries:**
    ```bash
    pip install numpy scipy tensorflow matplotlib
    ```

3. **Mount your Google Drive to access the dataset:**
    ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```

## Usage

1. **Load and preprocess the dataset:**
    Extract the data from the `.mat` files and combine them into training and testing sets.

2. **Train the neural network model:**
    ```python
    hist = model.fit(Combined_training, target_total_train, epochs=500, steps_per_epoch=2, validation_steps=2, validation_data=(Combined_testing, target_total_test))
    ```

3. **Evaluate the model:**
    ```python
    score = model.evaluate(Combined_testing, target_total_test, verbose=0)
    print("Testing Accuracy: ", score[1])
    ```

4. **Visualize the results:**
    ```python
    plt.plot(hist.history['loss'], label="Train_loss")
    plt.plot(hist.history['val_loss'], label="Valid_loss")
    plt.plot(hist.history['accuracy'], label="Train_accuracy")
    plt.plot(hist.history['val_accuracy'], label="Valid_accuracy")
    plt.legend()
    plt.show()
    ```

## Project Structure

```plaintext
cyber-attack-detection/
├── data/
│   ├── CSTR_train_attack.mat
│   ├── CSTR_train_noise.mat
│   ├── CSTR_train_normal.mat
│   ├── CSTR_test_attack.mat
│   ├── CSTR_test_noise.mat
│   ├── CSTR_test_normal.mat
├── notebooks/
│   ├── preprocessing.ipynb
│   ├── model_training.ipynb
├── src/
│   ├── model.py
│   ├── utils.py
├── README.md
└── requirements.txt

```

## Technologies Used
**Languages:** Python
**Libraries:** TensorFlow, Keras, NumPy, SciPy, Matplotlib
**Tools:** Google Colab, Git

## Model Architecture
The neural network model consists of the following layers:
Flatten layer to convert the input data into a 1D array.
Dense layer with 100 neurons and ReLU activation.
Dense layer with 50 neurons and ReLU activation.
Dense layer with 25 neurons and ReLU activation.
Dense layer with 3 neurons and softmax activation for classification.
Evaluation
The model is evaluated on both the training and testing datasets. The accuracy and loss are measured to determine the model's performance.

## Visualization
The training and validation loss and accuracy are plotted to visualize the model's learning process over epochs.

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes. For major changes, open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Contact
For any inquiries or questions, please contact me at:

**Email:** divyanshsaini.mzn@gmail.com
## Screenshots 
![Screenshot 2024-07-06 110309](https://github.com/user-attachments/assets/bd39f9f0-2e43-4f04-b38b-f6388297aedd)



