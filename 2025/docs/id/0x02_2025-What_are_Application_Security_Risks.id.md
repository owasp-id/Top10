<link rel="stylesheet" href="../../assets/css/RC-stylesheet.css" />

# Apa itu Risiko Keamanan Aplikasi?
Penyerang berpotensi menggunakan berbagai jalur berbeda melalui aplikasi Anda untuk membahayakan bisnis atau organisasi Anda. Masing-masing jalur ini menimbulkan risiko potensial yang perlu diselidiki.

![Diagram kalkulasi](../assets/2025-algorithm-diagram.png)

<table>
  <tr>
   <td>
    <strong>Agen Ancaman</strong>
   </td>
   <td>
    <strong>Vektor
Serangan</strong>
   </td>
   <td>
    <strong>Eksploitabilitas</strong>
   </td>
   <td>
    <strong>Kemungkinan Kurangnya Kendali
Keamanan</strong>
   </td>
   <td>
    <strong>Dampak
Teknis</strong>
   </td>
   <td>
    <strong>Dampak
Bisnis</strong>
   </td>
  </tr>
  <tr>
   <td>
    <strong>By environment, 
dynamic by situation picture</strong>
   </td>
   <td>
    <strong>By Application  exposure (by environment</strong>
   </td>
   <td>
    <strong>Avg Weighted Exploit</strong>
   </td>
   <td>
    <strong>Missing Controls 
by average Incidence rate 
Weighed by coverage</strong>
   </td>
   <td>
    <strong>Avg Weighted Impact</strong>
   </td>
   <td>
    <strong>By Business</strong>
   </td>
  </tr>
</table>

Dalam Peringkat Risiko kami, kami telah memperhitungkan parameter universal dari eksploitasi, kemungkinan rata-rata hilangnya kontrol keamanan untuk suatu kelemahan dan dampak teknisnya.

Setiap organisasi itu unik, begitu pula pelaku ancamannya, tujuan mereka, dan dampak dari setiap pelanggaran. Jika sebuah organisasi kepentingan publik menggunakan sistem manajemen konten (CMS) untuk informasi publik dan sistem kesehatan menggunakan CMS yang sama persis untuk rekam medis sensitif, pelaku ancaman dan dampak bisnisnya bisa sangat berbeda untuk perangkat lunak yang sama. Sangat penting untuk memahami risiko bagi organisasi Anda berdasarkan paparan aplikasi, agen ancaman yang berlaku berdasarkan gambaran situasi (untuk serangan terarah dan tidak terarah berdasarkan bisnis dan lokasi), dan dampak bisnis masing-masing.


## Bagaimana data digunakan untuk memilih kategori dan memeringkatnya

Pada tahun 2017, kami memilih kategori berdasarkan tingkat insiden untuk menentukan kemungkinan, lalu memeringkatnya berdasarkan diskusi tim berdasarkan pengalaman puluhan tahun untuk Eksploitasi, Detektabilitas (juga kemungkinan), dan Dampak Teknis. Untuk tahun 2021, kami menggunakan data untuk Eksploitasi dan Dampak (Teknis) dari skor CVSSv2 dan CVSSv3 di National Vulnerability Database (NVD). Untuk tahun 2025, kami melanjutkan metodologi yang sama yang kami buat pada tahun 2021.

Kami mengunduh OWASP Dependency Check dan mengekstrak skor CVSS Exploit dan Impact yang dikelompokkan berdasarkan CWE terkait. Proses ini membutuhkan riset dan upaya yang cukup besar karena semua CVE memiliki skor CVSSv2, tetapi terdapat kekurangan pada CVSSv2 yang perlu diperbaiki oleh CVSSv3. Setelah jangka waktu tertentu, semua CVE juga akan diberi skor CVSSv3. Selain itu, rentang skor dan rumus diperbarui antara CVSSv2 dan CVSSv3.

Di CVSSv2, baik Exploit maupun (Teknis) Impact bisa mencapai 10,0, tetapi rumusnya akan menurunkannya menjadi 60% untuk Exploit dan 40% untuk Impact. Di CVSSv3, batas maksimum teoretis dibatasi hingga 6,0 untuk Exploit dan 4,0 untuk Impact. Dengan mempertimbangkan pembobotan, skor Impact meningkat, hampir satu setengah poin rata-rata di CVSSv3, dan eksploitasi turun hampir setengah poin rata-rata ketika kami melakukan analisis untuk Top Ten 2021.

Terdapat sekitar 175 ribu rekaman (naik dari 125 ribu pada tahun 2021) CVE yang dipetakan ke CWE dalam Basis Data Kerentanan Nasional (NVD), yang diekstrak dari OWASP Dependency Check. Selain itu, terdapat 643 CWE unik yang dipetakan ke CVE (naik dari 241 pada tahun 2021). Dari hampir 220 ribu CVE yang diekstrak, 160 ribu memiliki skor CVSS v2, 156 ribu memiliki skor CVSS v3, dan 6 ribu memiliki skor CVSS v4. Banyak CVE memiliki beberapa skor, sehingga totalnya lebih dari 220 ribu.

Untuk Top Ten 2025, kami menghitung skor eksploitasi dan dampak rata-rata dengan cara berikut. Kami mengelompokkan semua CVE dengan skor CVSS berdasarkan CWE dan memberi bobot pada skor eksploitasi dan dampak berdasarkan persentase populasi yang memiliki CVSSv3, serta populasi yang tersisa dengan skor CVSSv2, untuk mendapatkan rata-rata keseluruhan. Kami memetakan rata-rata ini ke CWE dalam dataset untuk digunakan sebagai skor Eksploitasi dan Dampak (Teknis) untuk separuh persamaan risiko lainnya.

Mengapa tidak menggunakan CVSS v4.0, mungkin Anda bertanya? Hal ini dikarenakan algoritma penilaiannya telah berubah secara fundamental, dan tidak lagi mudah memberikan skor Exploit atau Impact seperti yang dilakukan CVSSv2 dan CVSSv3. Kami akan mencoba mencari cara untuk menggunakan penilaian CVSS v4.0 untuk versi Top Ten mendatang, tetapi kami belum dapat menentukan cara yang tepat waktu untuk melakukannya pada edisi 2025.

Untuk tingkat insiden, kami menghitung persentase aplikasi yang rentan terhadap setiap CWE dari populasi yang diuji oleh suatu organisasi selama periode waktu tertentu. Sebagai pengingat, kami tidak mengukur frekuensi (atau seberapa sering suatu masalah muncul dalam suatu aplikasi), melainkan persentase populasi aplikasi yang ditemukan memiliki setiap CWE.

Untuk cakupan, kami melihat persentase aplikasi yang diuji oleh semua organisasi untuk CWE tertentu. Semakin tinggi cakupan yang dihitung, semakin kuat jaminan keakuratan tingkat insiden karena ukuran sampel lebih representatif terhadap populasi.

Rumus yang kami gunakan untuk iterasi ini mirip dengan tahun 2021, dengan beberapa perubahan bobot: (Tingkat Insiden Maksimum % * 1000) + (Cakupan Maksimum % * 100) + (Eksploitasi Rata-rata * 10) + (Dampak Rata-rata * 20) + (Jumlah Kejadian / 10000) = Skor Risiko

Skor yang dihitung berkisar antara 621,60 untuk kategori Kontrol Akses Rusak hingga 271,08 untuk Kesalahan Manajemen Memori.

Ini bukan sistem yang sempurna, tetapi berharga untuk menentukan peringkat kategori risiko.

Tantangan tambahan yang semakin berkembang adalah definisi "aplikasi". Seiring industri beralih ke arsitektur berbeda yang terdiri dari layanan mikro dan implementasi lain yang lebih kecil dari aplikasi tradisional, perhitungan menjadi lebih sulit. Misalnya, jika suatu organisasi menguji repositori kode, apa yang dianggapnya sebagai aplikasi? Serupa dengan perkembangan CVSSv4, edisi Top Ten berikutnya mungkin perlu menyesuaikan analisis dan penilaian untuk memperhitungkan industri yang terus berubah.

## Faktor Data

Ada faktor data yang tercantum untuk masing-masing Sepuluh Kategori Teratas, berikut artinya:

**CWE yang Dipetakan**: Jumlah CWE yang dipetakan ke suatu kategori oleh tim Sepuluh Teratas.

**Tingkat Insiden**: Tingkat insiden adalah persentase aplikasi yang rentan terhadap CWE dari populasi yang diuji oleh organisasi tersebut untuk tahun itu.

**Exploit Tertimbang**: Subskor Exploit dari skor CVSSv2 dan CVSSv3 yang ditetapkan ke CVE dipetakan ke CWE, dinormalisasi, dan ditempatkan pada skala 10 poin.

**Dampak Tertimbang**: Subskor Dampak dari skor CVSSv2 dan CVSSv3 yang ditetapkan ke CVE dipetakan ke CWE, dinormalisasi, dan ditempatkan pada skala 10 poin.

**Cakupan (Pengujian)**: Persentase aplikasi yang diuji oleh semua organisasi untuk CWE tertentu.

**Total Kejadian**: Jumlah total aplikasi yang ditemukan memiliki CWE yang dipetakan ke suatu kategori.

**Total CVE**: Jumlah total CVE dalam DB NVD yang dipetakan ke CWE yang dipetakan ke suatu kategori.

**Rumus**: (Tingkat Insiden Maksimum % * 1000) + (Cakupan Maksimum % * 100) + (Eksploitasi Rata-rata * 10) + (Dampak Rata-rata * 20) + (Jumlah Kejadian / 10000) = Skor Risiko

