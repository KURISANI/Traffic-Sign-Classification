# 🚦 Traffic Signs Classification with CNN

A deep learning project that classifies German traffic signs using a Convolutional Neural Network (CNN) built with TensorFlow and Keras. This model can be used by smart cars to recognize traffic signs in real-time.

## 📌 Project Overview

This project uses the **GTSRB (German Traffic Sign Recognition Benchmark)** dataset to train a CNN model that classifies 43 different traffic signs. The model achieves **over 95% accuracy** on the test set.

**Key Features:**
- Classifies 43 different traffic signs
- Achieves 98%+ training accuracy
- Uses dropout for regularization to prevent overfitting
- Includes data preprocessing and normalization
- Visualizes training progress with accuracy/loss curves

## 🛠️ Tools & Technologies

| Category | Tools |
|----------|-------|
| **Framework** | TensorFlow / Keras |
| **Language** | Python 3 |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **Image Processing** | PIL (Pillow) |
| **Data Splitting** | Scikit-learn |

## 📁 Dataset

- **Source:** GTSRB – German Traffic Sign Recognition Benchmark (Kaggle)
- **Classes:** 43 different traffic signs
- **Training images:** ~39,000
- **Test images:** ~12,000
- **Image size:** Resized to 50x50 pixels
- **Labels:** Speed limits, warnings, prohibitions, mandatory signs, etc.

## 🧠 Model Architecture
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━┓
┃ Layer (type) ┃ Output Shape ┃ Param # ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━┩
│ conv2d (Conv2D) │ (None, 50, 50, 64) │ 1,792 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ max_pooling2d (MaxPooling2D) │ (None, 25, 25, 64) │ 0 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ conv2d_1 (Conv2D) │ (None, 23, 23, 64) │ 36,928 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ max_pooling2d_1 (MaxPooling2D) │ (None, 11, 11, 64) │ 0 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dropout (Dropout) │ (None, 11, 11, 64) │ 0 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ flatten (Flatten) │ (None, 7744) │ 0 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dense (Dense) │ (None, 128) │ 991,360 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dropout_1 (Dropout) │ (None, 128) │ 0 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dense_1 (Dense) │ (None, 43) │ 5,547 │
└─────────────────────────────────┴────────────────────────┴───────────────┘
Total params: 1,035,627 (3.95 MB)
Trainable params: 1,035,627 (3.95 MB)
Non-trainable params: 0 (0.00 B)


## 📊 Results

| Metric | Value |
|--------|-------|
| **Training Accuracy** | 98.35% |
| **Validation Accuracy** | 99.68% |
| **Test Accuracy** | ~95%+ |
| **Epochs** | 50 |
| **Batch Size** | 128 |

### Sample Predictions

| Original Label | Predicted Label | Status |
|----------------|-----------------|--------|
| Speed limit (30km/h) | Speed limit (30km/h) | ✅ Correct |
| Speed limit (70km/h) | Speed limit (70km/h) | ✅ Correct |
| Yield | Yield | ✅ Correct |
| Stop | Stop | ✅ Correct |

## 🚀 How to Run

### 1. Clone this repository
```bash
git clone https://github.com/YOUR_USERNAME/traffic-sign-classification.git
cd traffic-sign-classification
```

### 2. Install dependencies
pip install -r requirements.txt

### 3. Run the notebook

-Open traffic_sign_classification.ipynb in Jupyter Notebook or Google Colab

-Run all cells sequentially

### 4.  Kaggle API Setup (if downloading dataset)

1. Get your Kaggle API key from kaggle.com

2. Upload kaggle.json to Colab or place in ~/.kaggle/

3. The notebook will automatically download the dataset


📈 Visualizations
The notebook includes:

-Sample images from each class

-Training/validation accuracy curves

-Training/validation loss curves

-Prediction examples with labels

🔮 Future Improvements

-Hyperparameter tuning for higher accuracy

-Data augmentation (rotation, zoom, brightness)

-Deploy model as a web app using Streamlit

-Implement real-time camera detection

-Try transfer learning with pre-trained models

🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

👨‍💻 Author
McCauley Mabedhle

Data Scientist | Data Engineer

GitHub: https://github.com/KURISANI

LinkedIn: https://www.linkedin.com/in/mccauley-mabedhle-3ab022280/

Email: Kurisanimabedhle@gmail.com

📄 License
This project is open source and available under the MIT License.

🙏 Acknowledgements
- GTSRB Dataset on Kaggle

- TensorFlow and Keras documentation

- German Traffic Sign Recognition Benchmark paper
