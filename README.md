# Real-Time Sign Language Detection Using Deep Learning

## 📌 Project Overview

The Real-Time Sign Language Detection project is a computer vision application that recognizes hand gestures using a webcam. It uses MediaPipe to extract hand landmarks and an LSTM (Long Short-Term Memory) deep learning model to classify sequences of hand movements in real time.

The system captures video frames, processes hand landmarks, and predicts the corresponding gesture class.

## 🎯 Project Objectives

- Detect hand gestures using a webcam.
- Extract hand landmarks and keypoints from video frames.
- Train a deep learning model to recognize gesture sequences.
- Predict hand gesture classes in real time.
- Explore computer vision and deep learning techniques for gesture recognition.

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Deep Learning Framework:** TensorFlow and Keras
- **Deep Learning Model:** LSTM (Long Short-Term Memory)
- **Computer Vision:** OpenCV
- **Hand Landmark Detection:** MediaPipe
- **Data Processing:** NumPy
- **Dataset Splitting:** Scikit-learn

## 🧠 Model Architecture

The project uses a Sequential neural network with the following layers:

- LSTM layer with 64 units
- LSTM layer with 128 units
- LSTM layer with 64 units
- Dense layer with 64 units
- Dense layer with 32 units
- Softmax output layer for gesture classification

### Model Configuration

- **Optimizer:** Adam
- **Loss Function:** Categorical Crossentropy
- **Evaluation Metric:** Categorical Accuracy
- **Training Epochs:** 200
- **Input Features:** 63 hand landmark coordinates per frame (21 landmarks × 3 coordinates)

The model processes sequences of hand landmarks to learn temporal patterns associated with different gestures.

## ⚙️ Project Workflow

1. **Webcam Capture:** OpenCV captures video frames from the webcam.
2. **Hand Landmark Extraction:** MediaPipe identifies hand landmarks.
3. **Data Preparation:** Hand landmark coordinates are prepared as sequential input data.
4. **Model Training:** The LSTM model learns patterns from labeled gesture sequences.
5. **Gesture Prediction:** The trained model predicts a gesture class from incoming webcam data.
6. **Real-Time Display:** The predicted class is displayed on the application window.

## 📂 Project Files

- `app.py` — Runs the real-time webcam gesture detection application.
- `collectdata.py` — Captures and saves hand gesture images for data collection.
- `data.py` — Extracts hand landmarks and prepares keypoint data.
- `trainmodel.py` — Defines, trains, and saves the LSTM model.
- `function.py` — Contains helper functions and project configuration.
- `model.json` — Stores the serialized model architecture.
- `model.h5` — Stores the saved trained model.

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Open the Project Folder

Open the downloaded project folder in Visual Studio Code.

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 4. Install Dependencies

Install the required libraries used by the project. Check the repository's dependency file, if available, for the compatible versions.

### 5. Run the Application

```bash
python app.py
```

Allow webcam access if prompted, then show your hand within the camera frame.

Press `q` in the webcam window to close the application.

## 🧪 Current Project Status

The application runs locally and displays gesture predictions from the trained model. The configured gesture classes include A, B, and C.

The model's accuracy and the exact hand shape associated with each class should be verified through testing against the training data.

## 🔮 Future Enhancements

- Add more hand gesture classes.
- Evaluate the model using a separate test dataset.
- Improve recognition under different lighting conditions.
- Test the model with different users and hand positions.
- Explore additional sign language gestures.
- Improve prediction stability during continuous movement.

## 👨‍💻 Author

**Aishwarya T**

B.Tech — Artificial Intelligence and Data Science

## 📄 License

Add a license if you intend to distribute this project under specific reuse conditions.