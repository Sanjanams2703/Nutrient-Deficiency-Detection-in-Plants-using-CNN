# 🌱 Plant Nutrient Deficiency Detection with CNN & Fuzzy Logic  

This project presents an **Convolutional Neural Networks (CNNs)** combined with **fuzzy logic** to automatically identify nutritional deficiencies in plants. Designed for **precision agriculture**, the system supports early diagnosis, efficient nutrient management, and improved crop productivity.  

---

## 📖 Overview  

Nutrient deficiencies in plants directly affect **yield, growth, and quality**. Traditional manual inspection is subjective, time-consuming, and prone to human error.  
This project provides an automated pipeline that:  

- Analyzes **leaf images** using CNNs (VGG16 backbone).  
- Extracts deep visual features to detect deficiency symptoms.  
- Applies **fuzzy inference** for severity grading (Low, Medium, High).  
- Delivers interpretable outputs that help farmers take timely corrective actions.  

---

## 🎯 Goals  

- 📷 **Image Collection** – Use datasets like Kaggle’s *Plant Disease Dataset*.  
- 🧹 **Preprocessing** – Resize, normalize, and crop for consistent training.  
- 🌿 **Segmentation** – Focus primarily on leaf regions.  
- 🔍 **Feature Extraction** – Employ transfer learning with **VGG16**.  
- 🏷️ **Classification** – Categorize as *healthy* or *nutrient-deficient*.  
- 🧠 **Fuzzy Logic** – Map CNN confidence scores into interpretable severity levels.  

---

## 📊 Dataset  

Dataset Source: [Plant Disease Dataset on Kaggle](https://www.kaggle.com/datasets/saroz014/plant-disease)  
Includes **leaf samples** from multiple crops and nutrient conditions.  

---

## 🛠️ Methodology  

1. **Data Collection** – Curated plant leaf images covering various deficiencies.  
2. **Preprocessing** – Resized and normalized RGB images.  
3. **Model Training** – Fine-tuned **VGG16 CNN** for feature extraction & classification.  
4. **Fuzzy Inference Layer** –  
   - Membership functions: *Low*, *Medium*, *High*.  
   - Rules based on model confidence scores.  
5. **Prediction Pipeline** – CNN detects class → Fuzzy logic refines severity.  
6. **Evaluation** – Measured using **confusion matrix, precision, recall, F1-score**.  

---

## 🧰 Tools & Frameworks  

- **Programming** – Python  
- **Deep Learning** – TensorFlow, Keras  
- **Image Processing** – NumPy, Matplotlib  
- **Fuzzy Logic** – scikit-fuzzy (Mamdani inference system)  
- **Model** – Pre-trained VGG16 (transfer learning)  

---

## 📈 Performance  

| Class                   | Precision | Recall | F1-Score | Support |
|--------------------------|-----------|--------|----------|---------|
| Cherry (incl. sour)      | 1.00      | 1.00   | 1.00     | 190     |

- ✅ CNN + fuzzy logic consistently refined classification results  

---

## 🔗 CNN + Fuzzy Logic Integration  

- **CNN** → Provides raw confidence scores for predicted labels.  
- **Fuzzy System** → Maps confidence into severity categories:  
  - below 0.50 → **Low deficiency**  
  - 0.50–0.75 → **Medium deficiency**  
  - above 0.75 → **High deficiency**  

This ensures **explainable AI** instead of black-box predictions.  

---

## 🧪 Testing & Validation  

- Evaluated on **individual samples** and complete dataset batches.  
- Compared predicted labels against ground truth.  
- Generated **heatmap-based confusion matrix** for visual evaluation.  
- Metrics validated robustness across classes.  

---

## 📊 Results  

- The CNN showed **excellent generalization** to unseen data.  
- Fuzzy logic added **granularity and interpretability** to predictions.  
- Achieved **top scores across accuracy, precision, recall, and F1**.  
- Visualizations confirm **stable, high-performance results**.  

---

## 🚀 Conclusion  

This work demonstrates the potential of combining **deep learning** and **fuzzy inference** for **smart agriculture applications**. The hybrid system not only identifies nutrient deficiencies but also grades their severity, making it an effective tool for **farmers, agronomists, and researchers** working towards sustainable agriculture.  

---
