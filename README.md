# Prototipe IndoRPL: Sistem Integrasi NER, RE, dan QA

Repositori ini berisi kode prototipe terintegrasi dan *weights* model NLP berbasis **IndoRPL** yang dirancang khusus untuk menganalisis teks abstrak ilmiah/bidang *Software Engineering*.

Sistem ini menggabungkan 3 tugas pemrosesan bahasa alami (NLP) utama dalam satu alur kerja (*pipeline*):
1. **Named Entity Recognition (NER)**: Mengekstraksi entitas kunci dari teks.
2. **Relation Extraction (RE)**: Menganalisis hubungan relasi antar entitas yang terdeteksi.
3. **Question Answering (QA)**: Menjawab pertanyaan berbasis konteks dari teks input secara otomatis.

---
## Cara Menjalankan Prototipe di Google Colab

Seluruh alur pengunduhan model Git LFS dan penginstalan dependensi sudah diotomatisasi di dalam notebook. Anda **tidak perlu mengunduh file model secara manual**.

### Langkah-langkah:

1. **Buka Notebook di Colab**  
   Klik tombol **Open In Colab** di atas atau buka file `prototype_code.ipynb` langsung di Google Colab.

2. **Jalankan Semua Sel (*Run All*)**  
   Pada menu bagian atas Colab, klik **Runtime** $\rightarrow$ **Run all**.

3. **Tunggu Proses Download Model**  
   Skrip otomatis di sel awal Colab akan memasang Git LFS dan mengunduh ketiga model IndoRPL (`indorpl-ner`, `indorpl-re`, dan `indorpl-qa`) dari repositori ini secara otomatis.

4. **Akses Antarmuka Gradio UI**  
   Setelah semua sel selesai dijalankan, gulir ke sel paling bawah. Antarmuka interaktif **Gradio UI** akan muncul langsung di dalam notebook, atau Anda dapat mengklik **Public URL** yang dihasilkan untuk membukanya di tab baru.

---
## Fitur Antarmuka Pengguna (Gradio UI)

Aplikasi ini dilengkapi antarmuka interaktif untuk mempermudah analisis:
* **Input Teks Abstrak:** Tempat memasukkan teks abstrak ilmiah yang ingin dianalisis.
* **Input Pertanyaan:** Memungkinkan pengisian beberapa pertanyaan sekaligus (*multiline*).
* **Tab Hasil Analisis:**
  * **Tab 1 (Hasil NER):** Menampilkan tabel entitas terdeteksi beserta nilai *Confidence Score*.
  * **Tab 2 (Hasil RE):** Menampilkan tabel relasi yang terbentuk antar entitas.
  * **Tab 3 (Hasil QA):** Menampilkan jawaban ekstraktif untuk setiap pertanyaan yang diajukan.

---
