# EmoVision: Multimodal Mental Health Platform

EmoVision adalah platform kesehatan mental digital interaktif berbasis web yang dirancang sebagai ruang aman (*safe space*) bagi pengguna untuk mengenali, melacak, dan mengelola kondisi emosional secara mandiri. EmoVision hadir dengan pendekatan **Multimodal** yang mengombinasikan analisis teks berbasis **Natural Language Processing (NLP)** dan deteksi ekspresi wajah berbasis **Computer Vision** untuk memvalidasi perasaan pengguna secara objektif dan *real-time*.

---

## Proyek ini terdiri dari dua bagian utama:

### 1. Analisis Citra Wajah (Computer Vision)
Bagian ini berfokus pada deteksi ekspresi wajah pengguna untuk memvalidasi perasaan secara visual.
* **Tech Stack**: Python, Google Colab, Kaggle.
* **Struktur Folder**: `emovision-dataset-gambar/`
* **Proses**:
    * **Data Collection**: Pengumpulan dataset dalam tujuh kategori emosi (Happy, Sad, Neutral, Disgust, Surprise, Angry, Fear).
    * **Data Cleaning**: Standardisasi ukuran, peningkatan kualitas citra, dan pembersihan data.
* **Notebook**: `DATASET_GAMBAR_FINAL.ipynb`

### 2. Analisis Data Teks & Dashboard 
Bagian ini berfokus pada pemrosesan teks untuk mengidentifikasi sentimen dan kondisi emosional pengguna.
* **Tech Stack**: Python, Streamlit, Google Colab, Kaggle.
* **Struktur Folder**: `emovision-dataset-teks/`
* **Fitur Utama**:
    * **Visualisasi Wordcloud & SKI 2023**: Validasi urgensi proyek berdasarkan data survei kesehatan nasional.
    * **Analisis Sentimen**: Identifikasi kata kunci dominan terkait kondisi emosional dari data media sosial.
    * **Dashboard Interaktif**: Visualisasi hasil analisis untuk interpretasi pengguna.
* **Notebook**: `Data_Scientist_Dataset_Teks_CC26_PSU392.ipynb`

## Link Dataset 
https://s.id/Dataset-Emovision-CC26-PSU392

## Link Dashboard 
https://emovision-capstone.streamlit.app/ 