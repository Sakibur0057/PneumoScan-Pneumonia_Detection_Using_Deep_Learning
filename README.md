# PneumoScan-Pneumonia-Detection-Using-Deep-Learning-on-Chest-X-ray-Images
# 🫁 PneumoScan
### Pneumonia Detection Using Deep Learning on Chest X-ray Images

PneumoScan is a deep learning-based image classification project that uses a **Convolutional Neural Network (CNN)** to classify chest X-ray images into two categories: **NORMAL** and **PNEUMONIA**.

The project aims to explore how deep learning and computer vision can be applied to medical image classification.

## 🎯 Project Objectives

- Develop a CNN model for pneumonia classification.
- Process and prepare chest X-ray images for training.
- Apply image augmentation to improve model generalization.
- Train and validate the CNN model.
- Evaluate model performance using test data.
- Generate predictions for unseen X-ray images.

## 📂 Dataset

This project uses the **Chest X-Ray Images (Pneumonia)** dataset.

The dataset contains two image categories:

- `NORMAL` – Chest X-ray images without pneumonia.
- `PNEUMONIA` – Chest X-ray images labeled as pneumonia.

The dataset is organized into three directories:

```text
chest_xray/
├── train/
│   ├── NORMAL/
│   └── PNEUMONIA/
├── test/
│   ├── NORMAL/
│   └── PNEUMONIA/
└── val/
    ├── NORMAL/
    └── PNEUMONIA/
```

**Dataset:** [Chest X-Ray Images (Pneumonia) – Kaggle](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)

## 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Convolutional Neural Network (CNN)

## 🧠 Model Architecture

The project implements a Sequential CNN model with the following layers:

| Layer | Configuration |
|---|---|
| Input | 150 × 150 × 3 |
| Conv2D | 32 filters, 3 × 3, ReLU |
| MaxPooling2D | 2 × 2 |
| Conv2D | 64 filters, 3 × 3, ReLU |
| MaxPooling2D | 2 × 2 |
| Flatten | Feature conversion |
| Dense | 128 neurons, ReLU |
| Output | 1 neuron, Sigmoid |

### Model Configuration

- **Optimizer:** Adam
- **Loss Function:** Binary Crossentropy
- **Evaluation Metric:** Accuracy
- **Epochs:** 10
- **Batch Size:** 32
- **Image Size:** 150 × 150 pixels

## ⚙️ Data Preprocessing

The following preprocessing techniques are applied:

1. Image rescaling (1/255) to normalize pixel values.
2. Shear transformation for training images.
3. Zoom augmentation.
4. Horizontal flipping.
5. Image resizing to 150 × 150 pixels.

These techniques help introduce image variations during training.

## 🚀 Installation and Usage

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/PneumoScan.git
cd PneumoScan
```

### 2. Install Dependencies

```bash
pip install numpy pandas matplotlib tensorflow
```

### 3. Download the Dataset

Download the Chest X-Ray Images (Pneumonia) dataset from Kaggle and extract it.

### 4. Configure Dataset Path

Update the dataset directory in the notebook:

```python
base_dir = "/path/to/chest_xray"
```

Ensure that the directory contains the `train`, `test`, and `val` folders.

### 5. Run the Project

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Run `cse424-project.ipynb` cell by cell to preprocess the images, train the CNN model, evaluate performance, and generate predictions.

## 📊 Model Performance

The model was trained for 10 epochs.

**Reported test accuracy:**

| Evaluation Metric | Result |
|---|---:|
| Test Accuracy | 84.78% |

The notebook also plots training accuracy and validation accuracy to visualize model learning over epochs.

## 📁 Project Structure

```text
PneumoScan/
│
├── cse424-project.ipynb
├── README.md
└── submission.csv
```

`submission.csv` contains the predicted class labels for the test images when the prediction cell is executed.

## 🔮 Future Improvements

- Experiment with deeper CNN architectures.
- Apply transfer learning using pretrained models.
- Improve model generalization.
- Evaluate precision, recall, F1-score, and confusion matrix.
- Develop a simple web interface for image classification.
- Explore explainable AI techniques for understanding model predictions.

## ⚠️ Disclaimer

PneumoScan is an academic machine learning project developed for educational and research purposes. It is not a clinically validated diagnostic system and should not be used as a substitute for professional medical evaluation.

## 👨‍💻 Project Information

**Course:** CSE 424

**Project Name:** PneumoScan

**Project Title:** Pneumonia Detection Using Deep Learning on Chest X-ray Images

**Project Type:** Deep Learning / Computer Vision / Medical Image Classification

---

⭐ If you find this project interesting, feel free to explore the notebook and its implementation.
