# Perkenalan

![Logo OWASP](../../assets/TOP_10_logo_Final_Logo_Colour.png)

Selamat datang di edisi ke-8 OWASP Top Ten!

Terima kasih banyak kepada semua orang yang telah menyumbangkan data dan
perspektif dalam survei ini. Tanpa Anda, terbitan ini tidak akan mungkin
terwujud. **TERIMA KASIH!**

## Memperkenalkan OWASP Top 10:2025

- [A01:2025 - Kontrol Akses Rusak](A01_2025-Broken_Access_Control.id.md)
- [A02:2025 - Kesalahan Konfigurasi Keamanan](A02_2025-Security_Misconfiguration.id.md)
- [A03:2025 - Kegagalan Rantai Pasokan Perangkat Lunak](A03_2025-Software_Supply_Chain_Failures.id.md)
- [A04:2025 - Kegagalan Kriptografi](A04_2025-Cryptographic_Failures.id.md)
- [A05:2025 - Injeksi](A05_2025-Injection.id.md)
- [A06:2025 - Desain yang Tidak Aman](A06_2025-Insecure_Design.id.md)
- [A07:2025 - Kegagalan Autentikasi](A07_2025-Authentication_Failures.id.md)
- [A08:2025 - Kegagalan Integritas Data atau Perangkat Lunak](A08_2025-Software_or_Data_Integrity_Failures.id.md)
- [A09:2025 - Kegagalan Pencatatan Log & Peringatan](A09_2025-Logging_and_Alerting_Failures.id.md)
- [A10:2025 - Penanganan Kondisi Luar Biasa yang Salah](A10_2025-Mishandling_of_Exceptional_Conditions.id.md)

## Apa yang berubah di Top 10 untuk tahun 2025

Terdapat dua kategori baru dan satu konsolidasi dalam Top Ten untuk
tahun 2025. Kami telah berupaya sebisa mungkin untuk tetap berfokus pada
akar permasalahan, alih-alih pada gejalanya. Dengan kompleksitas
rekayasa perangkat lunak dan keamanan perangkat lunak, pada dasarnya
mustahil untuk membuat sepuluh kategori tanpa adanya tumpang tindih.

![Pemetaan](../../assets/2025-mappings.png)

- [**A01:2025 -- Kontrol Akses Rusak**](A01_2025-Broken_Access_Control.id.md)
  mempertahankan posisinya
  di peringkat #1 sebagai risiko keamanan aplikasi paling serius; data
  yang disumbangkan menunjukkan bahwa rata-rata, 3,73% aplikasi yang
  diuji memiliki satu atau lebih dari 40 Common Weakness Enumerations
  (CWE) dalam kategori ini. Sebagaimana ditunjukkan oleh garis
  putus-putus pada gambar di atas, Server-Side Request Forgery (SSRF)
  telah dimasukkan ke dalam kategori ini.
- [**A02:2025 - Kesalahan Konfigurasi Keamanan**](A02_2025-Security_Misconfiguration.id.md) 
  naik dari #5 pada
  tahun 2021 menjadi #2 pada tahun 2025. Kesalahan konfigurasi lebih
  umum dalam data untuk siklus ini. 3,00% aplikasi yang diuji memiliki
  satu atau lebih dari 16 CWE dalam kategori ini. Hal ini tidak
  mengherankan, karena rekayasa perangkat lunak terus meningkatkan
  jumlah perilaku aplikasi yang didasarkan pada konfigurasi.
- [**A03:2025 - Kegagalan Rantai Pasokan Perangkat Lunak**](A03_2025-Software_Supply_Chain_Failures.id.md) 
  merupakan perluasan dari [A06:2021 - Komponen Rentan dan Kedaluwarsa](https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/)
  untuk menyertakan cakupan kompromi yang lebih luas yang terjadi di
  dalam atau di seluruh ekosistem dependensi perangkat lunak, sistem
  pengembangan, dan infrastruktur distribusi. Kategori ini dipilih
  secara mayoritas sebagai perhatian utama dalam survei komunitas.
  Kategori ini memiliki 5 CWE dan kehadiran yang terbatas dalam data
  yang dikumpulkan, tetapi kami yakin hal ini disebabkan oleh tantangan
  dalam pengujian dan berharap pengujian dapat mengejar ketertinggalan
  di area ini. Kategori ini memiliki kejadian paling sedikit dalam data,
  tetapi juga memiliki skor eksploitasi dan dampak rata-rata tertinggi
  dari CVE.
- [**A04:2025 - Kegagalan Kriptografi**](A04_2025-Cryptographic_Failures.id.md) 
  turun dua peringkat
  dari #2 ke #4 dalam peringkat. Data yang disumbangkan menunjukkan
  bahwa, rata-rata, 3,80% aplikasi memiliki satu atau lebih dari 32 CWE
  dalam kategori ini. Kategori ini sering menyebabkan paparan data
  sensitif atau kompromi sistem.
- [**A05:2025 - Injeksi**](A05_2025-Injection.id.md) turun dua tingkat dari
  #3 ke #5 dalam peringkat, mempertahankan posisinya relatif terhadap
  Kegagalan Kriptografi dan Desain Tidak Aman. Injeksi adalah salah satu
  kategori yang paling banyak diuji, dengan jumlah CVE terbanyak terkait
  dengan 38 CWE dalam kategori ini. Injeksi mencakup berbagai masalah
  mulai dari kerentanan Cross-site Scripting (frekuensi tinggi/dampak
  rendah) hingga Injeksi SQL (frekuensi rendah/dampak tinggi).
- [**A06:2025 - Desain yang Tidak Aman**](A06_2025-Insecure_Design.id.md)
  turun dua tingkat dari #4 ke #6 karena Kesalahan Konfigurasi Keamanan
  dan Kegagalan Rantai Pasokan Perangkat Lunak melampauinya. Kategori
  ini diperkenalkan pada tahun 2021, dan kami telah melihat peningkatan
  yang signifikan dalam industri terkait pemodelan ancaman dan penekanan
  yang lebih besar pada desain yang aman.
- [**A07:2025 - Kegagalan
  Autentikasi**](A07_2025-Authentication_Failures.id.md) mempertahankan
  posisinya di #7 dengan sedikit perubahan nama (sebelumnya \"
  [Kegagalan Identifikasi dan Autentikasi](https://owasp.org/Top10/A07_2021-Identification_and_Authentication_Failures/)
  \") agar lebih akurat mencerminkan 36 CWE dalam kategori ini. Kategori
  ini tetap penting, tetapi peningkatan penggunaan kerangka kerja
  standar untuk autentikasi tampaknya memberikan dampak positif terhadap
  kejadian kegagalan autentikasi.
- [**A08:2025 - Kegagalan Integritas Data atau Perangkat Lunak**](A08_2025-Software_or_Data_Integrity_Failures.id.md) 
  masih berada
  di peringkat ke-8. Kategori ini berfokus pada kegagalan dalam menjaga
  batas kepercayaan dan memverifikasi integritas perangkat lunak, kode,
  dan artefak data pada tingkat yang lebih rendah daripada Kegagalan
  Rantai Pasokan Perangkat Lunak.
- [**A09:2025 - Kegagalan Pencatatan Log & Peringatan**](A09_2025-Logging_and_Alerting_Failures.id.md)
  mempertahankan posisinya di #9. Kategori ini mengalami sedikit
  perubahan nama (sebelumnya [Kegagalan Pencatatan dan Pemantauan Keamanan](https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures/)
  ) untuk menekankan pentingnya fungsi peringatan yang diperlukan untuk
  mendorong tindakan yang tepat pada peristiwa pencatatan yang relevan.
  Pencatatan yang baik tanpa peringatan hanya memiliki nilai minimal
  dalam mengidentifikasi insiden keamanan. Kategori ini akan selalu
  kurang terwakili dalam data, dan kembali dipilih dalam daftar oleh
  peserta survei komunitas.
- [**A10:2025 - Penanganan Kondisi Luar Biasa yang Tidak Tepat**](A10_2025-Mishandling_of_Exceptional_Conditions.id.md) 
  adalah
  kategori baru untuk tahun 2025. Kategori ini berisi 24 CWE yang
  berfokus pada penanganan kesalahan yang tidak tepat, kesalahan logika,
  kegagalan buka, dan skenario terkait lainnya yang berasal dari kondisi
  abnormal yang mungkin dialami sistem.

## Metodologi

Terbitan Top Ten ini tetap terinformasi data, tetapi tidak membuta
berbasis data. Kami memeringkat 12 kategori berdasarkan data yang
disumbangkan, dan mengizinkan dua kategori untuk dipromosikan atau
disorot oleh respons dari survei komunitas. Kami melakukan ini karena
alasan mendasar: memeriksa data yang disumbangkan pada dasarnya adalah
melihat ke masa lalu. Para peneliti Keamanan Aplikasi mendedikasikan
waktu untuk mengidentifikasi kerentanan baru dan mengembangkan metode
pengujian baru. Diperlukan waktu berminggu-minggu hingga bertahun-tahun
untuk mengintegrasikan pengujian ini ke dalam perangkat dan proses. Saat
kita dapat menguji kelemahan secara andal dalam skala besar, mungkin
sudah bertahun-tahun berlalu. Ada juga risiko penting yang mungkin tidak
akan pernah dapat kita uji secara andal dan hadir dalam data. Untuk
menyeimbangkan pandangan tersebut, kami menggunakan survei komunitas
untuk bertanya kepada para praktisi keamanan dan pengembangan aplikasi
di garis depan tentang risiko penting apa yang mereka lihat yang mungkin
kurang terwakili dalam data pengujian.

## Bagaimana kategori-kategori tersebut disusun

Beberapa kategori telah berubah dari edisi OWASP Top Ten sebelumnya.
Berikut ringkasan singkat perubahan kategori tersebut.

Dalam iterasi ini, kami meminta data, tanpa batasan CWE seperti yang
kami lakukan untuk edisi 2021. Kami meminta jumlah aplikasi yang diuji
untuk tahun tertentu (mulai tahun 2021), dan jumlah aplikasi dengan
setidaknya satu contoh CWE yang ditemukan dalam pengujian. Format ini
memungkinkan kami melacak seberapa prevalen setiap CWE dalam populasi
aplikasi. Kami mengabaikan frekuensi untuk tujuan kami; meskipun mungkin
diperlukan untuk situasi lain, frekuensi hanya menyembunyikan prevalensi
aktual dalam populasi aplikasi. Apakah suatu aplikasi memiliki empat
contoh CWE atau 4.000 contoh tidak termasuk dalam perhitungan Top Ten.
Terutama karena penguji manual cenderung hanya mencantumkan kerentanan
satu kali, terlepas dari berapa kali kerentanan tersebut diulang dalam
aplikasi, sementara kerangka kerja pengujian otomatis mencantumkan
setiap contoh kerentanan sebagai unik. Kami beralih dari sekitar 30 CWE
pada tahun 2017, menjadi hampir 400 CWE pada tahun 2021, menjadi 589 CWE
dalam edisi ini untuk dianalisis dalam kumpulan data. Kami berencana
melakukan analisis data tambahan sebagai pelengkap di masa mendatang.
Peningkatan jumlah CWE yang signifikan ini mengharuskan perubahan dalam
struktur kategori.

Kami menghabiskan beberapa bulan mengelompokkan dan mengkategorikan CWE
dan bisa saja melanjutkannya selama beberapa bulan lagi. Kami terpaksa
berhenti di suatu titik. Terdapat jenis CWE yang bersifat akar penyebab
dan gejala, di mana jenis akar penyebab seperti \"Kegagalan
Kriptografi\" dan \"Kesalahan Konfigurasi\" berbeda dengan jenis gejala
seperti \"Pemaparan Data Sensitif\" dan \"Penolakan Layanan\". Kami
memutuskan untuk berfokus pada akar penyebab sebisa mungkin karena lebih
logis untuk memberikan panduan identifikasi dan perbaikan. Berfokus pada
akar penyebab daripada gejala bukanlah konsep baru; Top Ten merupakan
gabungan antara gejala dan akar penyebab. CWE juga merupakan gabungan
antara gejala dan akar penyebab; kami hanya lebih berhati-hati dalam
menyebutkannya. Rata-rata terdapat 25 CWE per kategori dalam edisi ini,
dengan batas bawah 5 CWE untuk A02:2025 Kegagalan Rantai Pasokan
Perangkat Lunak dan A09:2025 Kegagalan Pencatatan Log dan Peringatan
hingga 40 CWE untuk A01:2025 Kontrol Akses Rusak. Kami memutuskan untuk
membatasi jumlah CWE dalam satu kategori menjadi 40. Struktur kategori
yang diperbarui ini menawarkan manfaat pelatihan tambahan karena
perusahaan dapat berfokus pada CWE yang sesuai untuk suatu
bahasa/kerangka kerja.

Kami telah ditanya mengapa tidak beralih ke daftar 10 CWE sebagai Top
10, mirip dengan MITRE Top 25 Most Dangerous Software Weaknesses. Ada
dua alasan utama mengapa kami menggunakan beberapa CWE dalam kategori.
Pertama, tidak semua CWE ada dalam semua bahasa pemrograman atau
kerangka kerja. Hal ini menyebabkan masalah untuk program perkakas dan
pelatihan/kesadaran karena bagian dari Top Ten mungkin tidak berlaku.
Alasan kedua adalah bahwa ada beberapa CWE untuk kerentanan umum.
Misalnya, ada beberapa CWE untuk Injeksi umum, Injeksi Perintah, Skrip
Lintas Situs, Kata Sandi Hardcoded, Kurangnya Validasi, Buffer Overflow,
Penyimpanan Teks Polos atas Informasi Sensitif, dan banyak lainnya.
Bergantung pada organisasi atau penguji, CWE yang berbeda dapat
digunakan. Dengan menggunakan kategori dengan beberapa CWE, kami dapat
membantu meningkatkan dasar dan kesadaran akan berbagai jenis kelemahan
yang mungkin terjadi di bawah nama kategori umum. Dalam edisi Top Ten
2025 ini, terdapat 248 CWE dalam 10 kategori. Total terdapat 968 CWE
dalam [kamus yang dapat diunduh dari MITRE](https://cwe.mitre.org) pada
saat rilis ini.

## Bagaimana data digunakan untuk memilih kategori

Mirip dengan yang kami lakukan untuk edisi 2021, kami memanfaatkan data
CVE untuk *Exploitability* dan *(Technical) Impact* . Kami mengunduh
OWASP Dependency Check dan mengekstrak skor CVSS Exploit dan Impact,
mengelompokkannya berdasarkan CWE relevan yang tercantum dalam CVE.
Proses ini membutuhkan riset dan upaya yang cukup besar, karena semua
CVE memiliki skor CVSSv2, tetapi terdapat kekurangan pada CVSSv2 yang
perlu diperbaiki oleh CVSSv3. Setelah jangka waktu tertentu, semua CVE
juga akan diberi skor CVSSv3. Selain itu, rentang skor dan rumus
diperbarui antara CVSSv2 dan CVSSv3.

Di CVSSv2, baik Eksploitasi maupun Dampak (Teknis) bisa mencapai 10,0,
tetapi rumusnya akan menurunkannya menjadi 60% untuk Eksploitasi dan 40%
untuk Dampak. Di CVSSv3, batas maksimum teoretis dibatasi hingga 6,0
untuk Eksploitasi dan 4,0 untuk Dampak. Dengan mempertimbangkan
pembobotan, skor Dampak bergeser lebih tinggi, hampir satu setengah poin
rata-rata di CVSSv3, dan eksploitasi bergeser hampir setengah poin lebih
rendah secara rata-rata.

Terdapat sekitar 175 ribu rekaman (naik dari 125 ribu pada tahun 2021)
CVE yang dipetakan ke CWE dalam Basis Data Kerentanan Nasional (NVD),
yang diekstrak dari OWASP Dependency Check. Selain itu, terdapat 643 CWE
unik yang dipetakan ke CVE (naik dari 241 pada tahun 2021). Dari hampir
220 ribu CVE yang diekstrak, 160 ribu memiliki skor CVSS v2, 156 ribu
memiliki skor CVSS v3, dan 6 ribu memiliki skor CVSS v4. Banyak CVE
memiliki beberapa skor, sehingga totalnya lebih dari 220 ribu.

Untuk Top Ten 2025, kami menghitung skor eksploitasi dan dampak
rata-rata dengan cara berikut. Kami mengelompokkan semua CVE dengan skor
CVSS berdasarkan CWE dan memberi bobot pada skor eksploitasi dan dampak
berdasarkan persentase populasi yang memiliki CVSSv3, serta populasi
yang tersisa dengan skor CVSSv2, untuk mendapatkan rata-rata
keseluruhan. Kami memetakan rata-rata ini ke CWE dalam dataset untuk
digunakan sebagai skor Eksploitasi dan Dampak (Teknis) untuk separuh
persamaan risiko lainnya.

Mengapa tidak menggunakan CVSS v4.0, mungkin Anda bertanya? Hal ini
dikarenakan algoritma penilaiannya telah berubah secara fundamental, dan
tidak lagi mudah memberikan skor *Exploit* atau *Impact* seperti yang
dilakukan CVSS v2 dan CVSS v3. Kami akan mencoba mencari cara untuk
menggunakan penilaian CVSS v4.0 untuk versi Top Ten mendatang, tetapi
kami belum dapat menentukan cara yang tepat waktu untuk melakukannya
pada edisi 2025.

## Mengapa kami menggunakan survei komunitas

Hasil dalam data sebagian besar terbatas pada apa yang dapat diuji
industri secara otomatis. Bicaralah dengan profesional AppSec yang
berpengalaman, dan mereka akan memberi tahu Anda tentang hal-hal yang
mereka temukan dan tren yang mereka lihat yang belum ada dalam data.
Dibutuhkan waktu bagi orang untuk mengembangkan metodologi pengujian
untuk jenis kerentanan tertentu, dan kemudian lebih banyak waktu lagi
agar pengujian tersebut dapat diotomatisasi dan dijalankan pada sejumlah
besar aplikasi. Semua yang kami temukan adalah melihat kembali ke masa
lalu dan mungkin melewatkan tren dari tahun lalu, yang tidak ada dalam
data.

Oleh karena itu, kami hanya memilih delapan dari sepuluh kategori dari
data tersebut karena datanya tidak lengkap. Dua kategori lainnya berasal
dari survei komunitas Top 10. Hal ini memungkinkan para praktisi di
garis depan untuk memilih apa yang mereka anggap sebagai risiko
tertinggi yang mungkin tidak ada dalam data (dan mungkin tidak pernah
diungkapkan dalam data).

## Terima kasih kepada kontributor data kami

Organisasi-organisasi berikut (bersama beberapa donatur anonim) dengan
baik hati menyumbangkan data untuk lebih dari 2,8 juta aplikasi sehingga
menjadikannya kumpulan data keamanan aplikasi terbesar dan terlengkap.
Tanpa Anda, hal ini mustahil terwujud.

- Accenture (Praha)
- Anonim (beberapa)
- Bugcrowd
- Contrast Security
- CryptoNet Lab
- Layanan SoftTech Intuitor
- Orca Security
- Probley
- Semgrep
- Sonar
- USD AG
- Veracode
- Wallarm

## Penulis Utama

- Andrew van der Stock - X: [\@vanderaj](https://x.com/vanderaj)
- Brian Glas - X: [\@infosecdad](https://x.com/infosecdad)
- Neil Smithline - X: [\@appsecneil](https://x.com/appsecneil)
- Tanya Janca - X: [\@shehackspurple](https://x.com/shehackspurple)
- Torsten Gigler - Mastodon: [\@torsten_gigler
  \@infosec.exchange](https://infosec.exchange/@torsten_gigler)

## Kandidat Rilis

Kandidat rilis ini awalnya dirilis pada 6 November 2025.

## Mencatat masalah dan permintaan pull

Harap catat segala koreksi atau masalah:

### Tautan proyek:

- [Beranda](https://owasp.org/www-project-top-ten/)
- [Repositori GitHub](https://github.com/OWASP/Top10)
