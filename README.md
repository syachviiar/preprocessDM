Analisis Variabel Tugas Pre-Processing Penambangan Data: 

Variabel yang tidak digunakan:
- NO (nomor identifikasi, biasanya tidak digunakan dalam model)
- NAMA (nama, biasanya juga tidak digunakan dalam model prediktif)

Variabel Atribut (fitur-fitur yang digunakan untuk memprediksi):
- USIA
- PARITAS (jumlah kelahiran hidup sebelumnya)
- JARAK KELAHIRAN (jarak antara kelahiran)
- RIW HIPERTENSI (riwayat hipertensi)
- RIW PE (riwayat preeklampsia)
- OBESITAS
- RIW DM (riwayat diabetes mellitus)
- RIW HIPERTENSI/PE DALAM KELUARGA
- SOSEK RENDAH (status sosial ekonomi rendah)

Variabel Target (variabel yang akan diprediksi):
- PE/Non PE (Preeklampsia atau tidak)

Deskripsi Tugas Pre-Processing Penambangan Data:
1. Mengimpor libraries: 
Menggunakan pandas dan numpy untuk manipulasi data dan LabelEncoder dari sklearn untuk mengubah nilai kategorikal menjadi numerik.
2. Membaca dataset: 
Menggunakan pd.read_excel() untuk membaca file excel.
3. Menghapus kolom yang tidak diperlukan: 
Kolom NO dan NAMA di-drop karena tidak akan digunakan.
4. Membersihkan kolom USIA: 
Menghapus string "TH" pada atribut usia dan mengubahnya ke integer.
5. Mengubah kategori JARAK KELAHIRAN: 
Mengubah kategori "< 2 tahun" dan "> 2 tahun" menjadi nilai biner 0 dan 1.
6. Mengubah data kategorikal yang lain: 
Menggunakan LabelEncoder untuk mengubah nilai "Ya"/"Tidak" atau kategori lain menjadi numerik.
7. Memeriksa hasil preprocessing:
print(df.head())
8. Menyimpan hasil preprocessing: 
Dataset yang sudah dipreprocessing disimpan kembali ke CSV.
