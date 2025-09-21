## 1. Mengapa memilih konfigurasi column tertentu untuk tiap breakpoint?

pilihan col ini mengikuti prinsip responsive grid Bootstrap: jumlah kolom menyesuaikan lebar device agar tata letak tetap rapi dan konsisten.

## 2. Bagaimana memastikan tombol Follow / Edit Profile tetap mudah dijangkau di mobile?**

tombol memenuhi 1 baris penuh, sehingga mudah diklik dengan jari. Di mobile tombol dipindah ke bawah bio, lebih natural dan tidak menekan area atas.

## 3. Jika postingan bertambah jadi 50, apa potensi masalah dan bagaimana solusi gridmu mengatasinya?**

**Potensi masalah**:
User harus scroll panjang.
Page load lebih lambat karena semua foto dimuat sekaligus.
Grid bisa terlalu padat jika tidak konsisten.

**Solusi dengan grid di kode kamu**:
Grid Bootstrap dengan .row g-3 otomatis menjaga jarak antar card meski jumlah foto bertambah. Jadi 50 foto tetap rapi tanpa pecah layout.

