# 🍅 Smart Agriculture: Tomato Plant Disease Prediction Using CNN

## 📌 Project Overview

Smart Agriculture: Tomato Plant Disease Prediction is a Deep Learning project that uses a Convolutional Neural Network (CNN) to identify diseases in tomato plants from leaf images.

The system analyzes an uploaded tomato leaf image and predicts whether it is healthy or affected by a particular disease.

The main objective is to support farmers and agricultural users in identifying potential tomato plant diseases through image classification.

## 🎯 Project Objectives

- Identify tomato leaf diseases using image classification.
- Build a CNN-based deep learning model.
- Preprocess and classify tomato leaf images.
- Evaluate model performance using accuracy, precision, recall and F1-score.
- Predict diseases from new tomato leaf images.
- Deploy the trained model using Streamlit.

## 📊 Dataset

**Dataset:** PlantVillage Dataset

Source:
- [TensorFlow PlantVillage Dataset](https://www.tensorflow.org/datasets/catalog/plant_village)
- [Plant Disease Dataset – Kaggle](https://www.kaggle.com/datasets/emmarex/plantdisease)

This project uses the 10 tomato classes from the PlantVillage dataset.

### Tomato Disease Categories

1. Tomato Bacterial Spot
2. Tomato Early Blight
3. Tomato Late Blight
4. Tomato Leaf Mold
5. Tomato Septoria Leaf Spot
6. Tomato Spider Mites (Two-Spotted Spider Mite)
7. Tomato Target Spot
8. Tomato Yellow Leaf Curl Virus
9. Tomato Mosaic Virus
10. Tomato Healthy

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| JupyterLab | Development environment |
| TensorFlow | Deep Learning framework |
| Keras | CNN model development |
| NumPy | Numerical operations |
| Pandas | Data handling |
| Matplotlib | Data visualization |
| Scikit-learn | Model evaluation |
| Streamlit | Web application deployment |
| PlantVillage | Image dataset |

## 🧠 Model Architecture

The project uses a Convolutional Neural Network (CNN).

### CNN Layers

1. Input Layer – 128 × 128 × 3
2. Convolution Layer – 32 filters
3. Max Pooling Layer
4. Convolution Layer – 64 filters
5. Max Pooling Layer
6. Convolution Layer – 128 filters
7. Max Pooling Layer
8. Flatten Layer
9. Dense Layer – 128 neurons
10. Dropout Layer – 0.5
11. Output Layer – 10 classes with Softmax activation

### Model Configuration

- Optimizer: Adam
- Loss Function: Sparse Categorical Crossentropy
- Evaluation Metric: Accuracy
- Image Size: 128 × 128
- Batch Size: 32
- Initial Epochs: 15

## 📂 Project Structure

```text
tomato_disease_prediction/
│
├── data/
│   ├── tfds/
│   ├── tomato/
│   └── split/
│       ├── train/
│       ├── val/
│       └── test/
│
├── models/
│   └── tomato_disease_model.keras
│
├── notebooks/
│   └── tomato_disease_prediction.ipynb
│
├── app.py
├── class_names.json
├── requirements.txt
└── README.md
```

## ⚙️ Installation and Setup

### Step 1: Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/tomato_disease_prediction.git
```

### Step 2: Navigate to the project folder

```bash
cd tomato_disease_prediction
```

### Step 3: Create a Conda environment

```bash
conda create -n tomato_ai python=3.11 -y
```

### Step 4: Activate the environment

```bash
conda activate tomato_ai
```

### Step 5: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 6: Launch JupyterLab

```bash
jupyter lab
```

Open the notebook and select the `Python (tomato_ai)` kernel.

## 🚀 Model Training

The model training process consists of:

1. Loading the PlantVillage dataset.
2. Extracting tomato leaf images.
3. Splitting the dataset into training, validation and testing sets.
4. Resizing images to 128 × 128 pixels.
5. Normalizing pixel values between 0 and 1.
6. Building the CNN architecture.
7. Compiling the model using Adam optimizer.
8. Training the model for up to 15 epochs.
9. Evaluating the model on test images.

## 📈 Model Evaluation

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Training and Validation Accuracy
- Training and Validation Loss

Actual evaluation results should be added here after training.

**Test Accuracy:** Add your measured test accuracy here.

## 🔍 Disease Prediction

The trained model accepts a new tomato leaf image and returns:

- Predicted disease category.
- Prediction confidence percentage.

Example:

```text
Input: Tomato Leaf Image

Predicted Disease: Tomato___Early_blight

Confidence: Model-generated percentage
```

The example above illustrates the output format, not an actual prediction result.

## 🌐 Streamlit Deployment

The project includes a Streamlit web application for uploading tomato leaf images and predicting their disease category.

Run the following command:

```bash
streamlit run app.py
```

The application will open at:

```text
http://localhost:8501
```

Users can upload a JPG, JPEG or PNG tomato leaf image and view the model prediction.

## 💡 Future Improvements

- Improve model performance using data augmentation.
- Experiment with transfer learning using MobileNetV2.
- Test the model using real-world agricultural images.
- Add more crop disease categories.
- Build a mobile-friendly application.
- Provide disease prevention and treatment recommendations verified by agricultural experts.
- Deploy the application to a cloud platform.

## ⚠️ Limitations

The model is trained using PlantVillage images, which are largely collected under controlled conditions. Performance may decrease on real-world farm images with different backgrounds, lighting and camera quality.

Predictions should be treated as preliminary guidance, not a definitive agricultural diagnosis.

## 👨‍💻 Author

**Your Name:** Soumya Ranjan Meher

**Project:** Smart Agriculture – Tomato Plant Disease Prediction

**Domain:** Artificial Intelligence | Machine Learning | Deep Learning | Smart Agriculture

## 📜 License

This project is intended for educational and research purposes.

---

⭐ If you find this project useful, consider giving the repository a star!
