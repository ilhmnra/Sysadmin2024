**Nama** : Aulia Ilham </br>
**NRP** : 3122600024 </br>
**Kelas** : 2 D4 IT A </br>


# Jawaban intuk pertanyaan tambahan yang diberikan oleh Bapak Dr Ferry Astika Saputra ST, M.Sc	
**Pertanyaan : "apa yang dimaksud dari busy system, busy user, busy lowait, busy irqs, busy other, idle in this?"**

Dalam konteks pemantauan sistem menggunakan Grafana dan Prometheus, metrik yang ditampilkan seperti "Busy System," "Busy User," "Busy Iowait," "Busy IRQs," "Busy Other," dan "Idle" merujuk pada bagaimana CPU menghabiskan waktu pemrosesannya. Berikut adalah penjelasan untuk masing-masing metrik tersebut:

1. **Busy System**:
   - Mengindikasikan waktu CPU yang dihabiskan untuk menjalankan kode kernel (operasi sistem).
   - Ini termasuk semua aktivitas yang dilakukan oleh sistem operasi seperti manajemen memori, proses interupsi, dan tugas sistem lainnya.

2. **Busy User**:
   - Menunjukkan waktu CPU yang digunakan untuk menjalankan kode aplikasi atau proses pengguna.
   - Ini adalah waktu yang dihabiskan untuk menjalankan program dan aplikasi yang Anda jalankan di komputer Anda.

3. **Busy Iowait**:
   - Waktu CPU yang dihabiskan menunggu operasi I/O (Input/Output) untuk selesai.
   - Ini menunjukkan berapa banyak waktu CPU yang tidak aktif karena menunggu aktivitas seperti membaca atau menulis ke disk, atau menunggu respons jaringan.

4. **Busy IRQs**:
   - Waktu yang dihabiskan untuk menangani interupsi perangkat keras.
   - Interupsi adalah sinyal dari perangkat keras (seperti keyboard, mouse, jaringan) yang memerlukan perhatian CPU.

5. **Busy Other**:
   - Ini bisa mencakup berbagai jenis waktu sibuk CPU yang tidak terklasifikasikan dalam kategori lain.
   - Bisa mencakup waktu yang dihabiskan untuk menangani tugas-tugas khusus yang tidak termasuk dalam kategori user, system, atau iowait.

6. **Idle**:
   - Waktu di mana CPU tidak melakukan apapun dan dalam keadaan siaga.
   - Ini menunjukkan berapa banyak waktu CPU yang tersedia untuk tugas lain.

Grafik tersebut membantu dalam memahami seberapa besar beban kerja yang ada pada sistem dan bagaimana sumber daya CPU digunakan dalam berbagai kategori tugas. Dari sini, Anda dapat mengidentifikasi potensi bottleneck (kemacetan) dalam sistem dan melakukan optimisasi sesuai kebutuhan.


**Pertanyaan : "Kalau di windows, prometheus dapat data cpu usage, ram usage dan data lain lain dari mana?"**

Di Windows, Prometheus mendapatkan data penggunaan CPU, penggunaan RAM, dan metrik lainnya melalui aplikasi monitoring seperti Node Exporter for Windows. Node Exporter adalah aplikasi yang mengumpulkan data dari sistem dan mengekspornya ke Prometheus untuk diproses dan ditampilkan di Grafana. Untuk Windows, ada beberapa cara untuk mengumpulkan data ini:

1. **WMI Exporter**:
   - WMI Exporter (Windows Management Instrumentation Exporter) adalah solusi populer untuk mengumpulkan metrik dari sistem Windows.
   - WMI Exporter mengumpulkan data menggunakan WMI, yang merupakan kerangka kerja manajemen yang terintegrasi dalam Windows untuk mengakses informasi sistem.
   - Data yang dikumpulkan termasuk penggunaan CPU, penggunaan RAM, disk I/O, jaringan, dan metrik sistem lainnya.
   - Cara penggunaannya melibatkan instalasi WMI Exporter pada mesin Windows, menjalankannya sebagai layanan, dan mengkonfigurasi Prometheus untuk mengumpulkan data dari WMI Exporter.

2. **Node Exporter for Windows (Metode yang Kami Gunakan)**:
   - Node Exporter untuk Windows adalah adaptasi dari Node Exporter asli yang ditujukan untuk sistem operasi Linux.
   - Exporter ini bekerja dengan cara yang mirip dengan WMI Exporter, namun dirancang khusus untuk mengumpulkan metrik dari sistem Windows.
   - Data yang dikumpulkan termasuk metrik dasar CPU, memori, disk, dan jaringan.
