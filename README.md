# Handwritten Digit Recognizer with NumPy 🧠

This project is a complete, from-scratch implementation of a simple neural network to recognize handwritten digits. It is built using only **NumPy** for the core machine learning logic, demonstrating a foundational understanding of deep learning mechanics.

The model is trained on the Kaggle-version of the MNIST dataset and can achieve high accuracy on a validation set. It also includes a function to preprocess and predict your own custom-drawn digits.

---

## 🚀 Key Features

* **Built from Scratch:** The entire neural network (MLP) is built using only NumPy. No `TensorFlow` or `Keras` is used for the model itself.
* **Core Mechanics Implemented:**
    * Forward Propagation
    * Backward Propagation (Gradient Descent)
    * Sigmoid (Hidden Layer) and Softmax (Output Layer) Activations
    * Cross-Entropy Loss Function
* **Custom Image Prediction:** After training, the script can load a local image (e.g., `my_digit.png`), preprocess it, and predict the digit.
* **Data Handling:** Uses `pandas` to load the dataset and `scikit-learn` to split it into training and validation sets.
* **Image Processing:** Uses `Pillow (PIL)` to prepare custom images for the model.

---

## 🏗️ How It Works: Network Architecture

The model is a simple **Multilayer Perceptron (MLP)** with a single hidden layer.

* **Input Layer:** 784 nodes (one for each 28x28 pixel)
* **Hidden Layer:** 64 nodes (using the `sigmoid` activation function)
* **Output Layer:** 10 nodes (one for each digit 0-9, using the `softmax` activation function)

The model is trained using gradient descent to minimize the cross-entropy loss.



---

## ⚙️ Installation

To run this project, you'll need Python 3 and a few common libraries.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```

2.  **Install the required libraries:**
    ```bash
    pip install numpy pandas scikit-learn pillow
    ```

3.  **Get the data:**
    * Download the `train.csv` file from the [Kaggle Digit Recognizer competition](https://www.kaggle.com/c/digit-recognizer/data).
    * Place the `train.csv` file in the same root directory as the Python script.

---

## Usage

There are two parts to running this project: training the model and testing your own image.

### 1. Training the Model

Simply run the Python script from your terminal:
The script will:

Load train.csv.

Split the data into a training set and a validation set.

Normalize and one-hot encode the data.

Initialize the network parameters.

Begin training for the specified number of epochs.

You will see the Loss decrease and the Validation Accuracy increase in your terminal every 100 epochs, showing the model as it learns.

### 2. Predicting Your Own Digit
After the training is complete, the script will automatically try to predict an image named my_digit.png.

Create your image: Open an image editor like MS Paint or GIMP.

Draw a digit: On a white background, use a black brush to draw a single, large, centered digit (0-9).

Save the image: Save the file as my_digit.png in the same folder as the Python script.

The script will then load, preprocess (invert, resize, flatten), and feed your drawing to the trained model, printing its final prediction.

Note: The model is highly specialized for the MNIST data format (centered, specific stroke width). It may struggle with photos or digits that are not centered, which is a known limitation of this simple MLP architecture.

```bash
python your_script_name.py
