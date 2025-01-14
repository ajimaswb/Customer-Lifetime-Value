# Customer-Lifetime-Value

**Context**

Customer Lifetime Value (CLV) merupakan indikator yang menunjukkan nilai pelanggan bagi perusahaan. Melalui CLV, perusahaan dapat mengetahui potensi keuntungan dari setiap pelanggan serta mengukur biaya yang dikeluarkan untuk mendapatkan pelanggan baru atau mempertahankan yang sudah ada. Data ini penting bagi perusahaan untuk mengarahkan strategi pemasaran secara lebih efektif kepada pelanggan bernilai tinggi dan memahami perubahan perilaku pelanggan di masa mendatang.

Perusahaan asuransi menghasilkan pendapatan dari premi asuransi yang dibayarkan oleh pelanggan serta dari hasil aktivitas investasinya. Walaupun tidak semua pelanggan mengajukan klaim, ada persentase tertentu yang harus dipenuhi oleh perusahaan sesuai ketentuan polis. Untuk meningkatkan margin keuntungan, perusahaan cenderung fokus pada upaya meningkatkan pendapatan premi karena jumlah klaim yang diajukan pelanggan tidak dapat sepenuhnya dikendalikan. Strategi pemasaran yang efektif dan tepat sasaran menjadi kunci untuk mendorong peningkatan penjualan premi.

**Problem Statement**

Sebuah perusahaan asuransi kendaraan bermotor berupaya meningkatkan pendapatan dengan strategi pemasaran yang berfokus pada retensi pelanggan. Untuk memastikan kegiatan pemasaran yang dilakukan tepat sasaran, promosi atau penawaran perlu diarahkan kepada pelanggan yang sesuai. Hal ini dapat dilakukan dengan memanfaatkan Customer Lifetime Value (CLV). CLV mengukur total pendapatan yang diharapkan dapat diperoleh perusahaan dari seorang pelanggan selama masa loyalitasnya. Secara matematis, CLV dihitung dengan mengalikan rata-rata nilai pembelian, frekuensi pembelian, dan rata-rata retensi pelanggan dalam satuan tahun. Dengan memahami faktor-faktor yang memengaruhi CLV, seperti karakteristik pelanggan atau jenis layanan asuransi yang digunakan, perusahaan dapat merancang strategi pemasaran yang lebih efektif dan terarah.

**Goals**

Untuk mengatasi permasalahan tersebut, dirancang sebuah model machine learning yang bertujuan memprediksi nilai Customer Lifetime Value (CLV) berdasarkan data profil pelanggan dan jenis layanan asuransi yang dipilih. Nilai CLV yang dihasilkan dari model ini akan menjadi acuan bagi perusahaan asuransi dalam merancang strategi promosi yang sesuai dengan kebutuhan dan potensi masing-masing pelanggan. Dengan demikian, perusahaan dapat lebih efektif dalam mengalokasikan anggaran pemasaran, meningkatkan transaksi pelanggan, dan pada akhirnya, mendorong pertumbuhan pendapatan perusahaan secara keseluruhan.

**Conclusion**

Berdasarkan pemodelan yang sudah dilakukan, fitur 'Number of Policies' dan 'Monthly Premium Auto' menjadi fitur yang paling berpengaruh terhadap 'CLV'.

 Metrik evaluasi yang digunakan pada model adalah nilai RMSE, MAE & MAPE. Jika ditinjau dari nilai MAPE yang dihasilkan oleh model setelah dilakukan hyperparameter tuning, yaitu sebesar ~9%, kita dapat menyimpulkan bahwa bila nanti model yang kita buat ini digunakan untuk memperkirakan CLV pada rentang nilai seperti yang dilatih terhadap model (maksimal CLV USD 16624.75), maka perkiraan CLVnya rata-rata akan meleset kurang lebih sebesar 9% dari CLV seharusnya. 
 
 Berdasarkan analisis feature importances, fitur Number of Policies dan Monthly Premium Auto memiliki pengaruh paling signifikan terhadap model dalam memprediksi nilai Customer Lifetime Value (CLV). Kedua fitur ini memberikan kontribusi sangat tinggi, sehingga fitur lain menjadi terlihat kurang signifikan.

 Model ini tentu masih dapat diimporvisasi agar dapat menghasilkan prediksi yang lebih baik lagi. Namun, kita dapat melakukan A/B testing terhadap model yang sudah dibuat pada project ini untuk mengetahui tingkat efektifitas penggunaan model terhadap peningkatan pendapatan dari CLV. Nantinya, dari hasil A/B testing, kita bisa mendapatkan insight lainnya terkait perihal yang bisa dan harus diperbaiki pada model.

 **Segi Data:**

**1. Menambah Jumlah Data**: Dengan memperluas dataset pelatihan, model dapat belajar dari lebih banyak variasi pola, sehingga mengurangi risiko overfitting dan meningkatkan akurasi prediksi. 

**2. Menambahkan Fitur Relevan**: Memperkaya dataset dengan fitur-fitur seperti durasi pelanggan menjadi nasabah, informasi alamat, dan lainnya dapat memberikan konteks tambahan yang membantu model dalam memprediksi nilai CLV dengan lebih baik. 

**3. Mengembangkan Model Klasifikasi Loyalitas Pelanggan**: Dengan mengkategorikan nilai CLV menjadi dua kelas—pelanggan loyal dengan CLV tinggi dan tidak loyal dengan CLV rendah—dapat dibangun model klasifikasi yang membantu dalam segmentasi pelanggan dan pengambilan keputusan strategis. 

**4. Membangun Model Prediksi untuk Premi Bulanan**: Menganalisis faktor-faktor yang mempengaruhi besarnya premi bulanan yang dibayarkan pelanggan dengan menjadikan **Monthly Premium Auto** sebagai variabel dependen dapat memberikan wawasan berharga. Hal ini membantu dalam merancang strategi penetapan harga dan penawaran produk yang lebih efektif.

Dengan menerapkan langkah-langkah di atas, perusahaan asuransi dapat meningkatkan akurasi model prediksi CLV, memahami perilaku pelanggan dengan lebih baik, dan merancang strategi pemasaran yang lebih tepat sasaran. 

**Segi Bisnis:**

**1. Strategi Berdasarkan Fitur Number of Policies**

Meningkatkan Jumlah Polis yang Dimiliki Pelanggan:
Diskon atau Bundling Produk:
Tawarkan diskon bagi pelanggan yang membeli lebih dari satu jenis polis asuransi (contoh: bundling antara asuransi mobil, rumah, atau kesehatan).
Loyalty Program:
Berikan insentif (poin, cashback, atau hadiah) kepada pelanggan yang memperbarui atau menambah polis asuransi mereka.
Promosi Cross-Selling:
Edukasi pelanggan tentang manfaat memiliki beberapa polis asuransi dengan menawarkan solusi yang relevan untuk kebutuhan mereka.

**2. Strategi Berdasarkan Fitur Monthly Premium Auto**

Mengelola Premi Asuransi Bulanan:
Diskon untuk Pembayaran Tahunan:
Berikan potongan harga jika pelanggan memilih membayar premi secara tahunan, yang dapat meningkatkan nilai CLV sekaligus mengurangi risiko churn.
Penawaran Premi Berbasis Segmentasi:
Sesuaikan premi bulanan berdasarkan profil risiko pelanggan, sehingga premi terasa lebih terjangkau namun tetap menguntungkan perusahaan.
Kampanye Edukasi:
Tingkatkan pemahaman pelanggan tentang manfaat perlindungan asuransi yang sepadan dengan premi bulanan mereka untuk mencegah keraguan atau pembatalan.

**3. Strategi Gabungan**

Targeting Pelanggan dengan Potensi CLV Tinggi:
Gunakan segmentasi berbasis data untuk mengidentifikasi pelanggan yang memiliki potensi tinggi dalam meningkatkan jumlah polis atau premi bulanan.
Personalized Marketing:
Kirimkan penawaran khusus yang disesuaikan dengan kebutuhan masing-masing pelanggan, seperti rekomendasi polis tambahan yang relevan atau premi lebih fleksibel.

**4. Optimalisasi Pengalaman Pelanggan**

Peningkatan Layanan Pelanggan:
Pastikan pengalaman klaim dan pembelian polis mudah dan cepat untuk meningkatkan kepercayaan pelanggan.
Digital Engagement:
Gunakan aplikasi atau portal online yang memungkinkan pelanggan memantau polis mereka, memperbarui informasi, atau membeli produk baru dengan mudah.
