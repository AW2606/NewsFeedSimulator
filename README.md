# News Feed Simulator (Kotlin Multiplatform + Compose Multiplatform)

**Nama**: Adhitya Warman  
**NIM**: 124140007  
**Mata Kuliah**: Pengembangan Aplikasi Mobile (KMP)  
**Tugas**: News Feed Simulator (Bobot 4%)

---

## Pemetaan Fitur ke Rubrik Penilaian

| Fitur / Spesifikasi Tugas | File Implementasi di KMP (`commonMain`) | Penjelasan Singkat & Konsep Kotlin | Bobot Rubrik |
|---|---|---|---|
| **1. Implementasi Flow** | [`NewsViewModel.kt`](file:///C:/Users/Adhitya\ Warman/AndroidStudioProjects/MyFirstKMPApp/shared/src/commonMain/kotlin/com/example/myfirstkmpapp/NewsViewModel.kt) | Menggunakan `flow { ... delay(2000) ... emit(...) }` (Cold Flow) untuk mensimulasikan pemancaran data berita baru secara berkala setiap 2 detik. | **25%** |
| **2. Penggunaan Operators** | [`NewsViewModel.kt`](file:///C:/Users/Adhitya\ Warman/AndroidStudioProjects/MyFirstKMPApp/shared/src/commonMain/kotlin/com/example/myfirstkmpapp/NewsViewModel.kt) | Menggunakan operator `.filter { ... }` untuk menyaring kategori berita sesuai pilihan pengguna, dan operator `.map { ... }` untuk mengubah objek `NewsItem` menjadi format string tampilan. | **20%** |
| **3. StateFlow Implementation** | [`NewsViewModel.kt`](file:///C:/Users/Adhitya\ Warman/AndroidStudioProjects/MyFirstKMPApp/shared/src/commonMain/kotlin/com/example/myfirstkmpapp/NewsViewModel.kt) | Menggunakan `MutableStateFlow` dan `StateFlow` (`readCount`) untuk menyimpan dan memancarkan jumlah berita yang telah dibaca secara reaktif ke UI menggunakan `collectAsState()`. | **20%** |
| **4. Coroutines Usage** | [`NewsViewModel.kt`](file:///C:/Users/Adhitya\ Warman/AndroidStudioProjects/MyFirstKMPApp/shared/src/commonMain/kotlin/com/example/myfirstkmpapp/NewsViewModel.kt) & [`App.kt`](file:///C:/Users/Adhitya\ Warman/AndroidStudioProjects/MyFirstKMPApp/shared/src/commonMain/kotlin/com/example/myfirstkmpapp/App.kt) | Menggunakan `suspend fun fetchNewsDetail(...)` dengan `withContext(Dispatchers.Default)` dan `delay(1000)` serta `coroutineScope.launch` untuk mengambil detail berita secara asynchronous saat item diklik. | **20%** |
| **5. Kode & Dokumentasi** | Seluruh kode di `commonMain` | Ditulis dengan prinsip clean code, struktur modular di `commonMain` (berjalan di Android & Desktop/iOS), serta dilengkapi komentar KDoc dan penjelasan Bahasa Indonesia di setiap bagian penting. | **15%** |

---

## Cara Menjalankan Project

1. **Melalui Android Studio**:
   - Buka project `MyFirstKMPApp` di Android Studio.
   - Pilih konfigurasi run `androidApp` untuk menjalankan aplikasi di Emulator Android atau Perangkat Fisik.
   - Klik tombol **Run (Shift + F10)**.

2. **Melalui Terminal (Gradle CLI)**:
   - Buka terminal di direktori root project (`C:\Users\Adhitya Warman\AndroidStudioProjects\MyFirstKMPApp`).
   - Untuk menjalankan aplikasi Android:
     ```bash
     ./gradlew :androidApp:assembleDebug
     ```
   - Untuk menjalankan Desktop/JVM (jika dikonfigurasi):
     ```bash
     ./gradlew run
     ```
