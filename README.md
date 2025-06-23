# 🥔 Potato Disease Classification using CNN

This project uses a Convolutional Neural Network (CNN) to classify potato leaves into three categories:
- **Potato__Early_blight**
- **Potato_healthy**
- **Potato_Late_blight**

It leverages the [PlantVillage dataset](https://www.kaggle.com/datasets/arjuntejaswi/plant-village) and implements a full training pipeline with TensorFlow and Keras.

---

## 📂 Dataset

Download the dataset from Kaggle:

🔗 [PlantVillage Dataset](https://www.kaggle.com/datasets/arjuntejaswi/plant-village)

Use only the following folders from the dataset:
- `Potato__Early_blight`
- `Potato_healthy`
- `Potato_Late_blight`

Place these inside a directory named `PlantVillage/`.

---

## 🚀 Model Pipeline

### 🔧 Preprocessing
- Images resized to `256x256`
- Normalized pixel values
- Data augmentation (random flip and rotation)

### 🧠 CNN Architecture
```text
Conv2D → MaxPool → Conv2D → MaxPool → … → Flatten → Dense → Softmax
````

* 6 convolutional layers
* 1 dense layer with ReLU
* Final output layer with softmax (3 classes)

### ⚙️ Training Details

* Optimizer: Adam
* Loss: SparseCategoricalCrossentropy
* Epochs: 20
* Batch Size: 32
* Dataset split: 80% Train, 10% Validation, 10% Test

---

## 📊 Results

Model accuracy and loss are visualized using `matplotlib` for both training and validation sets.

You’ll see plots like:

* **Training & Validation Accuracy**
* **Training & Validation Loss**

---

## 🔍 Prediction

The model is used to predict the class of individual test images. It displays:

* Actual label
* Predicted label
* Prediction confidence (%)

Sample output:

```text
Actual: Potato_Late_blight
Predicted: Potato_Late_blight
Confidence: 98.5%
```

## 🛠️ Requirements

Install required packages:

```bash
pip install tensorflow matplotlib numpy
```

---

## 📁 Folder Structure

```text
.
├── PlantVillage/
│   ├── Potato__Early_blight/
│   ├── Potato_healthy/
│   └── Potato_Late_blight/
├── model_training.ipynb  # (your main notebook)
├── README.md
└── Model/
    └── 1/                # exported model
```

