# 🧠 Image Captioning using CNN-LSTM

This project demonstrates **Image Captioning** – the process of generating meaningful textual descriptions from images using a hybrid **CNN + LSTM** deep learning architecture. It combines the power of **computer vision (CNN)** for feature extraction with **natural language processing (LSTM)** for text generation.

---

## 📌 Problem Statement

To create a model that can take an image as input and generate a relevant caption as output. This task lies at the intersection of **Computer Vision** and **NLP**.

---

## 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- CNN (DenseNet201)
- LSTM (Long Short-Term Memory)
- Custom Data Generator
- Matplotlib, Seaborn for visualization

---

## 🧱 Model Architecture

### 1. **Feature Extraction (CNN)**
- Pre-trained **DenseNet201** is used to extract feature vectors from input images.
- Final layer is removed to get a 1920-dimensional vector per image.

### 2. **Caption Generation (LSTM)**
- Image features and embedded captions are merged and passed through an LSTM layer.
- Final Dense layer with softmax activation predicts the next word in the sequence.

---

## 📂 Project Structure

- `IC CNN-LSTM.ipynb` – Main notebook with all training code
- Images stored in a local folder and processed using custom functions
- Features stored using a dictionary for efficiency

---

## 🔁 Training

- Early stopping and model checkpointing are used to avoid overfitting
- ReduceLROnPlateau helps manage the learning rate
- Training stops at best epoch based on validation loss

---

## 📉 Results

- Trained for 15 epochs with best model at epoch 10
- Validation loss: **~3.62**

---

## 🚧 Challenges Faced

- Tokenizing and padding varying-length captions
- Balancing training time with GPU limitations
- Avoiding overfitting with large vocabulary size

---

## 💡 Future Improvements

- Use **Transformers** or **Attention Mechanisms**
- Improve BLEU/ROUGE scoring metrics
- Optimize for real-time caption generation

