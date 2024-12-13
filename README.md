# SKINSENSE
## MACHINE LEARNING

### Introduction
This project develops an advanced multi-label classification model for product recommendations, leveraging machine learning techniques to predict products, features, and materials simultaneously. The system aims to provide personalized and precise product suggestions by analyzing complex input features.

### Dataset
- **Source**: Custom CSV dataset (`file_updated4.csv`) and dataset ingredients from https://www.beautyhaul.com/
- **Entries**: Comprehensive collection of product-related information
- **Key Features**: 
  - 14 input features
  - Multi-label classification across three categories
  - Encoded features for Produk, Fitur, and Bahan

### Exploratory Data Analysis
- **Preprocessing**: Multi-label encoding using `MultiLabelBinarizer`
- **Label Distribution**:
  - Produk: 12 categories
  - Fitur: 15 categories
  - Bahan: 10 categories
- **Feature Normalization**: MinMaxScaler applied to ensure consistent input scaling

### Model Architecture
- **Type**: Artificial Neural Network (ANN)
- **Input Layer**: 14 features
- **Hidden Layers**: 
  - First layer: 512 neurons
  - Second layer: 256 neurons
  - Third layer: 128 neurons
- **Regularization Techniques**:
  - Batch Normalization
  - Dropout (0.1 rate)
- **Output Layers**: 
  - Sigmoid activation
  - Independent predictions for Produk, Fitur, and Bahan

### Challenges
- **Multi-Label Classification**: Simultaneous prediction across three categories
- **Feature Encoding**: Converting categorical data to numerical representation
- **Maintaining Prediction Accuracy**: Balancing precision across different output layers

### Model Performance
- **Optimizer**: Stochastic Gradient Descent (SGD)
  - Learning Rate: 0.0065
  - Momentum: 0.95
- **Loss Function**: Binary Cross-Entropy
- **Evaluation Metrics**:
  - Accuracy for each output layer
  - Classification Reports
  - Loss and Accuracy tracking during training

### Model Versions
- Keras H5 (.h5)
- TensorFlow Lite (.tflite)

## Getting Started

### Prerequisites
- Python 3.8+
- Required Libraries:
  - TensorFlow 2.x
  - scikit-learn
  - pandas
  - numpy
  - matplotlib
  - joblib

### Installation

1. Clone the repository:
```bash
git clone [repository-url]
cd [repository-name]
```

2. Create virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```
