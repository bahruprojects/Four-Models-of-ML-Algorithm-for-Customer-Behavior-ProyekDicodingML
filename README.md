# Four-Models-of-ML-Algorithm-for-Customer-Behavior-ProyekDicodingML
# Proyek Tugas Akhir 

## Setup Environment - Anaconda Navigator - Jupyter Notebook
```
conda create -- main-ds python=3.12.2
conda activate main-ds
pip install numpy
pip isntall pandas
pip install matplotlib
pip install seaborn
pip install sklearn

```
# Result
### Analisis Kelebihan dan Kelemahan Model:

#### 1. **Random Forest**
- **Kelebihan:**
  - Model memiliki **fitting yang sangat baik** dengan selisih antara training score dan testing score yang sangat kecil (**Difference: 0.0025**), menunjukkan bahwa model **tidak overfitting maupun underfitting**.
  - Performa per kelas sangat konsisten, dengan **Precision** dan **Recall** mendekati atau mencapai 1.0 di semua kelas.
- **Kelemahan:**
  - Tidak ada kelemahan signifikan dalam metrik yang diberikan. Model sangat optimal untuk dataset ini.

---

#### 2. **K-Nearest Neighbors (KNN)**
- **Kelebihan:**
  - Model memiliki **fitting yang baik**, dengan **Difference** hanya 0.0019, menunjukkan performa yang stabil pada training dan testing data.
  - Performa per kelas juga sangat baik, dengan **Precision** dan **Recall** mencapai nilai sempurna untuk beberapa kelas.
- **Kelemahan:**
  - Sama seperti Random Forest, KNN juga tidak menunjukkan kelemahan signifikan berdasarkan metrik yang diberikan.
  - Namun, KNN umumnya lebih lambat pada dataset besar dan bergantung pada metrik jarak, yang tidak terlihat dari hasil ini.

---

#### 3. **Decision Tree**
- **Kelebihan:**
  - Memiliki **Training Score** sempurna (**1.0000**) dan performa testing yang tinggi (**0.9949**).
  - **Precision** dan **Recall** cukup tinggi untuk semua kelas.
- **Kelemahan:**
  - **Difference** antara training dan testing score adalah yang terbesar (**0.0051**) dibandingkan model lain, menunjukkan bahwa model sedikit **overfitting** pada training data.
  - **Recall pada kelas 1** (0.9856) lebih rendah dibandingkan Precision (1.0000), yang dapat berarti model tidak menangkap semua instance dari kelas 1 dengan sempurna.

##### Precision atau Recall rendah Pada model tertentu 
- Semua model menunjukkan **Precision** dan **Recall** yang sangat tinggi di semua kelas, dengan sedikit penurunan pada:
  - **Decision Tree (Kelas 1):** Recall lebih rendah (0.9856), yang dapat memengaruhi kemampuan model dalam menangkap semua instance dari kelas tersebut.
##### Apakah model mengalami overfitting atau underfitting?
Saya mengambil 3 model saja, berikut adalah rinciannya:
- **Random Forest:** Tidak overfitting maupun underfitting (Training dan Testing Score sangat mirip).
- **KNN:** Tidak overfitting maupun underfitting (Difference sangat kecil, 0.0019).
- **Decision Tree:** Mengalami sedikit **overfitting** karena **Training Score** sempurna (1.0000) sementara Testing Score sedikit lebih rendah (0.9949) dengan **Difference 0.0051**.
