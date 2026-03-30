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

## Evaluation
- **Training Accuracy:** **93%**
- **Validation Accuracy:** **88%**
- **Final Test Accuracy:** **87%**

   ## Findings
- *High Classification Power:* Model successfully distinguishes between Pneumonia and Normal X-rays.
- *Generalization:* Data augmentation (Zoom, Flip, Shear) improved the model's ability to handle unseen data.
- *Overfitting Control:* Continuous validation monitoring helped in maintaining a balanced learning rate and controlled overfitting.
- *Real-world Applicability:* The model shows good performance and can be further refined for clinical assistant tools.

## Usage
1. Open the Pneumonia_classification.ipynb` file in Google Colab.
2. Ensure the dataset is loaded and extracted.
3. Run all cells sequentially to view results and accuracy plots.
