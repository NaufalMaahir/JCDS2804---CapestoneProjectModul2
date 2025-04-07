# JCDS2804---CapestoneProjectModul2

# Analisis Pelanggan Supermarket: Segmentasi dan Risiko Churn

## Deskripsi Proyek
Proyek ini merupakan bagian dari analisis data pelanggan supermarket menggunakan dataset `Supermarket_Customers.csv`. Tujuan utama proyek ini adalah untuk memahami perilaku pelanggan melalui segmentasi berdasarkan pendapatan (`Income`) dan pengeluaran (`Total Spending`), mengidentifikasi pelanggan berisiko churn tinggi berdasarkan `Recency`, serta melakukan penanganan outlier untuk distribusi `Income`. Analisis dilakukan menggunakan Python (Jupyter Notebook) untuk pemrosesan data dan visualisasi awal, serta Tableau untuk membuat dashboard interaktif.

### Tujuan
1. Menganalisis distribusi `Recency` untuk pelanggan berisiko churn tinggi.
2. Melakukan segmentasi pelanggan berdasarkan `Income` dan `Total Spending` (Low, Medium, High).
3. Membersihkan data dengan penanganan outlier pada kolom `Income` menggunakan metode IQR.
4. Membuat dashboard interaktif di Tableau untuk memvisualisasikan hasil analisis.

---

## Langkah-Langkah Analisis
1. **Pembersihan Data**:
   - Dataset awal (`Supermarket_Customers.csv`) dibersihkan untuk menangani nilai yang hilang dan outlier.
   - Penanganan outlier dilakukan pada kolom `Income` menggunakan metode IQR (Interquartile Range), menghasilkan dataset baru dengan 2232 baris (dari awalnya 2240 baris).

2. **Analisis Risiko Churn**:
   - Pelanggan berisiko churn tinggi diidentifikasi berdasarkan `Recency` di atas kuartil ke-75 (threshold: 74 hari).
   - Histogram distribusi `Recency` untuk pelanggan high-risk churn (551 pelanggan) dibuat menggunakan `seaborn.histplot`.

3. **Segmentasi Pelanggan**:
   - Segmentasi `Income` dilakukan menggunakan `pd.qcut` untuk membagi pelanggan menjadi tiga segmen: Low, Medium, dan High.
   - Segmentasi `Total Spending` juga dilakukan dengan metode yang sama.
   - Bar plot dibuat untuk membandingkan rata-rata `Income` dan `Total Spending` berdasarkan segmen menggunakan `seaborn.barplot`.

4. **Visualisasi di Tableau**:
   - Histogram `Recency` untuk pelanggan high-risk churn.
   - Bar plot rata-rata `Income` berdasarkan `Income Segment`.
   - Bar plot rata-rata `Total Spending` berdasarkan `Spending Segment`.
   - Histogram `Income` setelah penanganan outlier.
   - Semua visualisasi digabungkan dalam dashboard interaktif berjudul **"Analisis Pelanggan Supermarket: Segmentasi dan Risiko Churn"**.

---

## Hasil dan Temuan
1. **Risiko Churn**:
   - Terdapat 551 pelanggan berisiko churn tinggi dengan `Recency` di atas 74 hari.
   - Distribusi `Recency` menunjukkan bahwa sebagian besar pelanggan high-risk churn memiliki `Recency` antara 75 hingga 100 hari.

2. **Segmentasi Income**:
   - Rata-rata `Income` per segmen:
     - Low: 28,445
     - Medium: 51,557
     - High: 76,710
   - Segmen High memiliki pendapatan rata-rata tertinggi, menunjukkan potensi pelanggan premium.

3. **Segmentasi Total Spending**:
   - Rata-rata `Total Spending` per segmen:
     - Low: ~100
     - Medium: ~400
     - High: ~1300
   - Segmen High memiliki pengeluaran rata-rata tertinggi, menunjukkan pelanggan yang paling aktif berbelanja.

4. **Distribusi Income**:
   - Setelah penanganan outlier, distribusi `Income` menjadi lebih normal dengan rentang 0 hingga 100,000 dan puncak di sekitar 40,000-60,000.
  
Dashboard : (https://public.tableau.com/app/profile/naufal.maahir/viz/JCDS2804016_CapestoneProject2_Naufal/Dashboard1?publish=yes)
