#  EmoVision Monorepo — Final Project Submission

<p align="center">
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/FastAPI-0.115-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/TensorFlow-2.15-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white"/>
  <img src="https://img.shields.io/badge/Gemini-AI-4285F4?style=for-the-badge&logo=google&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-Containerized-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Vercel-Hosted-000000?style=for-the-badge&logo=vercel&logoColor=white"/>
</p>

<p align="center">
  <b>EmoVision</b> adalah platform kesehatan mental digital interaktif berbasis web yang menggabungkan <b>Jurnaling Pintar</b> (NLP via mBERT) dan <b>Deteksi Ekspresi Wajah</b> (Computer Vision via TensorFlow). Sistem ini membantu pengguna mencatat luapan emosi harian, menerima umpan balik empati dari AI, serta menyediakan latihan pernapasan terpandu (Mindful Breathing) sebagai solusi preventif kesehatan mental.
</p>

---

## Daftar Isi

- [ Gambaran Umum EmoVision](#-gambaran-umum-emovision)
- [ Fitur Utama & Tambahan EmoVision](#-fitur-utama--tambahan-emovision)
- [ Dashboard & Tracking Angka](#-dashboard--tracking-angka)
- [ Arsitektur Teknologi](#%EF%B8%8F-arsitektur-teknologi)
- [ Tautan Penting Aplikasi Live](#-tautan-penting-aplikasi-live)
- [ Struktur Repositori Gabungan](#-struktur-repositori-gabungan)
- [ Petunjuk Setup Environment (.env.example)](#%EF%B8%8F-petunjuk-setup-environment-envexample)
- [ Cara Menjalankan Aplikasi Secara Lokal](#-cara-menjalankan-aplikasi-secara-lokal)
- [ Kategori Emosi yang Dikenali](#-kategori-emosi-yang-dikenali)
- [ Containerization & Deployment Cloud](#-containerization--deployment-cloud)
- [ Data Pengembang (Capstone Team)](#-data-pengembang-capstone-team)

---

## Gambaran Umum EmoVision
EmoVision adalah platform kesehatan mental digital interaktif berbasis web yang dirancang sebagai ruang aman (safe space) bagi pengguna untuk mengenali, melacak, dan mengelola kondisi emosional mereka secara mandiri. Berbeda dengan aplikasi jurnal konvensional yang cenderung pasif dan searah, EmoVision hadir dengan pendekatan Multimodal yang responsif. Aplikasi ini mengombinasikan analisis teks berbasis Natural Language Processing (NLP) dan deteksi ekspresi wajah berbasis Computer Vision untuk memvalidasi perasaan pengguna secara objektif dan real-time.

## Fitur Utama & Tambahan EmoVision 
EmoVision memisahkan fungsionalitasnya ke dalam dua kategori intervensi kesehatan mental yang saling berkesinambungan:
1. Fitur Utama
- Journaling dengan AI Feedback: Pengguna dapat menuangkan keluh kesah atau cerita harian mereka ke dalam jurnal digital. Setelah jurnal disimpan, sistem AI Generate berbasis NLP (mBERT) akan menganalisis sentimen dari tulisan tersebut dan memberikan umpan balik (feedback) berupa kalimat respons yang empati, hangat, dan dipersonalisasi khusus sesuai kondisi hati pengguna.  
- Face Mood Detection: Melalui integrasi kamera web, aplikasi ini mampu memindai ekspresi wajah pengguna untuk mendeteksi emosi secara objektif. Hasil pemindaian real-time ini mengklasifikasikan emosi ke dalam 7 kategori utama (Happy, Sad, Neutral, Angry, Fear, Disgust, Surprise) lengkap dengan skor akurasi persentase yang dinamis.  
2. Fitur Tambahan
- Affirmation (Afirmasi Positif): Fitur yang menyediakan kutipan harian dan kalimat-kalimat penguatan positif yang dirancang untuk membangun motivasi, meningkatkan rasa percaya diri, serta membantu pengguna memprogram ulang pikiran mereka ke arah yang lebih optimis setiap harinya.
- Mindful Breathing (Latihan Pernapasan): Sebagai bentuk pertolongan pertama psikologis (psychological first-aid), EmoVision menyediakan fitur latihan pernapasan terpandu secara interaktif. Fitur ini berfungsi membantu pengguna meredakan kecemasan, mengelola stres, atau menenangkan diri secara instan, terutama saat sistem mendeteksi adanya indikasi emosi negatif yang kuat.

## Dashboard & Tracking
Semua riwayat emosi dan jurnal harian pengguna akan direkam secara aman ke dalam database. Data ini kemudian disajikan kembali kepada pengguna di halaman Dashboard dalam bentuk Graphic Mood mingguan dan sistem User Streak (konsistensi mencatat jurnal) untuk memotivasi pengguna agar tetap rutin merawat kesehatan mental mereka.

## Arsitektur Teknologi
Secara teknis, EmoVision dibangun dengan arsitektur modern yang memisahkan tanggung jawab setiap komponen agar aplikasi berjalan sangat cepat dalam hitungan detik:

![Arsitektur Sistem EmoVision](arsitektur-sistem.png)

- Frontend: Menggunakan React.js dan Tailwind CSS yang dideploy di Vercel untuk menyajikan antarmuka pengguna yang estetik, responsif, dan ramah pengguna.  
- Backend RESTful API: Menggunakan Node.js dengan framework Express.js yang dihosting di Railway, bertugas sebagai pengatur lalu lintas data serta mengelola database PostgreSQL.
- Core AI API: Menggunakan Python dengan framework FastAPI yang dikemas di dalam Docker dan berjalan di Hugging Face Spaces. Sektor ini menggerakkan model deep learning TensorFlow untuk deteksi wajah serta arsitektur mBERT untuk analisis teks jurnal.

## Tautan Penting Aplikasi Live

* **Website Produksi (Frontend Live):** [https://emovision-app.vercel.app](https://emovision-app.vercel.app)
* **Base URL Backend API (Railway):** `https://emovision-backend-production.up.railway.app`
* **Base URL Core AI API (Hugging Face Spaces):** `https://fadidinna-emovision-api.hf.space`
* **Tautan Unduh Model ML (Google Drive):** `https://drive.google.com/drive/folders/1DmBS1H5JtD32gFAz_nsQ951Jzax24dbU?usp=sharing`
---

##  Struktur Repositori Gabungan

Repositori ini mengonsolidasikan seluruh *codebase* EmoVision ke dalam satu struktur folder monorepo yang rapi:

```text
emovision-monorepo/
├── emovision-frontend/     # Aplikasi Client-Side (React.js + Tailwind CSS)
├── emovision-backend/      # RESTful API & Database Controller (Node.js + Express + PostgreSQL)
├── emovision-ai-api/       # Core Machine Learning API Service (Python + FastAPI + mBERT + TensorFlow)
└── README.md               # Dokumentasi utama pengumpulan proyek
```
## Petunjuk Setup Environment (.env.example)

Untuk menjalankan seluruh ekosistem aplikasi ini secara lokal, Anda wajib menyalin template environment variable berikut ke file .env di masing-masing folder komponen:

1. Environment Frontend (emovision-frontend/.env)

```bash
VITE_API_URL=[https://emovision-backend-production.up.railway.app](https://emovision-backend-production.up.railway.app)
```

2. Environment Backend (emovision-backend/.env)

```bash
PORT=5000
DATABASE_URL=postgresql://username:password@host:port/database_name
JWT_SECRET=isi_kode_rahasia_jwt
```

3. Environment Core AI API (emovision-ai-api/.env)

```bash
GEMINI_API_KEY=isi_api_key_gemini_anda_disini
```

## Cara Menjalankan Aplikasi Secara Lokal
1. Menjalankan Layanan AI API (Python & FastAPI)

- Masuk ke folder layanan AI:
```Bash   
cd emovision-ai-api
```
- Buat dan aktifkan virtual environment (Disarankan Python 3.11):  
```Bash   
python -m venv venv
source venv/bin/activate  # Linux / macOS
venv\Scripts\activate     # Windows
```
- Install seluruh dependensi yang diperlukan:  
```Bash   
pip install -r requirements.txt
```
- Jalankan server FastAPI menggunakan Uvicorn:  
```Bash   
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```
2. Menjalankan Layanan Backend (Node.js & Express)
- Masuk ke folder backend:
```Bash   
cd emovision-backend
```
- Install seluruh dependensi package:
```Bash   
npm install
```
- Jalankan server backend dalam mode pengembangan:
```Bash  
npm run dev
```
3. Menjalankan Layanan Frontend (React.js via Vite)
- Masuk ke folder frontend:
```Bash   
cd emovision-frontend
```
- Install seluruh dependensi node modules:
```Bash   
npm install
```
- Jalankan server lokal frontend:
```Bash   
npm run dev
```
- Akses aplikasi lokal melalui browser di http://localhost:5173.

## Kategori Emosi yang Dikenali
Sistem kecerdasan buatan EmoVision dilatih untuk memproses teks jurnal dan mengenali 7 kelas emosi utama secara mendalam dengan rincian sebagai berikut:  
| Label Emosi | Deskripsi Kondisi Pengguna | Fitur Intervensi Tambahan |
| :--- | :--- | :--- |
| 😠 **Angry** | Ekspresi marah, dongkol, atau frustrasi berat | Pengalihan ke fitur *Mindful Breathing* |
| 🤢 **Disgust** | Ekspresi muak, benci, atau ketidaknyamanan emosi | Validasi empati otomatis via AI Insight |
| 😨 **Fear** | Ekspresi takut, gugup, atau kecemasan intens | Penanganan mandiri via *Mindful Breathing* |
| 😊 **Happy** | Ekspresi bahagia, senang, atau bersyukur | Pencatatan riwayat grafik kontribusi *streak* |
| 😐 **Neutral**| Ekspresi tenang, datar, atau emosi seimbang | Motivasi harian dan afirmasi positif |
| 😢 **Sad** | Ekspresi sedih, kecewa, atau suasana hati murung | Validasi & dukungan penguatan psikologis |
| 😲 **Surprise**| Ekspresi terkejut, kaget, atau tidak menyangka | Analisis kontekstual teks jurnal mendalam |

## Containerization & Deployment Cloud
- Docker & Hugging Face: Komponen AI API dikemas menggunakan konfigurasi Dockerfile agar menjamin konsistensi environment model saat dijalankan di platform Hugging Face Spaces.

- Graceful Error Handling: Sisi Frontend React dilengkapi dengan mekanisme interseptor error khusus. Jika layanan API eksternal (seperti limit kuota gratisan Gemini API) mengalami lonjakan trafik (503 Service Unavailable), sistem frontend akan menangkapnya secara mandiri dan menggantinya dengan pesan interaktif ramah pengguna tanpa merusak jalannya aplikasi.

## Tech Stack Data Scientist
Proyek ini dibangun menggunakan teknologi berikut:
- **Python**: Bahasa pemrograman utama untuk pengolahan dan analisis data.
- **Streamlit**: *Framework* utama untuk pengembangan *dashboard* interaktif.
- **Google Colab**: Tools pengembangan berbasis *cloud* untuk kolaborasi dan pengolahan data.
- **Kaggle**: Sumber dataset sekunder untuk riset dan pengembangan model.

---

## Data Pengembang (Capstone Team)

Berikut adalah data keanggotaan kelompok pengembang tim proyek capstone EmoVision:

| Nama | ID | Universitas | Learning Path |
| :--- | :--- | :--- | :--- |
| Hildyah Maretasya Araffad | CACC119D6X2214 | Institut Teknologi Sumatera | AI Engineer |
| Atika Adelia | CDCC119D6X2248 | Institut Teknologi Sumatera | Data Scientist |
| Elfa Noviana Sari | CACC119D6X2318 | Institut Teknologi Sumatera | AI Engineer |
| Fadzilah Saputri | CFCC119D6X2340 | Institut Teknologi Sumatera | FullStack Web Developer |
| Fadina Mustika Ratnaningsih | CFCC119D6X2423 | Institut Teknologi Sumatera | FullStack Web Developer |
| Charista Septi Dwi Artamy | CDCC183D6X2720 | Universitas Amikom Yogyakarta | Data Scientist |

---