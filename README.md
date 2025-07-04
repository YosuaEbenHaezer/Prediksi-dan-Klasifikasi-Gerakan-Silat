# Prediksi dan Klasifikasi Gerakan Silat

Repositori ini berisi proyek skripsi yang bertujuan untuk melakukan **prediksi koordinat gerakan 3 dimensi** dan **klasifikasi jenis gerakan** dalam pertandingan silat menggunakan algoritma **LSTM** dan **MediaPipe**.

---

## 🧠 Tujuan Penelitian

Membangun dua jenis model pembelajaran:
1. **Model Prediksi**  
   Untuk memprediksi koordinat 3 dimensi gerakan silat secara berurutan dari video pertandingan (menggunakan pendekatan *Time Series* dan **LSTM**).
   
2. **Model Klasifikasi**  
   Untuk mengklasifikasikan hasil prediksi koordinat ke dalam 3 kategori gerakan silat:
   - **Langkah**
   - **Tendangan**
   - **Kuda-kuda**
---

## 🔧 Teknologi & Tools
- **Bahasa**: Python
- **Framework**: TensorFlow / Keras
- **Pose Estimation**: [MediaPipe](https://google.github.io/mediapipe/)
- **Model**: LSTM (Long Short-Term Memory)
- **Data Format**: CSV dari hasil ekstraksi keypoints MediaPipe

---

## 🎥 Dataset Video Pertarungan Silat

Berikut adalah video yang digunakan sebagai sumber data gerakan:

1. **Igi Rangga B (TNI) vs Alvin Masaiz (Muba)**  
   - 🔗 [Tonton di YouTube](https://www.youtube.com/watch?v=h458Ykopes8)  
   - ⏱️ Durasi: 10:26  
   - 📌 Keterangan: Digunakan untuk pelatihan klasifikasi.

2. **Hanifan YK Kalahkan Malaysia 5:0 (Full)**  
   - 🔗 [Tonton di YouTube](https://www.youtube.com/watch?v=-l8dvoIWFoA)  
   - ⏱️ Durasi: 20:58  
   - 📌 Keterangan: Digunakan untuk pelatihan klasifikasi.

3. **Wewey Wita vs S. Lueangaphichation – Asian Games**  
   - 🔗 [Tonton di YouTube](https://www.youtube.com/watch?v=XV4bM_fkQDo)  
   - ⏱️ Durasi: 18:57  
   - 📌 Keterangan: Digunakan untuk pelatihan klasifikasi.

4. **Pipit Kamelia (DKI) vs Papua – Final Kelas D Putri**  
   - 🔗 [Tonton di YouTube](https://www.youtube.com/watch?v=Cdo5VYLJl9Y)  
   - ⏱️ Durasi: 12:12  
   - 📌 Keterangan: Digunakan untuk pelatihan klasifikasi.

5. **Hanifan YK vs Nguyen Trung – SEA Games 2022**  
   - 🔗 [Tonton di YouTube](https://www.youtube.com/watch?v=4Rj4otNSGCo)  
   - ⏱️ Durasi: 13:57  
   - 📌 Keterangan: Digunakan untuk pelatihan klasifikasi.

6. **INA vs VIE – Asian Games 2018, Final Kelas C Putra**  
   - 🔗 [Tonton di YouTube](https://www.youtube.com/watch?v=24KmFwdbT5Q&t=689s)  
   - ⏱️ Durasi: 30:54  
   - 📌 Keterangan: Digunakan untuk **pelatihan klasifikasi dan prediksi** berdasarkan bagian-bagian pertarungan.

---

## 📈 Output Model
### 1. Prediksi Koordinat
- Format output: Array 3D (frame x 33 keypoint x 3 koordinat)
- Model: LSTM yang dilatih menggunakan data sekuensial dari keypoint

### 2. Klasifikasi Gerakan
- Label: 23 jenis gerakan silat
- Input: Output koordinat dari model prediksi
- Output: Nama gerakan (Langkah, Tendang, Kuda-Kuda, dsb.)

---


Menambahkan sistem yang menjalankan kedua model.

![fiks_diagramalurpenelitian_silat (1) drawio (1)](https://github.com/user-attachments/assets/fc72eb39-ee48-4889-918e-b0d2cece7124)
