# HR Analysis Dashboard  

## 📌 Ringkasan Proyek  
Proyek ini bertujuan untuk membangun **HR Dashboard** yang dapat digunakan untuk **menganalisis dan memvisualisasikan data sumber daya manusia**. Dataset dalam proyek ini dibuat secara **sintetis** menggunakan kombinasi **ChatGPT prompts** dan **Python Faker library** untuk meniru data HR dunia nyata, termasuk:  
- **Demografi** (usia, gender, tingkat pendidikan)  
- **Detail pekerjaan** (departemen, jabatan, lokasi kerja)  
- **Informasi gaji**  
- **Evaluasi kinerja karyawan**  
- **Data attrition (keluar/mengundurkan diri)**  

Dashboard ini dikembangkan menggunakan **Tableau**, memberikan wawasan bagi tim HR untuk mendukung **perencanaan tenaga kerja, analisis gaji, dan evaluasi kinerja karyawan**.  

---

📊 **Dashboard Tableau**: [HR Analysis Dashboard](https://public.tableau.com/views/HRAnalysisDashboard_17362125848100/HRSummary?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## 📌 Cara Menggunakan Dashboard  
1. **Buka Tableau Dashboard** untuk menganalisis data karyawan.  
2. **Jelajahi Summary View** untuk melihat ringkasan metrik HR.  
3. **Gunakan Employee Records View** untuk analisis mendalam per individu.  
4. **Gunakan filter** untuk menyesuaikan data berdasarkan kebutuhan analisis.  

---

## 📌 Pembuatan Dataset  
Dataset ini dibuat dengan **Python** menggunakan **Faker library** untuk menghasilkan **8.950 data karyawan sintetis** dengan atribut realistis.  

### **Atribut Data**  
Setiap karyawan memiliki atribut berikut:  
1. **Employee ID** – Identifikasi unik untuk setiap karyawan.  
2. **Nama Lengkap** – Nama acak yang dihasilkan secara otomatis.  
3. **Gender** – Ditentukan secara probabilistik (**46% Female, 54% Male**).  
4. **Negara Bagian & Kota** – Dipilih secara acak dari daftar yang telah ditentukan.  
5. **Tanggal Diterima Kerja** – Ditentukan antara **2015 hingga 2024**, dengan distribusi probabilitas per tahun.  
6. **Departemen** – Ditentukan secara acak dengan **probabilitas tertentu** (IT, HR, Finance, dll.).  
7. **Jabatan** – Disesuaikan dengan departemen untuk mencerminkan struktur karir yang realistis.  
8. **Tingkat Pendidikan** – Ditentukan berdasarkan jabatan sesuai dengan kualifikasi dunia nyata.  
9. **Rating Kinerja** – Dikategorikan ke dalam **Excellent, Good, Satisfactory, dan Needs Improvement** dengan distribusi probabilitas tertentu.  
10. **Lembur (Overtime)** – Ditetapkan dengan probabilitas **30% Yes, 70% No**.  
11. **Gaji** – Ditentukan berdasarkan departemen dan jabatan dengan rentang yang sesuai.  
12. **Tanggal Lahir** – Disesuaikan dengan kelompok usia untuk memastikan konsistensi dengan jabatan dan pengalaman kerja.  
13. **Tanggal Pengunduran Diri** – Ditentukan untuk **11.2% karyawan** dengan aturan bahwa **minimal 6 bulan setelah tanggal diterima kerja**.  
14. **Gaji yang Disesuaikan** – Menggunakan faktor penyesuaian berdasarkan **gender, tingkat pendidikan, dan usia**.  


---

## 📌 User Story (Kebutuhan Pengguna)  
**Sebagai Manajer HR**, saya ingin memiliki **dashboard komprehensif** yang memungkinkan saya **menganalisis data karyawan**, baik dalam bentuk **ringkasan umum** maupun **detail per individu**.  

---

## 📌 Fitur Dashboard  

### 1️⃣ Ringkasan Data (Summary View)  
Bagian ini terbagi menjadi **tiga bagian utama**: **Overview, Demografi, dan Analisis Gaji**.  

![Tampilan Utama Dashboard](Icon%20and%20Design/HR%20Summary.png)

#### 📍 Overview  
- Menampilkan **jumlah total karyawan** (dipekerjakan, aktif, dan mengundurkan diri).  
- Menunjukkan **tren perekrutan dan pengunduran diri** setiap tahun.  
- Memvisualisasikan **jumlah karyawan berdasarkan departemen dan jabatan**.  
- Membandingkan **jumlah karyawan di kantor pusat (HQ) vs cabang**.  
- Memperlihatkan **distribusi karyawan berdasarkan kota dan negara bagian**.  


#### 📍 Demografi  
- Menampilkan **rasio gender** dalam perusahaan.  
- Memvisualisasikan **distribusi karyawan berdasarkan kelompok usia dan tingkat pendidikan**.  
- Menampilkan **jumlah karyawan berdasarkan kategori usia dan pendidikan**.  
- Menunjukkan **korelasi antara tingkat pendidikan dan rating kinerja karyawan**.  


#### 📍 Analisis Gaji (Income Analysis)  
- Membandingkan **gaji berdasarkan tingkat pendidikan dan gender**, untuk melihat apakah ada **ketimpangan gaji**.  
- Menganalisis **hubungan antara usia dan gaji** untuk karyawan di setiap departemen.  


---

### 2️⃣ Tampilan Detail Karyawan (Employee Records View)  
- Menampilkan **daftar lengkap karyawan**, termasuk **nama, departemen, jabatan, gender, usia, tingkat pendidikan, dan gaji**.  
- Memungkinkan pengguna **menyaring data berdasarkan kolom tertentu** untuk analisis lebih spesifik.  

![Employee Records View](Icon%20and%20Design/HR%20%20Details.png)


---

## 📌 Wawasan Penting dari Analisis  
🔹 **Karyawan dengan tingkat pendidikan lebih tinggi** cenderung memiliki **rating kinerja lebih baik**.  
🔹 **Perbedaan gaji antar gender** terlihat pada beberapa tingkat pendidikan tertentu.  
🔹 **Usia 30-45 tahun** merupakan kelompok dengan **gaji tertinggi** dalam beberapa departemen.  
🔹 **Tingkat pengunduran diri tertinggi** terjadi di beberapa departemen tertentu sehingga memerlukan strategi retensi karyawan yang lebih baik.  

---
