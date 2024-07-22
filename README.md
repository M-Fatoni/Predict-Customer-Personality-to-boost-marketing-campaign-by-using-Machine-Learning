# Overview

Sebuah perusahaan dapat berkembang dengan pesat saat mengetahui perilaku customer personality nya, sehingga dapat memberikan layanan serta manfaat lebih baik kepada customers yang berpotensi menjadi loyal customers. Dengan mengolah data historical marketing campaign guna menaikkan performa dan menyasar customers yang tepat agar dapat bertransaksi di platform perusahaan, dari insight data tersebut fokus kita adalah membuat sebuah model prediksi kluster sehingga memudahkan perusahaan dalam membuat keputusan.

# Insights

## 1. Conversion Rate Analysis Based on Income, Spending and Age

![img1](https://github.com/M-Fatoni/Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning/blob/main/img/cvr%20corr.JPG)

### **Interpretation:**

- ConversionRate memiliki korelasi yang cukup kuat dengan Income (0.66), TotalSpending (0.63), dan TotalTransaction (0.54). Hal ini menunjukkan bahwa pelanggan dengan pendapatan yang lebih tinggi cenderung memiliki tingkat konversi yang lebih tinggi, serta cenderung melakukan lebih banyak pembelian (TotalSpending dan TotalTransaction).
- Korelasi yang rendah antara Customer_Age (0.11) dan ConversionRate menunjukkan bahwa usia pelanggan tidak memiliki pengaruh signifikan terhadap tingkat konversi.

### **Recommendations:**

- Targeting Pelanggan dengan Pendapatan Tinggi: Fokus pada segmentasi dan strategi pemasaran untuk pelanggan dengan pendapatan tinggi, karena mereka memiliki korelasi yang signifikan dengan ConversionRate. Ini dapat termasuk penawaran eksklusif, produk premium, atau layanan tambahan yang sesuai dengan profil pelanggan ini.
- Optimasi Pengeluaran Pelanggan: Perhatikan pelanggan dengan Total Spending tinggi untuk memahami pola pembelian mereka lebih lanjut. Hal ini dapat membantu dalam mengoptimalkan strategi promosi, penawaran bundling, atau pengembangan produk yang sesuai dengan kebutuhan mereka.


## 2. Customer Segmentation using KMeans Clustering

![img 2](https://github.com/M-Fatoni/Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning/blob/main/img/elbow.JPG)

![img 3](https://github.com/M-Fatoni/Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning/blob/main/img/newplot.png)

![img 4](https://github.com/M-Fatoni/Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning/blob/main/img/silhouette.JPG)

## 3. Cluster Evaluation

![img 5](https://github.com/M-Fatoni/Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning/blob/main/img/cvr%20dist%20based%20clus.JPG)

**Cluster 3:** Memiliki tingkat konversi yang paling tinggi secara keseluruhan. Ini bisa mengindikasikan bahwa cluster ini memiliki karakteristik yang sangat menguntungkan untuk terjadinya konversi.

![img 6](https://github.com/M-Fatoni/Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning/blob/main/img/inc%20dist%20based%20clust.JPG)

- **Cluster 3:** Memiliki rata-rata pendapatan tertinggi dan distribusi yang cukup merata di sekitar rata-rata tersebut. Ini mengindikasikan bahwa sebagian besar anggota cluster ini memiliki pendapatan yang tinggi dan relatif konsisten.
- **Cluster 0:** Memiliki pendapatan yang paling rendah, akan tetapi memiliki distribusi yang paling luas.
- **Cluster 1** dan **Cluster 2:** Memiliki distribusi pendapatan yang berada di antara cluster 0 dan 3. Cluster 1 cenderung memiliki pendapatan yang sedikit lebih tinggi daripada cluster 2.

![img 7](https://github.com/M-Fatoni/Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning/blob/main/img/tot%20spend%20dist%20based%20clust.JPG)

**Cluster 3:** Memiliki rata-rata total pengeluaran tertinggi dan distribusi yang cukup merata di sekitar rata-rata tersebut. Ini mengindikasikan bahwa sebagian besar anggota cluster ini memiliki total pengeluaran yang tinggi dan relatif konsisten.

![img 8](https://github.com/M-Fatoni/Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning/blob/main/img/tot%20transc%20dist%20based%20clust.JPG)

Terdapat beberapa tumpang tindih (overlapping) antara cluster 3, 1, dan 2. Ini menunjukkan bahwa total transaksi di ketiga cluster tersebut relatif sama.

## 4. Business Recommendations

**Cluster 3: Pelanggan High-Value**
**Strategi:**
- **Program Loyalitas:** Implementasikan program loyalitas yang sangat menarik untuk mempertahankan dan meningkatkan keterlibatan pelanggan.
- **Personalisasi:** Tawarkan produk dan layanan yang sangat disesuaikan dengan preferensi individu.
- **Eksklusivitas:** Buat program atau event eksklusif untuk memberikan pengalaman belanja yang istimewa.
- **Cross-Selling dan Up-Selling:** Agressif dalam menawarkan produk atau layanan komplementer untuk meningkatkan nilai pesanan rata-rata.

**Cluster 1: Pelanggan Potensial**
**Strategi:**
- **Nurturing:** Lakukan upaya untuk meningkatkan frekuensi pembelian dan nilai pesanan rata-rata.
- **Personalisasi:** Tawarkan rekomendasi produk yang relevan berdasarkan riwayat pembelian.
- **Retargeting:** Gunakan iklan retargeting untuk mengingatkan pelanggan tentang produk yang pernah mereka lihat.
- **Promosi Khusus:** Tawarkan diskon atau promo khusus untuk mendorong pembelian pertama atau kedua.

**Cluster 2: Pelanggan Perlu Perhatian**
**Strategi:**
- **Analisis Mendalam:** Lakukan analisis lebih lanjut untuk memahami alasan mengapa pelanggan di cluster ini kurang aktif.
- **Personalisasi:** Tawarkan produk atau layanan yang sesuai dengan kebutuhan spesifik mereka.
- **Komunikasi:** Tingkatkan komunikasi dengan pelanggan melalui berbagai saluran (email, SMS, sosial media).
- **Promosi Khusus:** Tawarkan diskon atau promo khusus untuk menarik kembali pelanggan.

**Cluster 0: Tidak Berpotensi**
- Cluster 0 tampaknya tidak memiliki potensi untuk bisnis.
