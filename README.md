<a href="./README.en.md">English</a> | <b>Indonesia</b>

---

![icon](./file/icon_new.png)

![Thumbnail](./file/thumbnail.png)

# Bolatix - Aplikasi Pemesanan Tiket Sepak Bola

Bolatix adalah aplikasi Android untuk pemesanan tiket pertandingan sepak bola secara digital. Aplikasi ini dikembangkan sebagai proyek tim dalam program Studi Independen Bangkit Academy, mengombinasikan teknologi mobile, layanan cloud, dan kecerdasan buatan untuk memberikan pengalaman pemesanan tiket yang mudah, cepat, dan aman.

## Daftar Isi

- [Tentang Proyek](#tentang-proyek)
- [Fitur](#fitur)
- [Arsitektur](#arsitektur)
- [Teknologi yang Digunakan](#teknologi-yang-digunakan)
- [Tangkapan Layar](#tangkapan-layar)
- [Prasyarat](#prasyarat)
- [Instalasi](#instalasi)
- [Unduhan](#unduhan)
- [Tim Pengembang](#tim-pengembang)
- [Lisensi](#lisensi)

---

## Tentang Proyek

Bolatix hadir untuk menjawab kebutuhan penggemar sepak bola Indonesia dalam mendapatkan tiket pertandingan secara digital. Dengan fitur rekomendasi berbasis machine learning, pengguna dapat menemukan pertandingan yang relevan berdasarkan tim favorit maupun riwayat pembelian sebelumnya. Pembayaran terintegrasi dengan Midtrans sehingga mendukung berbagai metode pembayaran yang umum digunakan di Indonesia. Tiket diterbitkan dalam format PDF yang dapat diunduh dan dibagikan langsung dari aplikasi.

Proyek ini merupakan hasil kolaborasi tiga jalur keahlian: Mobile Development, Cloud Computing, dan Machine Learning dalam ekosistem Bangkit Academy.

---

## Fitur

| Fitur | Deskripsi |
|---|---|
| Autentikasi | Registrasi dan masuk menggunakan email, password, serta Google Sign-In |
| Onboarding | Tampilan pengenalan aplikasi untuk pengguna baru |
| Beranda | Menampilkan pertandingan mendatang dan rekomendasi personal |
| Rekomendasi Cerdas | Rekomendasi pertandingan berdasarkan tim favorit dan riwayat pembelian (ML) |
| Pemesanan Tiket | Pemilihan pertandingan, kelas tribun, dan gate masuk |
| Payment Gateway | Pembayaran terintegrasi dengan Midtrans (multi-metode) |
| Verifikasi Pembayaran | Konfirmasi dan verifikasi data sebelum transaksi final |
| Riwayat Pesanan | Daftar seluruh transaksi tiket yang pernah dilakukan |
| Tiket PDF | Unduh dan bagikan tiket dalam format PDF |
| Klasemen | Lihat klasemen liga terkini |
| Favorit Tim | Pilih dan simpan tim favorit untuk rekomendasi yang lebih akurat |
| Profil Pengguna | Ubah foto profil, nama, dan informasi personal |
| Notifikasi | Pemberitahuan dalam aplikasi terkait transaksi dan informasi pertandingan |
| Lupa Password | Pengiriman email reset password |
| FAQ | Pertanyaan yang umum diajukan |
| Kebijakan Privasi | Halaman kebijakan privasi dan ketentuan penggunaan |
| Tentang Kami | Informasi tim dan aplikasi |

---

## Arsitektur

Aplikasi ini menerapkan pola arsitektur **MVVM (Model-View-ViewModel)** dengan pendekatan Clean Architecture ringan, terdiri dari tiga lapisan utama:

```
app/src/main/java/com/example/bolatix/
├── data/
│   ├── firebase/        # Firebase Auth, Firestore, dan FCM helper
│   ├── models/          # Data class (User, Team, Stadium, Gate, dll.)
│   ├── remote/
│   │   ├── network/     # Retrofit service interface dan interceptor
│   │   └── response/    # Data class respons API
│   └── repository/      # AuthRepository dan FootballRepository
├── di/                  # Koin dependency injection module
├── preference/          # DataStore untuk preferensi onboarding dan user
├── ui/
│   ├── activities/      # Seluruh Activity (18 activity)
│   ├── adapters/        # RecyclerView Adapter
│   ├── components/      # Komponen UI custom
│   ├── fragments/       # Fragment (Home, Standings, Order, Profile)
│   └── viewmodels/      # ViewModel untuk setiap fitur
└── utils/               # Utility dan extension function
```

---

## Teknologi yang Digunakan

### Mobile (Android)
| Library | Versi | Kegunaan |
|---|---|---|
| Kotlin | - | Bahasa pemrograman utama |
| Android SDK | min 24 / target 34 | Platform Android |
| ViewBinding | - | Binding layout secara type-safe |
| Navigation Component | - | Navigasi antar fragment |
| Firebase Authentication | - | Autentikasi email dan Google |
| Firebase Firestore | - | Database pengguna dan notifikasi |
| Retrofit 2 | - | Komunikasi HTTP ke REST API |
| OkHttp Logging Interceptor | - | Logging dan retry request |
| Koin | - | Dependency Injection |
| Glide | - | Pemuatan gambar dari URL |
| UCrop | - | Pemotongan gambar profil |
| Midtrans SDK (UIKit) | - | Payment gateway |
| Progress Button | - | Tombol dengan animasi loading |
| ViewPager2 | - | Onboarding slide |
| DataStore Preferences | - | Penyimpanan preferensi lokal |
| Markwon Core | - | Render konten Markdown |
| Material 3 | - | Komponen UI Material Design |

### Backend
- REST API berbasis Cloud Run (Google Cloud Platform)
- Base URL: `https://bolatix-552077162382.asia-southeast2.run.app/api/`
- Repositori Backend: [BolaTix/Cloud-Computing](https://github.com/BolaTix/Cloud-Computing)

### Machine Learning
- Model rekomendasi berbasis riwayat dan preferensi tim
- Repositori ML: [BolaTix/Machine-Learning](https://github.com/BolaTix/Machine-Learning)

---

## Tangkapan Layar

<details>
  <summary>Tampilkan tangkapan layar</summary>
  <table>
    <tr>
      <td><img src="./file/screenshoot/1.png" alt="1" width="100%"></td>
      <td><img src="./file/screenshoot/2.png" alt="2" width="100%"></td>
      <td><img src="./file/screenshoot/3.png" alt="3" width="100%"></td>
      <td><img src="./file/screenshoot/4.png" alt="4" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/5.png" alt="5" width="100%"></td>
      <td><img src="./file/screenshoot/6.png" alt="6" width="100%"></td>
      <td><img src="./file/screenshoot/7.png" alt="7" width="100%"></td>
      <td><img src="./file/screenshoot/8.png" alt="8" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/9.png" alt="9" width="100%"></td>
      <td><img src="./file/screenshoot/10.png" alt="10" width="100%"></td>
      <td><img src="./file/screenshoot/11.png" alt="11" width="100%"></td>
      <td><img src="./file/screenshoot/12.png" alt="12" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/13.png" alt="13" width="100%"></td>
      <td><img src="./file/screenshoot/14.png" alt="14" width="100%"></td>
      <td><img src="./file/screenshoot/15.png" alt="15" width="100%"></td>
      <td><img src="./file/screenshoot/16.png" alt="16" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/17.png" alt="17" width="100%"></td>
      <td><img src="./file/screenshoot/18.png" alt="18" width="100%"></td>
      <td><img src="./file/screenshoot/19.png" alt="19" width="100%"></td>
      <td><img src="./file/screenshoot/20.png" alt="20" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/21.png" alt="21" width="100%"></td>
      <td><img src="./file/screenshoot/22.png" alt="22" width="100%"></td>
      <td><img src="./file/screenshoot/23.png" alt="23" width="100%"></td>
      <td><img src="./file/screenshoot/24.png" alt="24" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/25.png" alt="25" width="100%"></td>
      <td><img src="./file/screenshoot/26.png" alt="26" width="100%"></td>
      <td><img src="./file/screenshoot/27.png" alt="27" width="100%"></td>
      <td><img src="./file/screenshoot/28.png" alt="28" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/29.png" alt="29" width="100%"></td>
      <td><img src="./file/screenshoot/30.png" alt="30" width="100%"></td>
      <td><img src="./file/screenshoot/31.png" alt="31" width="100%"></td>
      <td><img src="./file/screenshoot/32.png" alt="32" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/33.png" alt="33" width="100%"></td>
      <td><img src="./file/screenshoot/34.png" alt="34" width="100%"></td>
      <td><img src="./file/screenshoot/35.png" alt="35" width="100%"></td>
      <td><img src="./file/screenshoot/36.png" alt="36" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/37.png" alt="37" width="100%"></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </table>
</details>

---

## Prasyarat

Sebelum menjalankan proyek ini, pastikan Anda telah menyiapkan:

- Android Studio Hedgehog atau yang lebih baru
- JDK 8 atau yang lebih baru
- Android SDK dengan API Level minimal 24
- Akun Firebase (untuk konfigurasi `google-services.json`)
- Akun Midtrans Sandbox (untuk konfigurasi client key)
- Koneksi internet aktif

---

## Instalasi

1. **Clone repositori**

```bash
git clone https://github.com/BolaTix/Mobile-Development.git
cd Mobile-Development
```

2. **Konfigurasi Firebase**

   - Buat proyek di [Firebase Console](https://console.firebase.google.com/)
   - Aktifkan Firebase Authentication (Email/Password dan Google Sign-In)
   - Aktifkan Cloud Firestore
   - Unduh file `google-services.json` dan tempatkan di direktori `app/`

3. **Konfigurasi Midtrans**

   Buka file `app/build.gradle.kts` dan sesuaikan nilai berikut:

   ```kotlin
   buildConfigField("String", "MERCHANT_KEY", "\"<client-key-sandbox-anda>\"")
   buildConfigField("String", "MIDTRANS_URL_CHARGE", "\"<url-charge-server-anda>\"")
   ```

4. **Buka di Android Studio**

   - Buka Android Studio, pilih `File > Open`, lalu arahkan ke folder proyek
   - Tunggu proses Gradle sync selesai

5. **Jalankan Aplikasi**

   - Sambungkan perangkat Android (API 24+) atau gunakan emulator
   - Tekan tombol `Run` di Android Studio

---

## Unduhan

| Sumber Daya | Tautan |
|---|---|
| Aplikasi Android (APK) | [Unduh BOLATIX.apk](./file/BOLATIX.apk) |
| Desain Figma | [Unduh FGMA-BOLATIX.fig](./file/FGMA-BOLATIX.fig) |
| Repositori Backend | [BolaTix/Cloud-Computing](https://github.com/BolaTix/Cloud-Computing) |
| Repositori Machine Learning | [BolaTix/Machine-Learning](https://github.com/BolaTix/Machine-Learning) |

---

## Tim Pengembang

Proyek ini dikembangkan oleh tim Mobile Development dalam program **Bangkit Academy** (Studi Independen Bersertifikat).

---

## Lisensi

Proyek ini dilisensikan di bawah **MIT License**. Lihat file [LICENSE](./LICENSE) untuk informasi selengkapnya.