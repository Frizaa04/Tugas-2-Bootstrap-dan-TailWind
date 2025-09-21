# Responsive Layout & Tailwind Utility Classes

## 1. Keputusan Grid-cols/Gap di Tiap Breakpoint
Pada setiap breakpoint, keputusan jumlah kolom grid-cols dan jarak antar elemen gap ditentukan berdasarkan:
- **Ukuran layar pengguna**: Mobile cenderung memakai grid-cols-1 atau grid-cols-2 agar konten tetap terbaca tanpa scrolling horizontal.
- **Kerapatan informasi**: Di layar yang lebih besar (tablet/desktop), kolom bisa ditambah grid-cols-3, grid-cols-4`, dst. karena ruang lebih lebar.
- **Estetika & keterbacaan**: gap lebih kecil di mobile agar hemat ruang, sedangkan di desktop bisa diperlebar untuk memberikan white space yang lebih nyaman.

Contoh:
``` html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
```

## 2. Pemanfaatan Utility Responsive Tailwind untuk Mobile
Utility responsive Tailwind sangat membantu memecahkan masalah layout di mobile dengan cara:
- **Stacking content**: Mengubah layout horizontal menjadi vertikal di mobile (flex-col vs flex-row).
- **Mengatur ukuran font & spacing**: Contoh text-sm sm:text-base lg:text-lg.
- **Hide/Show elemen**: Menggunakan hidden sm:block untuk menyembunyikan konten yang tidak penting di layar kecil.
- **Menjaga keterbacaan**: Padding (p-2 sm:p-4) disesuaikan agar konten tidak terlalu rapat di layar kecil.

## 3. Trade-off utility classes vs CSS tersendiri
- **utility**: Memiliki kecepatan dan konsisten dalam membuat sebuah design dan mudah diubah di level komponen. Namun menumpuk banyak class di HTML dapat membuat kode sulit untuk di baca dan sulit untuk memakai ulang jika ada banyak elemen yang serupa.
- **CSS**: Kode tampilan HTML menjadi lebih bersih dari pada utility dan dapat di pakai berulang kali. Jika ada sebuah perubahan yang cukup besar mudah untuk mengaturnya namun ini juga sebuah masalah jika perubahan kecil maka dibutuhkan untuk mengupdate CSSnya karena tidak bisa langsung dari class di HTML. 