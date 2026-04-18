# Day-100-CNN-architecture

###  Overview

**Convolutional Neural Networks (CNNs)** are a type of **deep learning model** specially designed for **image and visual data processing**.

They are widely used in **computer vision tasks** like image classification, object detection, and facial recognition.

---

##  What is a CNN?

A CNN automatically learns **important features from images** using convolution operations.

Basic structure:

```text id="c2n8k4"
Input Image → Convolution → Activation → Pooling → Fully Connected Layer → Output
```

---

##  Key Layers in CNN

### 1️ Convolution Layer

* Applies filters (kernels) to extract features
* Detects patterns like edges, textures

---

### 2️ Activation Function

* Adds non-linearity
* Common: ReLU

---

### 3️ Pooling Layer

* Reduces image size
* Helps in reducing computation

Types:

* Max Pooling
* Average Pooling

---

### 4️ Fully Connected Layer

* Final layer for prediction
* Converts features into output

---

##  Simple Implementation (Python)

```python id="k3n9x2"
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Conv2D, MaxPooling2D, Flatten, Dense

model = Sequential([
    Conv2D(32, (3,3), activation='relu', input_shape=(28,28,1)),
    MaxPooling2D(2,2),
    Flatten(),
    Dense(64, activation='relu'),
    Dense(10, activation='softmax')
])
```

---

##  Advantages

- Excellent for image data
- Automatic feature extraction
- High accuracy in vision tasks

---

##  Disadvantages

* Requires large datasets
* Computationally expensive

---

##  Use Cases

* Image classification
* Face recognition
* Object detection
* Medical imaging

---

##  Key Takeaways

- Specialized for image processing
- Uses convolution and pooling layers
- Core of modern computer vision

---

