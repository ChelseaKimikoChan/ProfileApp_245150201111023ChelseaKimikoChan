# Tugas Praktikum 2 - Konsep Dasar UI Jetpack Compose

## Penjelasan Singkat Kode
Aplikasi ini merupakan aplikasi profil sederhana interaktif yang dibuat menggunakan UI deklaratif dengan Jetpack Compose.
Aplikasi ini menampilkan halaman profil dimana tertera foto profil, nama, nim, deskripsi singkat, dan tombol follow interaktif. 

Layout nya menggunakan `Column` untuk menyusun komponen-komponen yang ada secara vertikal dengan parameter `horizontalAlignment = Alignment.CenterHorizontally` agar semuanya ditengah. 
Semua komponen dalam `Column` diberi `padding` sebesar 16 dp agar terdapat jarak antar komponen.

Foto profil menggunakan`Image` yang mengambil dari sumber `R.drawable.profil` yang dibentuk menjadi lingkaran menggunakan `Modifier.size(120.dp).clip(CircleShape)`. 

`Text` digunakan untuk menampilkan teks/informasi Nama (yang memiliki ukuran 20 sp dan di **bold**), NIM, dan deskripsi berupa status sebagai Mahasiswa Teknik Informatika. 

`Spacer` memberi jarak sebanyak 8 dp diantara  teks deskripsi dengan tombol dibawahnya.

Dibuat fungsi `@Composable` bernama `FollowButton()` yang menggunakan state sederhana yaitu `remember { mutableStateOf(false) }`.
Fungsi ini juga menggunakan `Button` yang ketika di klik, nilai boolean dari `isFollowed` berubah dari `True` ke `False` atau sebaliknya. 
Perubahan nilai boolean ini yang akan memicu UI untuk rebuild otomatis sehingga terdapat perubahan teks tombol dari "Follow" ke "Unfollow" atau sebaliknya.


## Analisis Singkat Keuntungan Compose Dibandingkan XML Layout
Keuntungan Compose dibandingkan XML adalah
Compose merupakan UI deklaratif sehingga programmer hanya perlu mendeklarasikan seperti apa tampilan yang diinginkan. 
Sedangkan XML adalah UI imperatif yang membutuhkan programmer untuk mendefinisikan apa yang harus dilakukan sistem langkah demi langkah.
Pada Jetpack Compose, UI juga akan berubah secara otomatis jika state berubah. 
Kode nya juga lebih ringkas, mudah dipelihara, dan konsisten dengan paradigma pemrograman modern.