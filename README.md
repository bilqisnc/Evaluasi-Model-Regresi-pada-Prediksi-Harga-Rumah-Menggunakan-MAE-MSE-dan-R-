# Evaluasi-Model-Regresi-pada-Prediksi-Harga-Rumah-Menggunakan-MAE-MSE-dan-R-
Prediksi harga rumah dengan Lars, Linear Regression, dan Gradient Boosting, dievaluasi memakai MAE, MSE, dan R².
Jawaban

MAE dan MSE: jauh dari 1.
R²: dekat dengan 1.

Alasan (tulis di bawah jawaban)
MAE dan MSE adalah ukuran error yang nilainya bergantung pada skala data. Harga rumah angkanya besar, jadi MAE bernilai puluhan ribu dan MSE bernilai miliaran. Nilai idealnya 0, bukan 1, sehingga nilai yang jauh dari 1 tidak berarti model jelek.
R² mengukur seberapa besar variasi harga yang dijelaskan model. Nilainya 0 sampai 1 dan makin dekat 1 makin baik. Pada model terbaik (Gradient Boosting) R² sekitar 0,90.
Bukti dari hasil modelmu
Model	MAE	MSE	R²
Lars	±25.563	±1,59 × 10⁹	0,793
Linear Regression	±21.593	±1,20 × 10⁹	0,844
Gradient Boosting	±17.072	±8,00 × 10⁸	0,896

Angka ini baru benar setelah sel evaluasi di notebook diperbaiki (hapus load_diabetes()), jadi cocokkan dengan hasil notebook-mu.

Referensi pendukung
1. Fitri, E. (2023). Analisis Perbandingan Metode Regresi Linier, Random Forest Regression dan Gradient Boosted Trees Regression untuk Prediksi Harga Rumah. Journal of Applied Computer Science and Technology (JACOST), Vol 4 No 1, hlm 58–64.
Link: https://journal.isas.or.id/index.php/JACOST/article/view/491
Mendukung poin: model tree-based (Random Forest, Gradient Boosting) dibandingkan dengan regresi linear.

2. Haryanto, Rahaningsih & Basysyar (2023). Komparasi Algoritma Machine Learning dalam Memprediksi Harga Rumah. JATI (Jurnal Mahasiswa Teknik Informatika), Vol 7 No 1, Februari 2023.
Link: https://ejournal.itn.ac.id/jati/article/view/6343
Mendukung poin: Random Forest Regression menjadi algoritma terbaik dengan akurasi 81,6%. 
itn

3. Brahmantyo, A. R. (2023). Perbandingan Hasil Prediksi Harga Properti di Daerah Brooklyn Menggunakan XGBoost, Random Forest, dan Linear Regression. Jurnal Komputer dan Informatika (Untar), Vol 18 No 2, Oktober 2023, hlm 124–132.
Link: https://journal.untar.ac.id/index.php/JKI/article/view/34511/20624
Mendukung poin: landasan teori metrik. Artikel ini menjelaskan bahwa semakin tinggi R² semakin baik kecocokan model, dan semakin kecil MAE semakin baik. Catatan: hasilnya jelek (R² tertinggi hanya 0,014), jadi pakai untuk teori, bukan untuk membuktikan R² tinggi. Daftar pustakanya mengakses sumber per Desember 2024, jadi cek lagi tanggal terbit onlinenya. 
untar

4. Wijaya & Dwidasmara (2023). Uji Performansi Algoritma LR dan RFR pada Implementasi Sistem Prediksi Harga Rumah. Jurnal Nasional Teknologi Informasi dan Aplikasinya (JNATIA), Vol 1 No 3, Mei 2023.
Link: https://ejournal2.unud.ac.id/index.php/jnatia/article/view/8 (ini halaman artikel lain di jurnal yang sama, lihat bagian Similar Articles di halaman itu untuk menemukan artikel ini).
Mendukung poin: perbandingan regresi linear dan Random Forest untuk harga rumah.

5. Cahyani dkk. (2024). Comparison of Decision Tree, Linear Regression, and Random Forest Regressor Models for Predicting House Prices. Jurnal Ilmiah Merpati, Vol 12 No 1, April 2024.
Link: https://ojs.unud.ac.id/index.php/merpati/article/download/112815/55168
Ini terbit 2024, di luar rentang yang kamu minta, tapi paling cocok dengan tugasmu karena memakai dataset yang sama, dataset Kaggle dengan 1460 baris dan 81 kolom, dibagi 80% latih dan 20% uji. Hasilnya mirip punyamu: Random Forest MAE 18.672, MSE 8,48 × 10⁸, R² 0,889, sedangkan regresi linear R² 0,797. Ini bukti kuat bahwa MAE dan MSE besar tapi R² dekat 1.
