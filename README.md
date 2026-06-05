# 🎵 Explainable Spectro-Temporal Modeling for Indian Raga Classification Using Hybrid Neural Network

📄 **Project Overview** 

---

# 🎯 Introduction

* 🎶 Indian Classical Music is based on **Ragas**, which define melodic frameworks.
* 🎵 Each raga has:

  * ⬆️ Aroha (Ascending Notes)
  * ⬇️ Avaroha (Descending Notes)
  * 🎼 Pakad (Signature Phrase)
  * 😊 Rasa (Emotion/Mood)
* 🧑‍🎓 Manual raga identification requires expert knowledge.
* 🤔 Similar ragas often create confusion due to overlapping note patterns.
* 🌐 Large online music repositories need automated classification systems.
* ⚠️ Traditional methods struggle with:

  * 🎵 Microtones
  * 🌊 Meend (Pitch Glide)
  * 🎼 Gamaka (Ornamentation)
  * 🎤 Improvisation
* 🤖 AI and Deep Learning provide an effective solution.

---

# 📚 Literature Survey

### 🔹 Existing Research

* 🎧 MFCC + GMM used for music genre classification.
* 😊 SVM used for mood classification.
* 🔄 RNN used for raga recommendation systems.
* 📊 KNN and Naive Bayes used for raga classification.
* 🧠 MFCC + RNN-LSTM used for music genre recognition.
* 🎼 CNN used for Indian classical raga classification.

### ⚠️ Limitations

* ❌ Focused mainly on genre and mood classification.
* ❌ Limited raga-level identification.
* ❌ Lack of explainability.
* ❌ Poor temporal modeling.
* ❌ Black-box predictions.

---

# 🔍 Research Gap

* 📉 Insufficient research on individual raga classification.
* 🏗️ Traditional ML models cannot capture complex raga structures.
* ⚫ Deep learning models lack transparency.
* 🎵 Long-term melodic patterns are not effectively captured.
* ❌ No integrated CNN + LSTM + Explainable AI framework available.

---

# 🎯 Objectives

* ✅ Develop an accurate raga classification system.
* ✅ Capture both spectral and temporal information.
* ✅ Improve transparency using SHAP.
* ✅ Assist music education and research.
* ✅ Preserve Indian musical heritage digitally.

---

# ⚙️ Proposed Methodology

## 🎧 Step 1: Audio Preprocessing

* 🔄 Resampling audio to **22050 Hz**
* ✂️ Silence removal
* 📏 Standardizing audio length

---

## 🎼 Step 2: Feature Extraction (MFCC)

* 🎵 Extract 40 MFCC features.
* 📊 Generate MFCC Matrix:

  * ⏳ Time Frames = 216
  * 🎚️ Frequency Features = 40
* 🔲 Reshape to:

  * (216 × 40 × 1)

---

## 🧠 Step 3: CNN-LSTM Architecture

### 🔹 CNN Layer

* 🎯 64 Filters
* 📐 Kernel Size = 3
* ⚡ ReLU Activation
* 🎵 Extracts spectral patterns

### 🔹 Max Pooling

* 📉 Pool Size = 2
* 🚀 Reduces dimensions

### 🔹 Dropout

* 🛡️ Rate = 0.3
* Prevents overfitting

### 🔹 LSTM Layer

* 🔄 64 Memory Units
* 🎼 Learns temporal dependencies

### 🔹 Dense Layer

* 🔢 64 Neurons
* ⚡ ReLU Activation

### 🔹 Output Layer

* 🎯 Softmax Activation
* 🎼 Predicts 10 Raga Classes

---

## 🏋️ Step 4: Model Training

* ⚡ Adam Optimizer
* 📈 Learning Rate = 0.001
* 📦 Batch Size = 8
* 🔄 Epochs = 100
* ⏹️ Early Stopping
* 📉 Learning Rate Scheduler

---

## 🔍 Step 5: Explainable AI (SHAP)

* 🧩 SHAP (SHapley Additive Explanations)
* 📊 Global Feature Importance
* 🎯 Local Prediction Explanation
* 🔍 Understands model decisions

---

# 📂 Dataset Details

* 🎵 Total Audio Samples = **1130**
* 🎼 Total Ragas = **10**

### Included Ragas

* 🎶 Asavari
* 🎶 Bageshree
* 🎶 Bhairavi
* 🎶 Bhoop
* 🎶 Bhoopali
* 🎶 Darbari
* 🎶 Dkanada
* 🎶 Malkauns
* 🎶 Sarang
* 🎶 Yaman

---

# 📈 Results

## 🏆 Overall Performance

* 🎯 Accuracy = **95.56%**
* 🎯 Precision = **95.41%**
* 🎯 Recall = **95.56%**
* 🎯 F1 Score = **95.47%**

### 🌟 Best Performing Ragas

* 🎵 Malkauns → 97.97%
* 🎵 Darbari → 96.80%
* 🎵 Bhairavi → 96.04%

### 📌 Lowest Performing Raga

* 🎵 Bageshree → 91.52%

### 📊 ROC-AUC

* 🚀 Nearly 1.00 for all classes
* ✅ Excellent classification performance

---

# 🔎 SHAP Explainability Results

### ⭐ Most Important Features

* 🎯 MFCC-39
* 🎯 MFCC-32
* 🎯 MFCC-28

### 💡 Benefits

* 🔍 Explains predictions
* 🎵 Identifies influential musical features
* 🤝 Builds trust among musicians and researchers

---

# 📊 Comparative Analysis

| 🤖 Model           | 🎯 Accuracy |
| ------------------ | ----------- |
| KNN + Naive Bayes  | 80.10%      |
| MFCC + GMM         | 83.70%      |
| SVM                | 86.40%      |
| RNN-LSTM           | 88.60%      |
| CNN                | 91.56%      |
| 🏆 CNN-LSTM + SHAP | **95.56%**  |

### 📌 Observation

* 🚀 Proposed model achieved the highest performance.

---

# 🧪 Ablation Study

| Configuration              | Accuracy   |
| -------------------------- | ---------- |
| ❌ Without LSTM             | 81.62%     |
| ❌ Only 13 MFCCs            | 83.75%     |
| ❌ Without CNN              | 84.71%     |
| ❌ Without Silence Trimming | 85.42%     |
| ❌ Without Dropout          | 86.32%     |
| ❌ Without MaxPooling       | 88.05%     |
| ❌ Without Early Stopping   | 90.14%     |
| ✅ Full Model               | **95.56%** |

### 🔑 Key Findings

* 🎵 CNN captures spectral features.
* 🔄 LSTM captures temporal dependencies.
* 🎧 MFCCs provide rich audio representation.
* 🛡️ Dropout improves generalization.

---

# 🌟 Advantages

* 🎯 High Accuracy
* 🔍 Explainable Predictions
* 🎵 Effective Spectral + Temporal Learning
* 📚 Useful for Music Education
* 🗄️ Supports Digital Archives
* 🇮🇳 Preserves Indian Cultural Heritage

---

# 🌍 Applications

* 🎓 Intelligent Music Learning Systems
* 🎵 Automatic Raga Recognition
* 🗂️ Digital Music Archives
* 🎧 Music Recommendation Systems
* 🔬 Computational Musicology Research
* 📖 Music Education Platforms

---

# 📝 Conclusion

* ✅ Developed a Hybrid CNN-LSTM Model.
* ✅ Integrated SHAP Explainable AI.
* ✅ Achieved **95.56% Accuracy**.
* ✅ Outperformed existing machine learning and deep learning approaches.
* ✅ Provides transparent and trustworthy raga classification.
* ✅ Supports preservation and analysis of Indian Classical Music. 

---

# 🚀 Future Scope

* 🎼 Use Chroma Features and Spectral Contrast.
* 🎵 Include more ragas and gharanas.
* 🧠 Integrate Attention Mechanisms.
* ⚡ Develop Real-Time Raga Identification.
* 🎤 Live Concert Analysis and Feedback.
* 📱 Build Interactive Mobile Applications.
* 🔗 Multimodal Learning (Audio + Lyrics + Notation).
* 🤖 Advanced Explainable AI Techniques.
* 🌍 Global Digital Preservation of Indian Classical Music Heritage. 

✨ **One-Line Summary:**
🎶 *A high-accuracy (95.56%) CNN-LSTM + SHAP based Explainable AI system for automatic Indian Raga Classification and Musical Heritage Preservation.* 🎶

