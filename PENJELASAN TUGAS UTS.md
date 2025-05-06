# Tugas-UTS-Data-Mining
NAMA: Ahmad Khoerul Riski_NIM: 231011400989

Penjelasan dari tugas UTS
LAPORAN ANALISIS DAN KLASIFIKASI DATA SERANGAN JARINGAN
1. Deskripsi Dataset
Tiga dataset yang digunakan dalam proyek ini adalah:

DDoS ICMP Flood.csv

DDoS UDP Flood.csv

DoS ICMP Flood.csv

Masing-masing dataset berisi data lalu lintas jaringan yang mewakili serangan berbeda. Ketiganya digabung secara vertikal menggunakan pandas.concat() untuk membentuk satu dataset gabungan bernama hasilgabung.

2. Persiapan Data
Penggabungan Dataset: Dataset digabung secara vertikal (axis=0) dan indeks di-reset menggunakan ignore_index=True.

Seleksi Fitur dan Target:

Fitur (x) diambil dari kolom ke-7 hingga ke-75.

Label/Target (y) diambil dari kolom ke-83.

3. Pembagian Data
Dataset dibagi menjadi data latih dan data uji menggunakan train_test_split dari scikit-learn dengan parameter:

test_size=0.2 (20% data digunakan sebagai data uji)

random_state=42 (agar hasil konsisten)

4. Implementasi Model Klasifikasi
Dua algoritma machine learning digunakan:

Decision Tree dengan parameter criterion='entropy' dan splitter='random'.

Random Forest Classifier dengan n_estimators=100 dan n_jobs=-1 untuk efisiensi pemrosesan.

5. Evaluasi Model
Akurasi dari model Random Forest ditampilkan menggunakan accuracy_score.

Confusion Matrix divisualisasikan menggunakan Seaborn Heatmap untuk menunjukkan performa klasifikasi terhadap tiga jenis serangan:

DDoS ICMP Flood

DDoS UDP Flood

DoS ICMP Flood

6. Visualisasi Decision Tree
Pohon keputusan dari model Decision Tree divisualisasikan dengan plot_tree dari sklearn.tree, menampilkan nama fitur dan kelas target.

7. Pemrosesan Tambahan – Pembagian Data Horizontal
Setelah penggabungan dataset, dilakukan pembagian DataFrame secara horizontal:

Bagian kiri: kolom dari awal hingga tengah.

Bagian kanan: kolom dari tengah hingga akhir.

Hasil dari pembagian ini ditampilkan untuk keperluan eksplorasi lebih lanjut.

Kesimpulan
Proyek ini melakukan penggabungan dan analisis tiga dataset serangan jaringan.

Dua model klasifikasi diterapkan untuk memprediksi jenis serangan.

Random Forest memberikan performa klasifikasi yang baik berdasarkan akurasi dan confusion matrix.

Dataset juga dieksplorasi dengan pembagian kolom menjadi dua bagian (kiri dan kanan) untuk kemungkinan analisis lanjutan.

