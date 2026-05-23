# 🍅 Pomodoro Timer + Virtual Pet — Prompt Engineering Guide

Panduan iteratif untuk membangun aplikasi **Pomodoro Timer** dengan fitur **Virtual Pet** menggunakan pendekatan prompt-driven development. Setiap iterasi memperkenalkan konsep baru secara bertahap.

---

## 🗂️ Overview Iterasi

| Iterasi | Fokus | Konsep Utama |
|---------|-------|--------------|
| 1 | Fondasi UI & Timer | HTML/CSS/JS, Dark Mode, Responsive Design |
| 2 | Virtual Pet & State | State Management, EXP System, Mood Logic |
| 3 | Anti-Selingkuh | Page Visibility API, Edge Cases, Event Handling |
| 4 | Persistensi & Evolusi | localStorage, Data Persistence, Visual Evolution |

---

## 🏗️ Iterasi 1 — Fondasi UI & Timer

**Tujuan:** Membangun kerangka dasar aplikasi dengan timer fungsional dan desain yang menarik.

### 🇮🇩 Bahasa Indonesia

> Buatkan sebuah file `index.html` tunggal yang berisi aplikasi web Pomodoro Timer. Desainnya harus modern, minimalis, dan sepenuhnya responsif. Gunakan tema warna dark mode dengan aksen neon (seperti ungu atau hijau). Halaman ini harus mencakup:
>
> 1. Countdown timer untuk sesi fokus (25 menit) dan sesi istirahat (5 menit).
> 2. Tombol `Start`, `Pause`, dan `Reset`.
> 3. Sebuah area kosong di tengah halaman untuk `Virtual Pet` yang akan kita implementasikan di langkah berikutnya.
>
> Gabungkan semua HTML, CSS, dan JavaScript ke dalam satu file agar mudah langsung dijalankan.

### 🇬🇧 English

> Create a single `index.html` file containing a Pomodoro Timer web application. The design should be modern, minimalist, and fully responsive. Use a dark mode color theme with neon accents (like purple or green). The page must include:
>
> 1. A countdown timer for focus sessions (25 minutes) and break sessions (5 minutes).
> 2. `Start`, `Pause`, and `Reset` buttons.
> 3. A designated empty space in the center for a `Virtual Pet` that we will implement in the next step.
>
> Please combine all HTML, CSS, and JavaScript into this single file so it's easy to run immediately.

---

## 🐾 Iterasi 2 — Memasukkan Logika "Virtual Pet" (State Management)

**Tujuan:** Memaksa mahasiswa mengatur status (state) peliharaan yang terikat dengan jalannya timer.

### 🇮🇩 Bahasa Indonesia

> Sekarang, mari kita tambahkan karakter Peliharaan Virtual (Virtual Pet) di area kosong tadi menggunakan elemen teks/emoji atau CSS murni. Pet ini punya status: **Level**, **EXP**, dan **Mood**. Tolong update kode JavaScript-nya dengan aturan berikut:
>
> 1. Saat timer fokus berjalan, Pet akan berstatus `Belajar` (misal emoji 📝 atau animasi membaca).
> 2. Jika user berhasil menyelesaikan 25 menit fokus tanpa menekan `Pause`, Pet mendapat **+20 EXP**. Jika EXP mencapai 100, Pet **naik Level**.
> 3. **JIKA** user menekan tombol `Pause` atau `Reset` sebelum 25 menit selesai, Mood si Pet akan berubah menjadi `Sedih/Kecewa` (misal emoji 😢) dan **EXP berkurang 10**.
>
> Perbarui kode dari file sebelumnya tanpa merusak fungsi timer yang sudah berjalan.

### 🇬🇧 English

> Now, let's add a Virtual Pet character into the designated space using text/emojis or pure CSS shapes. This pet has states: **Level**, **EXP**, and **Mood**. Update the JavaScript code with these rules:
>
> 1. When the focus timer is running, the pet's status changes to `Studying` (e.g., using a 📝 emoji or a reading animation).
> 2. If the user successfully completes the 25-minute focus session without hitting `Pause`, the pet gains **+20 EXP**. When EXP reaches 100, the pet **Levels Up**.
> 3. **IF** the user clicks `Pause` or `Reset` before the 25 minutes are up, the pet's Mood changes to `Sad` (e.g., 😢 emoji) and it **loses 10 EXP**.
>
> Update the previous code without breaking the existing timer functionality.

---

## 🔒 Iterasi 3 — Menambahkan Fitur "Anti-Selingkuh" (Edge Cases & Page Visibility API)

**Tujuan:** Mengajarkan cara menangani celah (exploit) pada aplikasi ketika user membuka tab lain saat belajar.

### 🇮🇩 Bahasa Indonesia

> Aplikasi ini punya celah: user bisa saja membiarkan timer berjalan lalu membuka tab lain untuk main media sosial. Saya ingin menambahkan fitur keamanan menggunakan **Page Visibility API** di JavaScript:
>
> 1. Jika user berpindah ke tab lain atau meminimalkan browser saat timer fokus aktif, otomatis timer akan **ter-pause**.
> 2. Saat hal itu terjadi, buat sebuah **pop-up atau notifikasi** di layar yang bertuliskan: *"Pet kamu menangis karena kamu tinggal selingkuh!"*
> 3. Ubah status Pet menjadi `Marah` (misal emoji 😡) dan **kurangi HP atau EXP-nya secara drastis**.
>
> Bimbing saya bagaimana cara mengintegrasikan logika deteksi tab ini ke dalam kode yang sudah ada.

### 🇬🇧 English

> There is a loophole in this app: users can leave the timer running while opening another tab to browse social media. I want to add a security feature using the JavaScript **Page Visibility API**:
>
> 1. If the user switches tabs or minimizes the browser while the focus timer is active, automatically **pause the timer**.
> 2. When this happens, display a **pop-up or on-screen notification** saying: *"Your pet is crying because you abandoned them!"*
> 3. Change the pet's status to `Angry` (e.g., 😡 emoji) and **drastically reduce its HP or EXP**.
>
> Guide me on how to integrate this tab-detection logic into our current code.

---

## 💾 Iterasi 4 — Implementasi Evolusi & Local Storage (Penyimpanan Data)

**Tujuan:** Mengunci kemampuan aplikasi agar data tidak hilang saat halaman di-refresh, serta menambahkan fitur perubahan visual yang kompleks.

### 🇮🇩 Bahasa Indonesia

> Tahap terakhir, saya ingin progress dari user tidak hilang saat halaman di-refresh.
>
> 1. Gunakan **localStorage** untuk menyimpan Level, EXP, dan Mood si Pet secara otomatis setiap ada perubahan. Saat halaman pertama kali dibuka, muat data tersebut.
> 2. Tambahkan fitur **`Evolusi`**: Jika Pet sudah mencapai **Level 3**, tampilannya akan berubah secara permanen menjadi bentuk yang lebih keren (misal dari emoji bayi 👶 berubah jadi ksatria 🧑‍🎤 atau perubahan bentuk CSS).
>
> Tolong berikan kode lengkap yang sudah diperbarui dan jelaskan di bagian mana fungsi localStorage ini bekerja.

### 🇬🇧 English

> For the final step, I want to ensure the user's progress is saved and doesn't disappear when the page is refreshed.
>
> 1. Use **localStorage** to automatically save the pet's Level, EXP, and Mood whenever a change occurs. Load this data when the page is first opened.
> 2. Add an **`Evolution`** feature: Once the pet reaches **Level 3**, its visual appearance should permanently change into a cooler form (e.g., transforming from a baby emoji 👶 into a knight 🧑‍🎤, or a change in the CSS shapes).
>
> Please provide the fully updated code and explain where the localStorage logic is being handled.

---

## 📚 Konsep yang Dipelajari Per Iterasi

### Iterasi 1
- Struktur file HTML tunggal (all-in-one)
- CSS custom properties (variabel warna)
- `setInterval` dan `clearInterval` untuk countdown
- Responsive design dengan Flexbox/Grid

### Iterasi 2
- State management manual dengan objek JavaScript
- Conditional logic berdasarkan aksi user
- DOM manipulation untuk update UI secara real-time
- Sistem EXP dan leveling sederhana

### Iterasi 3
- `document.addEventListener('visibilitychange', ...)`
- `document.visibilityState` untuk deteksi tab aktif
- Membuat modal/overlay notifikasi secara programatik
- Menangani edge case dan exploit pada aplikasi

### Iterasi 4
- `localStorage.setItem()` dan `localStorage.getItem()`
- JSON serialization: `JSON.stringify()` dan `JSON.parse()`
- Load state saat `DOMContentLoaded`
- Conditional rendering berdasarkan level/state

---

## 💡 Tips untuk Instruktur

- Minta mahasiswa menjalankan setiap iterasi secara mandiri sebelum melihat solusi.
- Diskusikan mengapa **state management** penting bahkan di aplikasi kecil sekalipun.
- Iterasi 3 adalah titik kritis — dorong mahasiswa untuk memikirkan *"bagaimana user bisa menyalahgunakan aplikasi ini?"*
- Iterasi 4 membuka diskusi tentang **keamanan client-side storage** vs **server-side storage**.

---

*Dibuat untuk keperluan pembelajaran pemrograman web interaktif.*
