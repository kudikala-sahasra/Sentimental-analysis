# 💬 Emotion Detection with BERT (Multi-class Sentiment Analysis)

A powerful real-time **emotion classification system** using `BERT` and `Gradio`, trained on text data to detect emotions like **happy**, **sad**, **angry**, and more.

---

# 💬 Emotion Detection with BERT (Multi-class Sentiment Analysis)

A powerful real-time **emotion classification system** using `BERT` and `Gradio`, trained on text data to detect emotions like **happy**, **sad**, **angry**, and more.

---

## 📌 Project Objective

To build a deep learning model that can **classify emotions** from text using **BERT** and provide **real-time sentiment detection** through an interactive web interface.  
Applicable in:
- ✅ Customer feedback analysis  
- ✅ Chatbot emotional intelligence  
- ✅ Mental health monitoring  
- ✅ Social media emotion mining  

---

## 🗂 Dataset Details

- 📁 **File:** `smile-annotations-final.csv`  
- 📊 **Columns:** `id`, `text`, `category`  
- 🔢 **Labels:** Multi-class emotions (e.g., happy, sad, angry)

---

## ⚙️ Workflow Overview

| Step | Description |
|------|-------------|
| 🔹 **1. Data Preprocessing** | Filtered relevant labels, cleaned text, encoded emotions |
| 🔹 **2. Train-Validation Split** | 85% training, 15% validation using stratified sampling |
| 🔹 **3. Tokenization** | Used Hugging Face’s `BERT tokenizer` with padding and attention masks |
| 🔹 **4. Dataset Preparation** | Created PyTorch tensors for inputs and labels |
| 🔹 **5. Model Setup** | Used `BertForSequenceClassification` (`bert-base-uncased`) |
| 🔹 **6. Training** | Fine-tuned with `AdamW`, warm-up scheduler, F1 & Accuracy metrics |
| 🔹 **7. Evaluation** | Evaluated using **Weighted F1 Score** & per-class accuracy |
| 🔹 **8. Gradio Demo** | Built real-time user interface for predictions |

---

## 🧠 Model Architecture

- 🔸 Pretrained `bert-base-uncased` model  
- 🔸 Classification head added for multi-class output  
- 🔸 Optimized using `AdamW` + scheduler  
- 🔸 Fine-tuned with small batches to avoid memory issues

---

## 📉 Challenges & Solutions

| Challenge | Solution |
|----------|----------|
| ⚠️ Class imbalance | Used **Weighted F1 Score** for fair evaluation |
| ⚠️ Hardware constraints | Used small batch sizes and tuned learning rate |
| ⚠️ Noisy labels | Filtered and cleaned data before encoding |
| ⚠️ Deployment | Used `Gradio` for an easy-to-use web interface |

---

## 🧪 Metrics

- ✅ **Weighted F1 Score** (handles class imbalance)  
- ✅ **Accuracy Per Class**  
- ✅ **Validation Loss**

---

## 🖥 Demo - Gradio App

### 👉 Try it in real-time!

Just input a sentence and get instant emotion prediction 🎯

```python
import gradio as gr

def predict_emotion(text):
    # Load tokenizer, model and run inference here
    return "Predicted Emotion"

gr.Interface(fn=predict_emotion, inputs="text", outputs="text").launch()


