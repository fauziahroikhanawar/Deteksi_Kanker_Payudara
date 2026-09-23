# Analisis Clustering dan Klasifikasi untuk Deteksi Kanker Payudara Menggunakan K-Means dan Decision Tree

## Deskripsi Proyek
Proyek ini membangun sistem deteksi kanker payudara melalui integrasi K-Means Clustering dan Decision Tree Classifier pada dataset Breast Cancer (569 observasi, 30 fitur). K-Means mengidentifikasi 2 cluster optimal (Silhouette Score 0,3447), sedangkan Decision Tree dengan hyperparameter tuning (max_depth=4) mencapai akurasi 95,32% pada data uji dengan metrik Precision, Recall, dan F1-Score yang seimbang untuk kelas Benign dan Malignant.

## Tujuan
- Membangun sistem deteksi kanker payudara yang cepat dan akurat.
- Membangun model Decision Tree yang mudah dipahami dan diinterpretasikan.
- Mengidentifikasi fitur yang paling berpengaruh dalam membedakan tumor jinak dan ganas.

## Tools & Library
- Python 3
- Scikit-learn (K-Means, Decision Tree, GridSearchCV, PCA, metrik evaluasi)
- Pandas, NumPy (manipulasi data)
- Matplotlib (visualisasi)
- Google Colab

## Tahapan Proyek
1. **Load Data** - Dataset Breast Cancer dari Kaggle (569 observasi, 30 fitur)
2. **EDA** - Statistika deskriptif, cek missing values, distribusi kelas
3. **Preprocessing** - Hapus kolom Unnamed, Label Encoding, StandardScaler
4. **Clustering (K-Means)** - Penentuan k optimal via Silhouette Score (k=2), visualisasi PCA & centroid
5. **Klasifikasi (Decision Tree)** - Hyperparameter tuning via GridSearchCV (max_depth=4), split 70:30
6. **Evaluasi** - Accuracy, Precision, Recall, F1-Score, Confusion Matrix
7. **Interpretasi** - Visualisasi Decision Tree + Interactive Search

## Hasil
| Tahap | Hasil |
|---|---|
| **K-Means** | k=2 optimal (Silhouette Score 0,3447) |
| **Jarak antar centroid** | 6,594 (terpisah dengan baik) |
| **Cluster 0** | 188 data (fitur tinggi → Malignant) |
| **Cluster 1** | 381 data (fitur rendah → Benign) |
| **Decision Tree** | max_depth=4 (GridSearchCV 5-fold) |
| **Akurasi CV** | 92,72% |
| **Akurasi Test** | **95,32%** |
| **Precision/Recall/F1 (B)** | 0,96 / 0,96 / 0,96 |
| **Precision/Recall/F1 (M)** | 0,94 / 0,94 / 0,94 |

**Fitur paling berpengaruh (Decision Tree):** concave points_mean, texture_worst, area_worst.

## File Terkait
- Notebook: (./notebook/klasifikasi_kanker_payudara.ipynb)
- Dataset: Breast Cancer Dataset (Kaggle)<br>(https://www.kaggle.com/datasets/wasiqaliyasir/breast-cancer-dataset)

## Author
**Fauziah Roikhana Wardah** (dan tim Kelompok 08)
- Program Studi S1 Sains Data, Universitas Negeri Surabaya
