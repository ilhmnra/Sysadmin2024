---
marp: true
theme: uncover
_class: invert
---
# SISTEM ADMINISTRASI 3122600024 AULIA ILHAM

---
# <!--fit-->
1. **Sumber Perangkat Lunak Debian GNU/Linux:**
   Debian menggunakan metodologi repositori untuk mendistribusikan aplikasi. Ini memungkinkan sentralisasi perangkat lunak dan penggunaan antarmuka sederhana untuk mengelola dan mengupgrade sistem tanpa harus mengunjungi situs perangkat lunak itu sendiri.
---
# <!--fit-->
2. **Berkas sources.list:**
   Alamat Internet repositori Debian disimpan dalam berkas /etc/apt/sources.list, dan juga dalam berkas dengan tipe /etc/apt/sources.list.d/xxx.list. Untuk mengedit dan memodifikasi berkas sources.list, Anda dapat menggunakan salah satu perintah berikut (dalam mode administrator): `apt edit-sources` atau `nano /etc/apt/sources.list`.

   Contoh isi berkas sources.list:
   ```plaintext
   deb http://deb.debian.org/debian/ bookworm main non-free-firmware
   deb-src http://deb.debian.org/debian/ bookworm main non-free-firmware
   deb http://security.debian.org/debian-security bookworm-security main non-free-firmware
   ```
---
# <!--fit-->
3. **Tentang Repositori, Cabang, dan Bagian/Komponen:**
   Debian mengorganisir paket perangkat lunaknya dalam repositori yang terbagi dalam cabang dan bagian/komponen. Ada empat bagian resmi dalam repositori Debian: "main", "non-free-firmware", "contrib", dan "non-free". Bagian "main" adalah yang secara resmi didukung oleh proyek Debian dan sepenuhnya bersifat perangkat lunak bebas.
---
# <!--fit-->
4. **Paket Backport:**
   Debian juga menyediakan repositori khusus yang disebut backports, yang berisi versi lebih baru dari beberapa aplikasi. Repositori ini tidak diaktifkan secara default dan tidak menimbulkan risiko khusus. Backport memungkinkan aplikasi dari repositori pengembangan untuk dipindahkan kembali ke versi "stable".

   Lebih banyak detail tentang Backports dapat ditemukan di [Debian Wiki tentang Backports](https://wiki.debian.org/Backports).
---
# <!--fit-->
5. **Memodifikasi Repositori:**
   Sebelum memodifikasi sumber perangkat lunak sistem, perlu menyadari risiko penggunaan komponen "contrib" atau "non-free". Risiko melibatkan kebebasan paket, dukungan proyek Debian, dan kemungkinan kontaminasi sistem Debian yang sepenuhnya bebas.

   Contoh perintah untuk memodifikasi sources.list:
   ```bash
   apt edit-sources
   ```
   Juga dapat dimodifikasi menggunakan pengelola paket grafis seperti Synaptic.
---
# <!--fit-->
6. **Perintah Apt untuk Pencarian dan Tampilan Informasi:**
   Ada beberapa perintah Apt yang dapat dieksekusi sebagai pengguna biasa untuk menampilkan informasi paket seperti `apt show foo`, mencari paket dengan `apt search foo`, dan menampilkan versi yang tersedia dengan `apt-cache policy foo`.
---
# <!--fit-->
7. **Perintah Apt untuk Pemeliharaan Sistem dalam Mode Administrator:**
   Beberapa perintah Apt yang memerlukan hak administrator, seperti `apt update` untuk memperbarui metadata repositori, `apt install foo` untuk menginstal paket, dan `apt upgrade` untuk memperbarui paket yang terinstal secara aman.
---
# <!--fit-->
8. **Perintah Apt untuk Pemeliharaan Penuh Sistem dalam Mode Administrator:**
   Perintah seperti `apt full-upgrade` dapat digunakan untuk memperbarui paket yang terinstal dengan menambahkan/menghapus paket lain jika diperlukan. Ada juga perintah untuk menghapus paket, membersihkan cache, dan lainnya.
---
# <!--fit-->
9. **Manajer Paket Perangkat Lunak (Software):**
   Software adalah manajer sederhana untuk aplikasi Debian, memungkinkan pencarian, instalasi, penghapusan, dan pembaruan paket.
---
# <!--fit-->
10. **Cari dan Instalasi Aplikasi dengan Software:**
    Pengguna dapat mencari dan menginstal aplikasi dengan mudah melalui antarmuka Software. Cukup klik pada deskripsi aplikasi dan pilih "Install".
---
# <!--fit-->
11. **Pembaruan Aplikasi dengan Software:**
    Pengguna dapat memperbarui sistem dari bagian "Updates" dan melihat pembaruan yang tersedia atau sudah diunduh.
---
# <!--fit-->
12. **Penghapusan Aplikasi dengan Software:**
    Pengguna dapat menghapus aplikasi yang terinstal melalui kategori "Installed" dan memilih "Remove".
---
# <!--fit-->
13. **Pembaruan Sistem Umum:**
   Bagian ini membahas pembaruan umum sistem, termasuk pembaruan keamanan, perbaikan bug, dan peningkatan kinerja. Software: tab pembaruan menunjukkan opsi untuk memulai pembaruan sistem dan mengharuskan restart setelahnya.
---
# <!--fit-->
14. **Mengelola Repositori untuk Pembaruan Perangkat Lunak:**
   Pengguna diberikan panduan untuk mengelola repositori perangkat lunak Debian secara grafis menggunakan aplikasi "Software". Ini termasuk menambahkan sumber "non-free" dan menentukan frekuensi pembaruan.
---
# <!--fit-->
15. **Mengganti Konfigurasi Repositori:**
   Setelah mengubah repositori, pengguna harus me-reload paket informasi. Jendela pesan akan memberi tahu jika informasi paket terbaru sudah usang dan memerlukan pembaruan.

16. **Pilihan Pengaturan Otomatis untuk Pembaruan:**
   Panduan mencakup cara mengaktifkan pembaruan otomatis menggunakan mekanisme yang disediakan oleh aplikasi "Software". Pengguna dapat mengatur preferensi pembaruan otomatis dan mendapatkan notifikasi ketika pembaruan telah diinstal.
---
# <!--fit-->
17. **Manajemen Aplikasi dengan Discover (KDE):**
   Discover adalah antarmuka pengguna grafis yang memungkinkan pencarian, instalasi, dan pembaruan aplikasi. Panduan mencakup cara mencari, menginstal, dan menghapus aplikasi menggunakan Discover.
---
# <!--fit-->
18. **Menambahkan dan Menghapus Komponen Plasma (KDE):**
   Discover memungkinkan pengguna menambahkan komponen tambahan ke lingkungan Plasma mereka. Panduan memberikan petunjuk tentang cara menemukan dan menginstal komponen Plasma melalui Discover.
---
# <!--fit-->
19. **Menghapus Aplikasi dengan Discover:**
   Panduan menunjukkan cara menghapus aplikasi yang telah terinstal melalui Discover, yaitu dengan mengunjungi kategori "Installed" dan mengklik "Remove".
---
# <!--fit-->
20. **Memperbarui Aplikasi dengan Discover:**
   Proses pembaruan aplikasi dijelaskan, termasuk cara memeriksa pembaruan secara manual dan melalui tombol yang disediakan dalam antarmuka Discover.
---
# <!--fit-->
21. **Manajemen Repositori dengan Synaptic:**
   Synaptic dijelaskan sebagai antarmuka grafis yang lebih rinci dan komprehensif untuk manajemen paket Debian. Panduan memberikan gambaran tentang cara menggunakan Synaptic, termasuk me-reload paket, pencarian, dan pengaturan pembaruan.
---
# <!--fit-->
22. **Perhatian pada Keamanan dan Konfirmasi Tindakan:**
    Setiap tindakan yang melibatkan perubahan pada perangkat lunak meminta konfirmasi dan kata sandi administrator. Pengguna disarankan untuk berhati-hati dan memastikan adanya koneksi internet yang berfungsi saat melakukan instalasi atau pembaruan.
---
# <!--fit-->
23. **Periksa Pembaruan Secara Manual:**
    Panduan menyajikan cara memeriksa pembaruan secara manual dan mengupdate aplikasi dengan mengklik tombol yang sesuai.
---
# <!--fit-->
24. **Manajemen Repositori dengan Discover (KDE):**
    Discover pada KDE memberikan opsi untuk mengelola repositori. Pengguna dapat mengubah sumber-sumber aplikasi dan memodifikasi repository.
---
# <!--fit-->
25. **Mengelola Aplikasi Flatpak dari Terminal:**
    Bagian ini memberikan daftar perintah dasar untuk mengelola aplikasi Flatpak melalui terminal.
---
# <!--fit-->
   - `flatpak search flatpak_name`: Mencari aplikasi Flatpak dalam semua repositori.
   - `flatpak install repository flatpak_name`: Menginstal aplikasi Flatpak dari repositori.
   - `flatpak uninstall flatpak_name`: Menghapus aplikasi Flatpak.
   - `flatpak uninstall --unused`: Menghapus dependensi yang tidak digunakan.
   - `flatpak update`: Memperbarui semua aplikasi Flatpak yang terinstal.
   - `flatpak run flatpak_name`: Menjalankan aplikasi Flatpak.
---
# <!--fit-->
 26.  **Instalasi Flatpak untuk Pengguna Saat Ini dengan Opsi "--user":**
   Untuk menginstal Flatpak hanya untuk pengguna saat ini dengan opsi "--user", file akan ditempatkan di direktori pengguna (SHOME/.local/share/flatpak/).
   Contoh penggunaan dengan LibreOffice:
   - `flatpak --user install repository flatpak_name`: Contoh instalasi LibreOffice dari Flathub.
   - `flatpak install flathub org.libreoffice.Libreoffice`: Instalasi LibreOffice dari Flathub.
---
# <!--fit-->
27. **Menghapus Aplikasi Flatpak yang Terinstal Secara Grafis:**
   Jika Anda telah menginstal Flatpak melalui antarmuka grafis seperti Software atau Discover, cukup hapusnya dari menu aplikasi yang terinstal pada manajer perangkat lunak Anda. Cari Flatpak yang ingin dihapus dan mulai proses penghapusan dengan mengeklik tombol yang ditujukan.

---
# <!--fit-->
28. **Penting: Uninstall Semua Ketergantungan (Dependencies):**
   Perlu diingat bahwa jika Anda ingin menghapus semua dependensi (perangkat lunak yang terinstal tambahan selain Flatpak untuk operasinya), Anda harus menjalankan perintah berikut di terminal:
   ```
   flatpak uninstall --unused
   ```
---
# <!--fit-->
29. **Repositori Flathub:**
   Repositori Flathub (https://flathub.org/) adalah tempat berkumpulnya berbagai aplikasi. Untuk menambahkan repositori ini, gunakan perintah berikut:
   ```
   flatpak remote-add flathub https://flathub.org/repo/flathub.flatpakrepo
   ```
   Anda dapat menggunakan opsi "--if-no-exists" untuk menghindari kesalahan yang dihasilkan oleh duplikat.

---
# <!--fit-->
30. **Repositori Flatpak KDE:**
   Repositori Flatpak KDE dapat ditambahkan menggunakan perintah berikut:
   ```
   flatpak remote-add kdeapps https://distribute.kde.org/kdeapps.flatpakrepo
   ```
---
# <!--fit-->
31. **Repositori Flatpak Gnome-nightly:**
   Repositori Flatpak Gnome-nightly, yang berisi versi terbaru dari Gnome, dapat ditambahkan dengan perintah:
   ```
   flatpak remote-add gnome-nightly https://nightly.gnome.org/gnome-nightly.flatpakrepo
   ```
# <!--fit-->