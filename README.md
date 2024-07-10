# Cyber_Threat_Analysis
Cyber Attack Detection using Neural Network

Objective:
The goal of this project is to develop a neural network model that can accurately detect cyber attacks by analyzing network traffic and system logs.

Workflow:

Data Collection: Extracted training and testing datasets from MATLAB files, including attack, noise, and normal data.
Data Preprocessing:
Loaded datasets using scipy.io.
Combined and structured the data into training and testing sets.
One-hot encoded the target labels for compatibility with the neural network.
Model Development:
Built a neural network using TensorFlow/Keras with multiple layers (Dense layers with ReLU activation and an output layer with softmax activation).
Compiled the model with categorical cross-entropy loss and Adam optimizer.
Trained the model for 300 epochs and validated it on the test data.
Evaluation:
Plotted training and validation loss and accuracy to visualize model performance.
Analyzed the graph to check for overfitting, which was not observed as training and validation curves converged well.
Results:
Achieved good training and validation accuracy.
Demonstrated the model's ability to generalize well on unseen data.
Libraries Used:

zipfile: For extracting data files.
numpy: For numerical operations.
scipy.io: For loading MATLAB data files.
tensorflow/keras: For building and training the neural network.
pandas: For data manipulation.
matplotlib: For visualizing training progress.
sklearn.preprocessing (OneHotEncoder): For encoding categorical labels.
Conclusion:
The neural network successfully detects cyber attacks by learning from network traffic patterns, achieving high accuracy and demonstrating good generalization to new data
