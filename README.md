# Indonesia Coffee Chain Wars 2026

Analisis komersial jaringan kedai kopi di Indonesia berbasis notebook Python. Proyek ini mengevaluasi kinerja merek, ekonomi diskon, format gerai, pelanggan, kompetisi, profitabilitas, dan risiko ekspansi.

> **Kesimpulan utama:** diskon membeli volume, tetapi mengorbankan profit. Ekonomi gerai lebih banyak dibedakan oleh kedalaman diskon, format gerai, jenis biji, dan loyalitas pelanggan daripada oleh kota atau segmen pelanggan.

## Ringkasan analisis

- **Data:** 13.000 observasi gerai, 26 kolom, 5 merek, 16 kota/area, dan 5 format gerai.
- **Kualitas data:** tidak ditemukan missing value atau duplikat. Namun beberapa metrik turunan sangat mudah direkonstruksi dari kolom mentah, sehingga data kemungkinan sintetis.
- **Ekonomi diskon:** dibandingkan gerai dengan diskon <=10%, gerai dengan diskon >40% memiliki cups sekitar **58% lebih tinggi**, tetapi revenue **33% lebih rendah**, margin turun **18 poin persentase**, dan profit proxy turun **64%**.
- **Pendorong margin:** diskon, format gerai, dan jenis biji menjelaskan hampir seluruh variasi margin dalam data. Kota menjelaskan kurang dari 1% variasi profit proxy.
- **Volume trap:** sekitar **26,5% gerai** menghasilkan **33,1% revenue**, tetapi hanya **28,2% profit proxy**, dengan margin sekitar 25%. Risiko ini terkonsentrasi pada format Mall Kiosk/Office Lobby dan terutama Fore Coffee.
- **Merek:** Tomoro Coffee memimpin volume, tetapi memiliki profit proxy per gerai terendah. Kopi Kenangan memimpin profit proxy per gerai.
- **Pelanggan:** tier loyalitas lebih informatif daripada segmen pelanggan. Die-Hard memiliki diskon rata-rata sekitar 9,8% dan margin 36,5%, sedangkan Promo-Chaser memiliki diskon 38,6% dan margin 24,0%.
- **Switching:** pemicu terbesar adalah pengalaman (40,6%) dan harga (30,5%); promosi hanya 7,7%.
- **Geografi dan segmentasi:** perbedaan antar-kota kecil, sementara segmentasi klaster berstruktur lemah (silhouette sekitar 0,23). Keduanya tidak boleh digunakan sebagai satu-satunya dasar keputusan ekspansi.

## Rekomendasi manajemen

1. Ganti diskon massal dengan promosi tertarget dan validasi melalui eksperimen A/B per merek atau wilayah.
2. Turunkan diskon Tomoro secara bertahap sambil memperbaiki antrean, pickup, dan loyalitas non-diskon.
3. Prioritaskan screening ekspansi berdasarkan format dan disiplin diskon: Ruko, Office Lobby, dan Drive-Thru perlu diprioritaskan; ekonomi Mall Kiosk perlu ditinjau ulang.
4. Untuk Fore Coffee, fokuskan perbaikan pada harga dan bauran produk/biaya biji, bukan sekadar mengurangi diskon.
5. Bangun loyalitas melalui konsistensi rasa, kecepatan layanan, dan kenyamanan, bukan ketergantungan pada voucher.
6. Kumpulkan data biaya, penjualan aktual, dan histori waktu sebelum mengambil keputusan investasi besar.

## Batasan penting

Temuan ini bersifat **asosiatif, bukan kausal**. Margin adalah estimasi dan profit proxy dihitung sebagai revenue x margin, bukan laba akuntansi. Dataset tidak memiliki dimensi waktu dan tidak menyediakan biaya sewa, COGS, kapasitas, kualitas lokasi, harga kompetitor aktual, atau penjualan antar-gerai untuk mengukur kanibalisasi secara nyata. Karena beberapa variabel tampak sintetis atau merupakan turunan mekanis, hasil harus diperlakukan sebagai struktur ekonomi dalam dataset, bukan bukti langsung perilaku pasar riil.

## Isi repositori

- [`Indonesia_Coffee_Chain_Wars_2026_Analytics.ipynb`](./Indonesia_Coffee_Chain_Wars_2026_Analytics.ipynb) — notebook lengkap dari audit kualitas data sampai rekomendasi strategis dan audit angka executive summary.
- `indonesia_coffee_chain_wars_enriched_2026.csv` — dataset yang dibutuhkan notebook, tidak termasuk dalam repositori ini.

## Menjalankan notebook

1. Sediakan file `indonesia_coffee_chain_wars_enriched_2026.csv` di direktori proyek atau folder `data/`.
2. Buka notebook dengan Jupyter Notebook, JupyterLab, atau Google Colab.
3. Jalankan seluruh cell secara berurutan.

Notebook menggunakan Python dengan pandas, NumPy, SciPy, statsmodels, scikit-learn, matplotlib, seaborn, dan IPython.
