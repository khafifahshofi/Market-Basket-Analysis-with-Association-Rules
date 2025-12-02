Association Rules Berdasarkan Musim dengan Market Basket Analysis

Proyek ini menganalisis pola pembelian konsumen berdasarkan musim menggunakan algoritma Apriori. Dataset transaksi dipecah menjadi empat periode: Winter, Spring, Summer, dan Autumn untuk melihat apakah terdapat perbedaan pola pembelian pada setiap musim. Analisis ini digunakan untuk mengidentifikasi produk yang sering dibeli bersama dalam masing-masing musim.

1. Deskripsi Proyek : Market Basket Analysis digunakan untuk menemukan kombinasi produk yang sering muncul dalam satu transaksi. Pada proyek ini, analisis tidak dilakukan secara keseluruhan, melainkan dibagi berdasarkan musim agar pola pembelian lebih tersegmentasi dan relevan.

  - Empat set basket transaksi dibuat:

  - Winter

  - Spring
  
  - Summer

  - Autumn

Setiap musim diproses menggunakan:

  - Pembersihan data

  - Segmentasi transaksi berdasarkan musim

  - Pembentukan basket (one-hot encoding)

  - Frequent itemsets (Apriori)

  - Association rules

  - Identifikasi rules dengan lift tertinggi

  - Perbandingan pola antar musim

2. Dataset : Dataset yang digunakan adalah Online Retail Dataset dari Kaggle, memuat transaksi e-commerce Inggris tahun 2010–2011. Variabel yang digunakan dalam proses segmentasi musim:

  a. InvoiceDate → digunakan untuk menentukan musim berdasarkan bulan transaksi.

  b. Pembagian musim: 
    - Winter: Desember, Januari, Februari

    - Spring: Maret, April, Mei

    - Summer: Juni, Juli, Agustus

    - Autumn: September, Oktober, November

3. Alur Analisis: Membersihkan data dengan menghapus transaksi duplikat, quantity negatif, dan deskripsi kosong Menambahkan kolom Season berdasarkan bulan transaksi

    a. Memisahkan dataset menjadi empat subset musim

    b. Mengelompokkan item berdasarkan invoice dan mengubahnya ke one-hot encoding

    c. Menggunakan Apriori untuk mendapatkan frequent itemsets di setiap musim

    d. Membuat association rules (support, confidence, lift)

    e. Menyeleksi rules terbaik berdasarkan lift tertinggi untuk masing-masing musim

    f. Menyimpulkan perbedaan pola pembelian antar musim

4. Teknologi yang Digunakan : Python, Pandas, mlxtend (TransactionEncoder, Apriori, Association Rules), Google Colab

5. Hasil Utama : Hasil analisis menunjukkan bahwa setiap musim memiliki karakteristik pembelian yang berbeda. Item yang termasuk dalam satu seri, warna, atau tema tertentu cenderung terbeli bersama.

    Ringkasan temuan:

    Winter: Pola belanja lebih stabil dan cenderung menunjukkan pembelian set produk dekoratif.

    Spring: Produk bertema cerah dan dekoratif lebih sering muncul bersama.

    Summer: Pembelian cenderung terfragmentasi, rule lebih sedikit.

    Autumn: Pola mirip winter, dengan kombinasi produk rumah tangga dan dekoratif.




