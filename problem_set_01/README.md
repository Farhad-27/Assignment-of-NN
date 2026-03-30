# Problem Set 01: Pediatric Chest X-Ray Classification

## Objective
Classify pediatric chest X-ray images into **Pneumonia** or **Normal** using Convolutional Neural Networks (CNN).

## Dataset
- **Total Images:** 5,863 (train, test, val folders)
- **Classes:** Pneumonia, Normal
- **Source:** Pediatric hospital X-ray dataset
- **Download:** [Dataset Link](https://drive.google.com/file/d/1219EeGE1XTJVXYaulynJSa3BXGsbNCLx/view?usp=sharing)

---

## Approach & Methodology

### 1. Data Preprocessing
- **Images resized to:** (128, 128)
- **Pixel values normalized** to range [0, 1]
- **Data augmentation applied on training data:**
  - Shear Range (0.2)
  - Zoom (0.2)
  - Horizontal flip

### 2. Model Architecture (CNN)
- **Input shape:** (128, 128, 3)
- **Convolutional Layers:**
  - Conv2D (32 filters) → ReLU → MaxPooling
  - Conv2D (64 filters) → ReLU → MaxPooling
- **Flatten layer:** Converts 2D feature maps to 1D vector.
- **Dense layer:** 128 neurons with ReLU activation.
- **Output layer:** 1 neuron with **Sigmoid** activation for binary classification.

### 3. Training
- **Optimizer:** Adam
- **Loss Function:** binary_crossentropy
- **Metrics:** Accuracy
- **Epochs:** 5
- **Batch size:** 32

---

## Findings & Evaluation
- **Model Performance:** The model successfully learns to distinguish between normal and pneumonia-affected lungs.
- **Training Accuracy:** ~93.00%
- **Validation Accuracy:** **87.50%**
- **Observation:** Data augmentation effectively reduced overfitting and improved the model's ability to generalize.

## Usage
1. Open the `.ipynb` file in Google Colab.
2. Ensure the dataset is loaded and extracted.
3. Run all cells sequentially to view results and accuracy plots.
