# 🧠 OCR Evaluation Tool

This project is a comprehensive **OCR (Optical Character Recognition) Evaluation Framework** designed to rigorously test and analyze the performance of custom OCR pipelines. It supports printed and handwritten text recognition, and delivers detailed performance insights including character-level metrics, word accuracy, and confusion matrices.

---

## 📁 Project Structure

- `dataset/img/` – Folder containing input images for OCR evaluation  
- `dataset/text/` – Corresponding ground truth `.txt` files  
- `backend.py` – Includes `extract_text()` for OCR inference and `preprocess_image()` for image preparation  
- `evaluate.py` – Main evaluation script computing metrics and visualizations

---

## 📊 Metrics Computed

- ✅ **Word-Level Accuracy**
- 🔠 **Character-Level Accuracy**
- ✏️ **Average Levenshtein Distance**
- 🎯 **Precision, Recall, and F1 Score (char-wise)**
- 🔍 **Character Confusion Matrix** via Seaborn heatmap

---

## 🛠️ How It Works

For each image in `dataset/img/`, the following is performed:

1. Ground truth is loaded from the corresponding `.txt` file.
2. The image is preprocessed using `preprocess_image`.
3. Text is extracted using a custom OCR engine via `extract_text`.
4. Evaluation metrics are computed:
   - Word-wise comparison
   - Character-wise match count
   - Levenshtein distance
   - Confusion matrix data

Results are accumulated and visualized in real-time.

---

## 🖥️ Sample Output (Console)

